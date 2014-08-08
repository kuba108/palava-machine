# PalavaMachine

PalavaMachine is a WebRTC signaling server. Signaling describes the process of finding other peers and exchange information about how to establish a media connection. It works together with the [palava-client](https://github.com/palavatv/palava-client).

The server is implemented in [EventMachine](http://rubyeventmachine.com/) and [Redis PubSub](http://redis.io/topics/pubsub) and communication to the clients is done via WebSockets. See it in action at [palava.tv.](https://palava.tv)

Checkout our [blog post](https://blog.palava.tv/2013/12/How_to_host_your_own_WebRTC_Video_Conferencing_on_ubuntu/) for information on how to setup your own palava!


## Installation & Usage

Make sure you have redis(http://redis.io/download) installed, then clone this repository and run

    $ bundle install

Start the server with

    $ bin/palava-machine

Alternatively, download the [palava_machine gem](http://rubygems.org/gems/palava_machine) from rubygems.org:

    $ gem install palava_machine

And run:

    $ palava-machine

### Deamonized Version

The PalavaMachine can be started as a daemon process for production usage:

    $ palava-machine-daemon start

Stop it with

    $ palava-machine-daemon stop

### Configure using Environment Variables

You can set the address of the redis server via environment variable. The default is 'localhost:6379'.

    $ export PALAVA_REDIS="some_ip:some_port"
    $ bin/palava-machine

### Specs

To run the test suite use

    $ rspec

## Credits

AGPLv3. Part of the [palava project](https://palava.tv).

    Copyright 2013 Jan Lelis       jan@signaling.io
    Copyright 2013 Marius Melzer   marius@signaling.io
    Copyright 2013 Stephan Thamm   thammi@chaossource.net
    Copyright 2013 Kilian Ulbrich  kilian@innovailable.eu

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU Affero General Public License as
    published by the Free Software Foundation, either version 3 of the
    License, or (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU Affero General Public License for more details.

    You should have received a copy of the GNU Affero General Public
    License along with this program. If not, see
    <http://www.gnu.org/licenses/>.
