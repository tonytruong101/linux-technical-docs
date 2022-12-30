## Technical Overview

Mtr (short for "My Traceroute") is a command-line utility that is similar to Traceroute. It is used to display the path that packets take from a source device to a destination device on a network, as well as the network performance along the path.

**Here is a technical overview of how Mtr works**:

1. Mtr sends a series of packets to the destination device, each with a gradually increasing Time-To-Live (TTL) value. The TTL value is a field in the packet header that specifies how many hops the packet can pass through before it is discarded.

1. As each packet passes through a router on the network, the router decrements the TTL value by 1. If the TTL value reaches 0, the router sends an error message back to the source device and discards the packet.

1. Mtr receives the error messages from the routers and displays the IP addresses and hostnames of the routers that the packets passed through, as well as the network performance along the path. The network performance is measured in terms of the round-trip time (RTT) of the packets, which is the time it takes for a packet to be sent to the destination device and receive a response.

## Mtr Options & What do they do

list of some common options that can be used with mtr:

- **-r**: Report the results continuously, updating the display every second.
- **-n**: Resolve IP addresses to hostnames.
- **-m**: Specify the maximum number of hops.
- **-c**: Specify the number of pings to send to each hop.
- **-s**: Specify the packet size (in bytes).
- **-i**: Specify the interval (in seconds) between pings.
- **-t**: Specify the ttl (time to live) value.

**Simple example of an Mtr command that displays the path and network performance from the source device to a destination device**:

```
mtr www.example.com
```
This command sends packets to the destination device at www.example.com and displays the path that the packets take through the network, along with the network performance along the path.

**Example -r option to report the results continuously:**

```
mtr -r example.com
```
This will perform a traceroute to the host example.com and report the results continuously, updating the display every second.

**Example -n option to resolve IP addresses to hostnames:**

```
mtr -n example.com
```
This will perform a traceroute to the host example.com and resolve the IP addresses to hostnames.


## Other Example Use Cases of Mtr

**Perform a traceroute to a specific host:**

```
mtr example.com
```
This will perform a traceroute to the host example.com, showing the hop-by-hop path and the round-trip times to each hop.


**Perform a traceroute to a specific host and report the results continuously:**

```
mtr -r example.com
```
This will perform a traceroute to the host example.com and report the results continuously, updating the display every second.

**Perform a traceroute to a specific host and resolve the IP addresses to hostnames:**

```
mtr -n example.com
```
This will perform a traceroute to the host example.com and resolve the IP addresses to hostnames.

**Perform a traceroute to a specific host and specify the maximum number of hops:**

```
mtr -m 20 example.com
```
This will perform a traceroute to the host example.com and specify the maximum number of hops as 20.

