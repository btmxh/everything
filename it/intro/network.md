- a set of many [[computer]]s connected with each other via networking devices
- usage:
	- exchange [[info]]
	- sharing [[resources]]

- lines
	- no-line (vô tuyến) => mostly waves
	- yes-line (hữu tuyến) => cables, wires, etc.
- bandwidth: max speed of [[info]] transfer, measured in (10^sth) bits per second: bps, Kbps, Mbps, Gbps, etc.

- arch
	- protocol: how to interpret stuff that was transfered
	- topology: how stuff is transfered between [[computer]]: bus, ring, star, mesh, etc.
- fundamental action: transfer
	- each [[computer]] has its own ip addr
	- source [[computer]] send, target [[computer]] recv

categories
- pan: personal area network (bluetooth, nfc), only a few meters, some [[computer]]
- lan: local area network (wifi) smoll office, homes, neighborhood, few hundred [[computer]] max
- man: metroopolitan area network, a city, some geographical area, etc., million [[computer]]s
- wan: wide area network, gan: global area network => wide and big asf, e.g. internet

kinds
- client-server
- p2p
- combination of both

2 kinds of connection
- wired
	- PSTN (slow asf), ADSL: using static telephone network (Kbps < 14Mbps down, 1.4Mpbs up)
	- optical cables: GPON, FTTH (Gbps)
- wireless
	- 3G(7.2/2Mbps), 4G(150/50Mbps), 5G(10Gbps)
## addr
- identifier of computers in a network
- ip: a 32 bit string (ipv4) or 128 bit string (ipv6)
- domain name: a string that'll be mapped into ip by the dns for a user to do stuff on some site
	- [[computer]] don't use domain names to communicate
- dns (domain name service): sth that maps hostname to ip

**WWW**
- before 1990s, internet is limited to gov, labs, email, ftp, etc.
- the www solves this issue via html bla bla
- **url**: uniform resource locator
	- protocol (https://)
	- web site (google.com)
	- path/directory (torani/dev/nrs-impl-kt/output)
	- resource (scores.json)
- **http**: hypertext transfer protocol
- https: http + secure
	- these protocols use requests and response to communicate between clients and servers

