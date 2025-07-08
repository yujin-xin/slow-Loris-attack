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
