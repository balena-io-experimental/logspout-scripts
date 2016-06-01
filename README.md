# logspout-scripts

Scripts for setting up logspout loggin containers in resin.io devices

## Installation

This script should be run withing a running application container of a resin device.
To access the application container, simply use the Terminal from the Dashboard or
connect to the device using `resin ssh`.

Assuming a debian-flavored base OS, the installation steps are:

1. `sudo apt-get update && apt-get install -y git jq`
2. `git clone https://github.com/resin-io-playground/logspout-scripts`

## Using

* `cd logspout-scripts`
* `LOGGING_SERVER="syslog+tcp://logstash.resin.io:5000" ./logsetup.sh create`. Set `LOGGING_SERVER` accordingly to point to your server.

If you need to remove logspout containers (e.g. you are no longer intersted in logging and want to preserve resources) simply run
* `./logsetup.sh teardown`

## Dependencies

* `jq >= 1.5`

## Support

If you're having any problem, please [raise an issue](https://github.com/resin-io-playground/logspout-scripts/issues/new) on GitHub and the Resin.io team will be happy to help.

## Contribute

- Issue Tracker: [github.com/resin-io/logspout-scripts/issues](https://github.com/resin-io/logspout-scripts/issues)
- Source Code: [github.com/resin-io/logspout-scripts](https://github.com/resin-io/logspout-scripts)`

## Licence

The project is licenced under the Apache 2.0 license.
