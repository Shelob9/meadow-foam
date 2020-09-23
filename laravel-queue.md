# Laravel Queues

- [Learn Laravel Queues](https://learn-laravel-queues.com) - 5 stars! Buy This.

## Serial Vs Parallel Requests With Laravel Queues

A chain of jobs is executed in series, one after another. Batching can be used to run jobs in paralled. In both cases, you can call a funcion when its done or when an error is caught.

On Vapor, queues are not first in first out -- FIDO -- and jobs can run more then once. So whether jobs are in chain or dispatched in a loop, they will run out of order.

### Science

I wrote two commands, that dispatch this job a hundred times:

```php
<?php

namespace App\Jobs;

use Illuminate\Bus\Queueable;
use Illuminate\Contracts\Queue\ShouldQueue;
use Illuminate\Foundation\Bus\Dispatchable;
use Illuminate\Queue\InteractsWithQueue;
use Illuminate\Queue\SerializesModels;

class LogTimeAndArgsJob implements ShouldQueue
{
    use Dispatchable, InteractsWithQueue, Queueable, SerializesModels;

    /* @var int */
    protected $itteration;

    /* @var string */
    protected $command;

    /**
     * @param int $itteration
     * @param string $command
     */
    public function __construct(int $itteration, string $command)
    {
        $this->itteration = $itteration;
        $this->command = $command;
    }

    public function handle()
    {
        logger(sprintf('Itteration: %s Command: %s', $this->itteration,$this->command) );
    }
}
```

Using a loop to dipsatch jobs in order:

```php
Artisan::command('test:loop', function (){
    for( $i = 0;$i <=100;$i++){
      dispatch( new \App\Jobs\LogTimeAndArgsJob($i,'test:loop'));
    }

});
```

And using a chain:

```php
Artisan::command('test:chain', function (){
    $jobs = [];
    for( $i = 0;$i <=100;$i++){
        $jobs[] = new \App\Jobs\LogTimeAndArgsJob($i,'test:chain');
    }

    \Illuminate\Support\Facades\Bus::chain(
       $jobs
    )->catch(function() {
        logger('test:chain failed' );
    })->dispatch();
});
```

I deployed this to Vapor, and used Vapor UI to trigger both commands. As I expected, the jobs dispatched with a loop ran in mildly random order. The chain executed in order of itterations.

## Testing Queues

### Testing A Laravel Command That Dispatches A job

```php
//Mock Bus to test jobs dispatched
use Illuminate\Support\Facades\Bus;
//Mock queue to test jobs pushed into queue using a chain.
use Illuminate\Support\Facades\Queue;

class SomeTests exteds TestCase {
    public function testDispatches()
    {
        //Mock queue bus
        Bus::fake();
        $this->artisan('command that calls a job');
        //Assert command dispatched a job 2 times
        Bus::assertDispatched(WhateverJob::class,2);

    }

    public function testChained()
    {
        //Mock queue
        Queue::fake();
        $this->artisan('command that chaines');
        //Assert job was pushed one times
        Queue::assertPushed(WhateverJob::class,1);
    }
}
```
