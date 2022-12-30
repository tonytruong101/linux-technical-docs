## Technical Overview

Netstat (short for "network statistics") is a command-line utility that is used to display information about the network connections of a system. It is commonly used for tasks such as identifying the active network connections of a system, analyzing the traffic on the network, and troubleshooting connectivity problems.

**Here is a technical overview of how Netstat works**:

1. Netstat reads the network statistics of the operating system and retrieves information about the network connections of the system. The network statistics include data such as the protocol, the local and remote IP addresses, the local and remote port numbers, and the state of the connection.

1. Netstat displays the network statistics in a tabular form. By default, Netstat displays the protocol, the local and remote IP addresses, and the local and remote port numbers of each active network connection.

1. Netstat provides a number of options that can be used to modify the information that is displayed, such as -a (display all active network connections), -r (display the routing table), and -i (display the network interfaces).

## Netstat Options & What they do

list of some common options that can be used with netstat:

- **-a**: Display all active network connections.
- **-r**: Display routing table information.
- **-i**: Display interface statistics.
- **-s**: Display network statistics.
- **-t**: Display only TCP connections.
- **-u**: Display only UDP connections.
- **-p**: Display the process ID or name associated with each connection.
- **--dport**: Display connections to the specified destination port.
- **--sport**: Display connections from the specified source port.

**Simple example of a Netstat command that displays the active network connections**:

```
netstat -a
```
This command displays the active network connections, including the protocol, the local and remote IP addresses, and the local and remote port numbers.

**Example -r option to display routing table information:**

```
netstat -r
```
This will display routing table information, showing the destination, gateway, and mask for each route.

**Example -i option to display interface statistics:**

```
netstat -i
```
This will display interface statistics, showing the name, MTU (maximum transmission unit), and number of packets and errors for each interface.


## Other Example Use Cases of AWK

**Display active TCP connections and their associated process IDs:**

```
netstat -t -p
```
This will display active TCP connections and their associated process IDs, which can be helpful for identifying which processes are using which connections.

**Display active network connections and their associated process names**:

```
netstat -a -p
```
This will display active network connections and their associated process names, which can be helpful for identifying which processes are using which connections.

**Display network statistics for a specific protocol:**

```
netstat -s -p protocol
```
This will display network statistics for the specified protocol (e.g., TCP, UDP).

**Display active network connections filtered by protocol and port number:**

```
netstat -a -p protocol --dport port
```
This will display active network connections for the specified protocol and port number.
