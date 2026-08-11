# TCP, UDP & the Three-Way Handshake

## TCP — Transmission Control Protocol
**Connection-oriented, reliable.** Guarantees delivery and correct order — used when accuracy matters more than speed.

Common uses: websites (HTTP/HTTPS), FTP, SSH

**The Three-Way Handshake** (how a TCP connection is established):
1. **SYN** — client sends a synchronize request to the server
2. **SYN-ACK** — server acknowledges and sends its own synchronize request back
3. **ACK** — client acknowledges — connection is now established

This handshake is *why* TCP is reliable — both sides confirm they're ready before data flows. It's also foundational to understanding port scanning (e.g. a SYN scan sends only the first packet to check if a port responds, without completing the full handshake).

**Common TCP-based ports:** HTTP = 80, HTTPS = 443

## UDP — User Datagram Protocol
**Connectionless, no delivery guarantee.** No handshake, no acknowledgment — just sends and hopes it arrives. Faster than TCP because there's no overhead from confirming delivery.

Common uses: video streaming, voice calls (VoIP), video calls — cases where speed matters more than occasionally losing a packet (a dropped frame in a call is preferable to lag from waiting for retransmission).

## Practical Note
Use **Wireshark** to actually watch a TCP three-way handshake happen live on the wire — seeing the SYN/SYN-ACK/ACK packets in real traffic makes this concept click a lot faster than reading about it.