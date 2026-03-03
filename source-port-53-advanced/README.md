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
