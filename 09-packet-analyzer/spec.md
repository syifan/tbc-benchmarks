# Packet Sniffer & Protocol Analyzer

## What do you want to build?

Build a network packet sniffer and protocol analyzer in Python that captures live network traffic, dissects packets across protocol layers, and presents results in both a CLI interface and a web-based dashboard.

The implementation must include:
- Raw packet capture using libpcap (via ctypes or scapy as capture backend only)
- Protocol dissection — implemented from scratch for: Ethernet, IPv4, IPv6, TCP, UDP, ICMP, DNS, HTTP/1.1, TLS (handshake parsing only), ARP
- Packet reassembly: TCP stream reassembly for HTTP content extraction
- BPF filter support (e.g., "tcp port 80")
- PCAP file reading and writing
- Statistics: packets/sec, bytes/sec, protocol distribution, top talkers (by IP)
- Anomaly detection: port scan detection, SYN flood detection, DNS tunneling heuristics
- CLI interface with live scrolling packet display (like tcpdump but with colors and decoded fields)
- Web dashboard (Flask/FastAPI): live packet feed, protocol pie chart, traffic timeline, connection table
- Export to JSON for further analysis

## How do you consider the project is success?

1. Correctly dissects all supported protocols — validated against Wireshark output on 10 PCAP files from publicly available captures
2. TCP stream reassembly correctly reconstructs HTTP request/response pairs from a PCAP with interleaved connections
3. DNS dissection handles standard record types (A, AAAA, CNAME, MX, TXT) and response codes
4. Port scan detection triggers alert when >100 SYN packets to different ports from same source within 60 seconds
5. PCAP read/write roundtrip preserves all packet data (byte-identical)
6. Web dashboard displays live traffic with <2 second latency
7. Handles sustained capture at 10,000 packets/sec without dropping packets (on localhost traffic)
8. Test suite with at least 30 tests covering dissection, reassembly, anomaly detection, and PCAP I/O
