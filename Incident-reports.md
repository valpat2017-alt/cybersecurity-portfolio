# SOC Incident Report – Telnet Brute‑Force Attempt

## Summary
A brute‑force login attempt was detected against the Telnet service running on Metasploitable2. The attack originated from the Kali Linux VM and was identified through repeated authentication failures in system logs.

---

## Incident Details
- **Source IP:** 192.168.56.102 (Kali)
- **Target Service:** Telnet (port 23)
- **Attack Method:** Brute‑force login attempts using Hydra
- **Evidence:** `/var/log/auth.log` and `/var/log/syslog` entries showing repeated failed login attempts
- **Action Taken:** Attacker IP blocked via firewall rule (`iptables`)

---

## Log Evidence (Excerpt)

pam_unix(login:auth): authentication failure FAILED LOGIN (1) FROM 192.168.56.102 FOR msfadmin
