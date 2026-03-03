# Methodology

## 1. Initial Scan

nmap p50000 -sS -Pn - -n -v <target>

Result:
50000/tcp filtered

---

## 2. Source Port Manipulation Test

nmap -p50000 -sS -Pn -n --source-port 53 -v <target>

Result:
50000/tcp open

---

## 3. Establishing Connection

ncat -nv --source-port 53 <target> 50000

Result:
Connection established
