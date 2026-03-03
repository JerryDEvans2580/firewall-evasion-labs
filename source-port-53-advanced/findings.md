# Findings

The firewall was configured to allow traffic based solely on source port number.

Likely Rule:

ALLOW inbound IF source port = 53
DENY other traffic

This represents stateless filtering and improper trust assumptions.
