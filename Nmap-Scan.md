# Nmap Scans

1. Ping Scan (Host Discovery)
`bash
nmap -sP 192.168.1.0/24
`
Result: Detected 4 active hosts (router, laptop, phone, VM).


2. Service/Version Detection
`bash
nmap -sV 192.168.1.137
`
Result: Port 5357 open, running Microsoft HTTPAPI httpd 2.0.


3. Aggressive Scan
`bash
nmap -A 192.168.1.137
`
Result: OS detected as Windows, detailed service info.


4. Full Port Scan
`bash
nmap -Pn -p- 192.168.1.137
`
Result: Comprehensive port check, confirmed only 5357 open.


5. No Ping Scan
`bash
nmap -Pn 192.168.1.117
`
Result: VM host up, but no services exposed.


6. Vulnerability Script Scan
`bash
nmap --script vuln 192.168.1.137
`
Result: Checked for known CVEs on exposed services.
`
