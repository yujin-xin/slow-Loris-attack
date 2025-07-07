#Slowloris DDoS attack

run:
python3 slowloris.py -h to see the options

This is how the attack works
* Script run and opens lots of connections to a web server.
* Instead of finishing each request quickly, it sends tiny bits of data very slowly, just enough to keep the connection open.
* It never completes the full request, and it just keeps the connection half-open.
* Since Slowloris opens hundreds or thousands of these half-finished connections, the server becomes too busy to handle real users.
* The server runs out of available connections

