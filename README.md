# Encrypted Bind Shell in Python

A simple Python-based bind shell with AES encryption for secure communication between client and server. This project allows you to execute remote commands over a TCP connection while encrypting all traffic.

## Features

AES Encryption: All communication is encrypted using AES-256 in ECB mode.

Server/Client Mode: Can run as a bind shell server or connect as a client.

Multithreaded: Handles multiple connections concurrently.

Cross-platform: Works on Windows, Linux, and macOS (requires Python).

### Requirements

Python 3.8+

PyCryptodome

### Install dependencies:

pip install pycryptodome

### Usage

1. Run as Server (Bind Shell)
python bind_shell.py --listen


Starts the server on 0.0.0.0:1234.

Displays the AES encryption key generated for the session.

Waits for client connections.

2. Connect as Client
python bind_shell.py --connect <SERVER_IP> --key <AES_KEY>


Replace <SERVER_IP> with the server's IP address.

Replace <AES_KEY> with the key displayed on the server.

Example

Server:

python bind_shell.py --listen


Output:

Key -> a3f9c7e8b5d2f1a0e3b9c1d7a2f4e5d6...
[ -- Starting Bind Shell -- ]


Client:

python bind_shell.py --connect 192.168.1.10 --key a3f9c7e8b5d2f1a0e3b9c1d7a2f4e5d6...
[ Connecting to Bind Shell !! ]

### Important Notes

The encryption uses AES-256 in ECB mode. For higher security, consider using CBC with IVs.

This tool is for educational purposes only. Unauthorized access to systems is illegal.

Use a firewall and limit exposure when testing in real networks.
