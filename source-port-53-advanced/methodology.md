# Methodology

## 1. Initial Scan

nmap target -sS -Pn -n --disable-arp-ping --source-port 53 -v

Result:

22/tcp    open  ssh

80/tcp    open  http

50000/    tcp   filtered

---

## 2. Source Port Manipulation Test

nmap <targetIp> -p50000 -sS -Pn -n --disable-arp-ping --source-port 53 -v

Result:
50000/tcp open


## Evidence

Initial scan result:

50000/tcp filtered

Bypass scan result:

50000/tcp open

---

## 3. Establishing Connection

ncat -nv --source-port 53 <targetIp> 50000

Result:
Connection established
