# node-lp

node-lp is an adapter to the unix 'lp(1)' command allowing files to be submitted for printing or altering a pending job. This will only work on Linux at the moment however if anyone wants a windows port then that might happen.

## Requirements

You need `cups` installed to use this module.

## Installation

node-lp can then be installed via NPM

```sh
npm install node-lp
```

Then, require the module

```js
var lp = require("node-lp");
var options = {};

printer = lp(options);

printer.queue ("/tmp/test-file.pdf");
```

## Usage

```js
lp.queue(fileLocation, callback)

lp.queue(buffer, callback)

lp.stop(jobid)

lp.resume(jobid)

lp.hold(jobid)
```

## Options Available

Option | Description
------ | ----------
destination | Prints files to the named printer.
hostname | Chooses an alternate server.
port | Chooses an alternate server port (only use if hostname is specified).
username | Specifies the username to use when connecting to the server.
encryption | Forces encryption when connecting to the server.
digitalCopy | Allows logging of what excatly is being printed.
args | Pass custom arguments to lp (in array).

## Licence

Licensed under the [New BSD License](http://opensource.org/licenses/bsd-license.php)
