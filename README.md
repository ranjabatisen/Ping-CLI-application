# Ping-CLI-application (Cloudflare internship 2020 application)

It is a small Ping CLI application for Linux. The CLI app accepts a hostname or an IP address as its argument, then sends ICMP "echo requests" in a loop to the target while receiving "echo reply" messages. It reports loss and RTT times for each sent message.


===========================================================

How to run the code

==========================================================


1. Compile the code
```
gcc ping.c -o ping
```

2. Run the program
```
sudo ./ping <hostname/ip address> [-t] <ttl_value>
```
(Here sudo is used since root access is needed for raw socket. Also, TTL argument is optional.)

Code can also be run as:
```
sudo ./ping <hostname/ip address>
```
(in this case, default ttl = 53)

Also, in program default ping packet size is 56, which translates into 64 ICMP data bytes when combined with the 8 bytes of ICMP header data.
