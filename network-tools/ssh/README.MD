## Technical Overview
SSH (Secure Shell) is a network protocol that is used to secure communication between two devices over an unsecured network. It provides a secure channel for connecting to remote systems and enables the exchange of data between devices.

**Here is a technical overview of how SSH works**:

1. The client initiates an SSH connection by sending a request to the server.

1. The server responds with a public key and a server identification string.

1. The client verifies the server's identity using the server identification string and the server's public key. If the server's identity is verified, the client sends an acknowledgement to the server.

1. The server generates a random number (called the session key) and sends it to the client, encrypted with the client's public key.

1. The client decrypts the session key using its private key and sends an acknowledgement to the server.

1. Both the client and server use the session key to encrypt and decrypt data that is exchanged between them.

1. When the connection is closed, both the client and server discard the session key.

There are several versions of the SSH protocol, including SSH1, SSH2, and SSH2-Transport Layer Security (SSH2-TLS). The most widely used version is SSH2, which is designed to be more secure than SSH1 and includes additional features such as compression and connection multiplexing.

To use SSH, you will need an SSH client and an SSH server. The client is typically installed on the device that you want to use to connect to the remote system, and the server is installed on the remote system itself. There are several options for both SSH clients and servers, including command-line tools and graphical user interface (GUI) applications.
## SSH Options & What they do
list of some common options that can be used with ssh:

- **-L**: Tunnel mode. Tunnel a port from the local machine to the remote machine.
- **-R**: Reverse tunnel mode. Tunnel a port from the remote machine to the local machine.
- **-p**: Specify the port to use for the connection.
- **-i**: Specify the private key to use for authentication.
- **-t**: Force a pseudo-terminal allocation.
- **-v**: Verbose mode. Enable verbose output.
- **-o**: Specify options to pass to ssh.

**Example -L option to tunnel a port:**

```
ssh -L localhost:8888:localhost:80 user@remote
```
This will connect to the remote machine using the user account and tunnel the port 8888 on the local machine to port 80 on the remote machine. This can be useful for accessing a web server running on the remote machine from the local machine.

**Example -R option to tunnel a port in the opposite direction:**

```
ssh -R localhost:80:localhost:8888 user@remote
```
This will connect to the remote machine using the user account and tunnel the port 80 on the remote machine to port 8888 on the local machine. This can be useful for allowing the remote machine to access a server running on the local machine.

**Example -p option to specify the port to use for the connection:**

```
ssh -p 2222 user@remote
```
This will connect to the remote machine using the user account and the port 2222.


## Other Example Use Cases of SSH

**Connect to a remote machine and execute a command:**

```
ssh user@remote 'uptime'
```
This will connect to the remote machine using the user account and execute the uptime command, displaying the uptime of the remote machine.

**Connect to a remote machine and start an interactive session:**

```
ssh user@remote
```
This will connect to the remote machine using the user account and start an interactive session, allowing you to execute commands on the remote machine.

**Connect to a remote machine and tunnel a port:**

```
ssh -L localhost:8888:localhost:80 user@remote
```
This will connect to the remote machine using the user account and tunnel the port 8888 on the local machine to port 80 on the remote machine. This can be useful for accessing a web server running on the remote machine from the local machine.

**Connect to a remote machine using a specific private key:**

```
ssh -i /path/to/private/key user@remote
```
This will connect to the remote machine using the user account and the private key located at /path/to/private/key.

