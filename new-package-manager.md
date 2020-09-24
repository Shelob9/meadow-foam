# New Package Manager

What is there was a JavaScript and PHP package manager that was designed to manage dependencies, script running, etc for BOTH.

## Problems

- Have to write some scripts with yarn/npm and some with composer. Then glue them toghether with bash or choose one to run the other.
- npm doesn't know about PHP autoloader. Composer doesn't know about package.json bin/main and other entries.
- Composer installs dev dependencies of dependencies in development. Sometimes that's what you want. Othertimes:
  - You don't need those dependencies.
  - The dev dependencies clash with yours.
  - It would be better to run application's test with no-dev/dist version of the dependency anyway.
- No, recursive install of dependencies in composer makes WordPress plugins using composer in a full site managed by composer a mess.
- composer.lock confuses me.
