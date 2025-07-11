# Slowloris DoS Simulation Tool – Python CLI

## Overview
A Python-based command-line application that replicates the Slowloris Denial-of-Service (DoS) technique, designed for ethical testing, research, and understanding of application-layer DoS attacks. The tool targets HTTP servers by maintaining numerous half-open TCP connections, exhausting server resources without requiring high bandwidth.

## Key Features
* Low-Bandwidth DoS Simulation: Demonstrates how application-layer exhaustion attacks can be launched with minimal network traffic.
* Persistent Socket Handling: Opens multiple sockets and sends partial HTTP requests slowly to keep connections open as long as possible.
* Target Configuration: Accepts custom host, port, and connection count parameters via CLI.
* CLI-Based Operation: Lightweight and scriptable tool ideal for testing environments or controlled lab simulations.

## Use Cases
* Educational tool for understanding HTTP-based DoS attacks
* Internal red team or security lab testing scenarios
* Demonstrating the importance of rate limiting, timeout configuration, and reverse proxies in mitigating application-layer threats

## How Slow-loris Works
* The attack takes advantage of the fact that web servers have a limited number of concurrent connections they can handle. Slowloris opens many connections to the target server but sends HTTP requests very slowly and incompletely, keeping these connections alive for as long as possible.

## Result
* The server's connection pool becomes filled with these slow, incomplete requests
* Legitimate users can't establish new connections because the server has reached its maximum concurrent connection limit
* The server becomes unresponsive to real traffic

## How to use
Clone first the repository and proceed to the directory (follow the instruction bellow)
```bash
git clone https://github.com/yujin-xin/slow-Loris-attack
cd slow-Loris-attack
python slowloris.py -h
```

After running the `slowloris.py`, it will show you how to use it
```bash
usage: slowloris.py [-h] -t TARGET [-p PORT] [-i INTERVAL] [-d DURATION] [-s SOCKETCOUNT]
slowloris.py: error: the following arguments are required: -t/--target
```



## Mitigation
* Implementing connection timeouts for incomplete requests
* Limiting connections per IP address
* Using reverse proxies or load balancers that can handle slow connections better
* Employing web servers less vulnerable to this attack (like Nginx or IIS)


## Technical Stack
* Language: Python
* Networking: TCP/IP stack
* OSI Layer: TCP socket connections simulating incomplete HTTP headers
* Platform: Cross-platform
* Interface: Command-line interface (CLI)

## Benefits
* Reinforces understanding of low-and-slow DoS techniques used in real-world scenarios
* Aids in testing server resilience and tuning timeout or resource handling configurations
* Enhances both red team and blue team knowledge by showing how subtle attacks evade basic detection

## Note
Designed strictly for educational and controlled testing environments. Unauthorized use against systems without explicit permission violates ethical standards and legal boundaries.
