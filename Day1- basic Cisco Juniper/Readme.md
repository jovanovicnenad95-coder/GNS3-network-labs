Day 1 – Cisco R1 ↔ Juniper R2 Basic Connectivity
Objective: Configure basic IP connectivity between Cisco R1 and Juniper R2.
Actions:
Assigned hostname and IP address to each device interface.
Connected R1 (G0/0) to R2 (ge-0/0/0) with matching subnet.
Issue Encountered: Ping from R1 to R2 failed.
Troubleshooting Steps:
Verified interface status on both devices.
On Juniper R2, added interface to trust zone.
Configured security policy to allow ICMP (ping) in trust zone.
Result: Successful bidirectional ping between devices.