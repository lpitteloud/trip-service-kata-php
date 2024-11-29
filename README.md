PHP kata from https://github.com/sandromancuso/trip-service-kata

To execute the unit tests you need to run :

```shell
composer test
```

## Coverage

To run with coverage you will have to configure your system with this:

Linux and macOS
```shell
export XDEBUG_MODE=coverage
```

Windows
```shell
set XDEBUG_MODE=coverage
```

When running the tests a coverage report should be generated automatically in simple text format and html report. If you want
to visualize it from the browser you can open the `coverage/report/index.html` file in a browser after running the tests.

Enjoy
