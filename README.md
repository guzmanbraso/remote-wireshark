remote-wireshark
================

Simple script to run wireshark locally getting traffic dump from a remote host through ssh + tcpdump.

Requirements
------------

It assumes you have sudo working on the remote host and passwordless access to tcpdump through sudo.

Usage
-----

./remote-wireshark.sh "[SSH CREDENTIALS AND EXTRA OPTIONS]" "[TCPDUMP EXTRA OPTIONS]"

Examples
--------

Showing web traffic on eth0 for user@host: 
```./remote-wireshark.sh "user@host" "-i eth0 port 80"
```

Connecting though a different port to sniff google dns traffic:
```./remote-wireshark.sh "-p 9999 user@host" "-i eth1 host 8.8.8.8 or host 8.8.4.4"
```
