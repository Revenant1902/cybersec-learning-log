# IP & MAC Addressing

## IP Addresses
- **IPv4** — 32-bit, written in decimal (e.g. `192.168.1.1`), split into 4 octets (8 bits each). This is still the dominant addressing scheme.
- **IPv6** — 128-bit, written in hexadecimal (e.g. `2001:0db8::1`), created because IPv4's ~4.3 billion address space ran out. Not fully adopted everywhere yet, but increasingly common — worth being comfortable reading both.

## CLasses of IP Address
(images/ip.png)

## MAC Addresses
**MAC = Media Access Control.** A hardware address burned into a network interface card (NIC), used for local communication.

Format: `00-1A-2B-3C-4D-5E` (6 pairs of hex digits)
- **First 3 pairs (OUI — Organizationally Unique Identifier)** — identify the manufacturer (e.g. Dell, Intel, Cisco)
- **Last 3 pairs** — unique to that specific device

**Layer:** MAC operates at **Layer 2 (Data Link)** of the OSI model — related to switching, not routing. Switches use MAC addresses to forward frames within a local network; routers use IP addresses to forward packets between networks.

## Why This Matters for Pentesting
- IP addresses define your scope/targets in an engagement
- MAC addresses matter for local network attacks (ARP spoofing, MITM on a LAN) since Layer 2 has no built-in authentication of who's claiming which MAC