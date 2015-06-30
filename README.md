## ship-syslog
Adaptation of andrewhodel's [node-listen-udp-syslog](https://github.com/andrewhodel/node-listen-udp-syslog).
Written for OS X 10.10, because ALS still uses BSD-style syslog where time has no timezone component. Waaat?

It's basically a syslog UDP server for handling RFC5424 messages (http://tools.ietf.org/html/rfc5424) over UDP (http://tools.ietf.org/html/rfc5426).
It parses the messages to JSON and forwards them to an arbitrary server, specified as a parameter or SHIP_SYSLOG_HOST environment variable

## Running

`app.js` provides an example of how to include and configure the library, as well as process received UDP syslog messages.

`node app.js`

will listen on port 1514 and echo messages to the console

## Still in progress
 - attaching timezone to dates
