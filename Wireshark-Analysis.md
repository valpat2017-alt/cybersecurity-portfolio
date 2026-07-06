# Wireshark Practice Report – July 2026

## Objective
To practice protocol filtering and DNS analysis using Wireshark in a controlled lab environment.

## Filters Applied
- `ip.addr == <target_IP>` → Isolated traffic to/from specific hosts.
- `udp` → Observed lightweight transport traffic (DNS, DHCP).
- `tcp` → Analyzed reliable transport traffic, focusing on SYN/ACK patterns.
- `dns` → Captured domain resolution queries and responses.

## Key Findings
- **Request vs Response:** Learned to distinguish client queries from server replies.
- **DNS Records:** 
  - A record → IPv4 resolution.
  - AAAA record → IPv6 resolution.
- **Ping Test:** Pinging `google.com` triggered DNS queries, which resolved successfully and were visible in Wireshark.

## Blue Team Insights
- Protocol filters allow precise traffic isolation.
- DNS analysis reveals how devices resolve domains — critical for detecting suspicious lookups.
- Understanding request/response flow helps identify anomalies and brute‑force attempts.

## Next Steps
- Expand into HTTP/HTTPS traffic analysis.
- Simulate brute‑force attempts and detect them in Wireshark.
- Document findings in SOC‑style incident reports for portfolio growth.
