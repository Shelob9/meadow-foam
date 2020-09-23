# Laravel Vapor

- [Serverless Laravl Course](https://serverlesslaravelcourse.com/)

## Database

Find this sticky note.

- Serverless vs Fixed
  - Aurora takes too long to scale up for many app types.
    - Minumuma capactity with automatic scaling is an advantage of serverless.
    - Will not pay most of the time for staging database, beacuse its paused.
    - Cost is complex and can be real expensive.
    - Requires a VPC.
    - Self-healing and more throughput.
  - Over-provisioning a RDS is fixed cost, still managed.
    - Probably over-paying, but predictable cost.
    - Risk is high traffic breaking DB
      - Limit queue concurrency.
      - Add Redis cache level.
- Scaling/ Failover
  - A failover database comes online if production db goes down.
    - Failover takes ~60 or more.

## Queues

- With standard queue, can not assume order. Can not assume that job will only run once.
- Assume SQS is down, to prevent loosing jobs. Always use retry.
  - https://laravel.com/docs/8.x/helpers#method-retry
- Queues run in there [own Lamda](https://blog.laravel.com/vapor-using-a-separate-lambda-function-for-queues).
  - Use `queue-memory` to set the RAM.

### Retry Laravel Job

- https://serverlesslaravelcourse.com/video/27

```php
      return retry(20, function () {
          dispatch( new SomeJob( ) );
      }, 200 );
```

### Ensuring A Job Only Runs Once

- https://serverlesslaravelcourse.com/video/28
- Set a queue timeout. Something a little longer then longest jobs.
- Default timeout is 70s, so then it runs again. Potential loop.
- Job timing out is fine, job running multiple times is not.
- Always check database is onlin.

## Other

- "warn" - avoid 2s post-deploy delay.
  - Bring X containers online before deployment and rewarmed every 5 minutes.
  - Warming, not too expensive. Polling warms for 40 containers would be ~\$1.
- Concurrency
  - Warming can slow requests happening during warming. Concurrency keeps X containers always online.
  - Could mean paying to keep things online all the, or could avoid paying for warming. Can save a lot of money, if enough consitent traffic.
