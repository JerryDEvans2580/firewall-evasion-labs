# IDS/IPS Misconfiguration via Source Port 53

## Summary

A hidden service on port 50000 was initially filtered by firewall rules.
By manipulating the source port to 53 (DNS), the filtering mechanism was bypassed.

## Key Finding

Firewall trusted traffic originating from source port 53.
This allowed access to otherwise filtered internal services.

---

## Impact

- Bypass of network segmentation
- Exposure of hidden services
- Potential lateral movement vector

## Attack Flow

1. Port 50000 appeared filtered.
2. Hypothesis: Firewall filtering in place.
3. Tested source-port manipulation using 53.
4. Port state changed to OPEN.
5. Confirmed firewall trust misconfiguration.
