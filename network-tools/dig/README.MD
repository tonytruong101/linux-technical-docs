## Technical Overview

Dig (short for "Domain Information Groper") is a command-line utility that is used to query Domain Name System (DNS) servers for information about domain names and IP addresses. It is commonly used for tasks such as troubleshooting DNS issues, analyzing the DNS configuration of a domain, and testing the performance of DNS servers.

**Here is a technical overview of how Dig works**:

1. Dig sends a query to a DNS server and asks for information about a specific domain name or IP address. The query is sent using the DNS protocol, which is a standard for transmitting DNS data over the internet.

1. The DNS server receives the query and responds with the requested information, if it is available. The response is a packet of data that contains the DNS record for the domain name or IP address, along with other information such as the IP addresses of the DNS servers and the time-to-live (TTL) value of the record.

1. Dig displays the response from the DNS server in a format that is easy to read and understand. By default, Dig displays the DNS record for the domain name or IP address, along with the IP addresses of the DNS servers and the TTL value of the record.


## Dig Options & What do they do

list of some common options that can be used with dig:

- **+short**: Display the results in a short format (i.e., just the record values).
- **+nocmd**: Suppress the initial comment lines.
- **+noquestion**: Suppress the question section.
- **+noauthority**: Suppress the authority section.
- **+noadditional**: Suppress the additional section.
- **+multiline**: Print the results in a multi-line format.
- **+tries=N**: Set the number of tries.
- **+time=N**: Set the initial time-out value.
- **@server**: Use the specified server for the DNS lookup.

**Simple example of a Dig command that queries a DNS server for information about a domain name**:

```
dig www.example.com
```
This command sends a query to a DNS server and asks for information about the domain name www.example.com.


**Example +short option to display the results in a short format:**

```
dig example.com +short
```

**Example +nocmd and +noquestion options to suppress the initial comment lines and question section:**

```
dig example.com +nocmd +noquestion
```
This will perform a DNS lookup for the domain name example.com and suppress the initial comment lines and question section.

**Example +noauthority option to suppress the authority section:**

```
dig example.com +noauthority
```
This will perform a DNS lookup for the domain name example.com and suppress the authority section. The authority section of the output contains information about the name servers responsible for the domain. By using the +noauthority option, the authority section will not be included in the output.


##Other Example Use Cases of AWK

**Perform a DNS lookup for a specific record type:**

```
dig example.com MX
```
This will perform a DNS lookup for the MX (mail exchange) record of the domain name example.com. The output will include the MX record value(s).

**Perform a DNS lookup for a domain name and display the results in a specific format:**

```
dig example.com +short
```
This will perform a DNS lookup for the domain name example.com and display the results in a short format (i.e., just the record values).

## Use Case Examples with different dig Options

**Perform a DNS lookup for a domain name and suppress the initial comment lines and question section:**

```
dig example.com +nocmd +noquestion
```
This will perform a DNS lookup for the domain name example.com and suppress the initial comment lines and question section.

**Perform a DNS lookup for a domain name and print the results in a multi-line format:**

```
dig example.com +multiline
```
This will perform a DNS lookup for the domain name example.com and print the results in a multi-line format.

**Perform a DNS lookup for a domain name and set the number of tries to 3:**

```
dig example.com +tries=3
```
This will perform a DNS lookup for the domain name example.com and set the number of tries to 3.


**Perform a DNS lookup for a domain name and set the initial time-out value to 5 seconds:**

```
dig example.com +time=5
```
This will perform a DNS lookup for the domain name example.com and set the initial time-out value to 5 seconds.

