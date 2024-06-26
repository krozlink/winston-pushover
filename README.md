# winston-pushover

[![Build Status](https://img.shields.io/travis/matthewtole/winston-pushover.svg?style=flat-square)](https://travis-ci.org/matthewtole/winston-pushover)
[![Dependency Status](https://img.shields.io/david/matthewtole/winston-pushover.svg?style=flat-square)](https://david-dm.org/matthewtole/winston-pushover)
[![npm Version](https://img.shields.io/npm/v/winston-pushover.svg?style=flat-square)](https://www.npmjs.org/package/winston-pushover)

A [Winston][0] transport that outputs using the [Pushover][1] service.

## Usage

``` js
  var winston = require('winston');

  // Requiring `winston-pushover` will expose `winston.transports.Pushover`
  require('winston-pushover').Pushover;

  winston.add(winston.transports.Pushover, options);
```
The Pushover transport takes the following options. Both 'userKey' and 'token' are required:

* __level:__ Level of messages that this transport should log, defaults to 'info'.
* __silent:__ Boolean flag indicating whether to suppress output, defaults to false.
* __userKey:__ The user key for the Pushover user who will receive the notifications.
* __token:__ The Pushover API token for your application.
* __sound:__ Which custom notification sound to use (optional).
* __messageFormatter:__ A function that takes a message object and returns the formatted string that will be displayed in the notification (optional).
* __getMessagePriority:__ A function that takes a log level and returns the pushover priority level to be used (optional).

## Dependencies

* [node-pushover][2]
* [winston][3]

## Installation

### Installing npm (node package manager)

``` bash
  $ curl http://npmjs.org/install.sh | sh
```

### Installing winston-pushover

``` bash
  $ npm install winston
  $ npm install winston-pushover
```

#### Author: [Matthew Tole](http://matthewtole.com)

[0]: https://github.com/flatiron/winston
[1]: https://pushover.net/
[2]: https://github.com/qbit/node-pushover
[3]: https://github.com/flatiron/winston
