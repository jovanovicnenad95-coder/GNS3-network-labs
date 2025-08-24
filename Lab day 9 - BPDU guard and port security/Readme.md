I configured sticky MAC learning and set different violation modes (protect on SW1 and shutdown on SW2).

When I replaced PC1 with a rogue PC on SW1, the port did not go down, but the new MAC was not learned and traffic was silently dropped (protect mode). On SW2, the same action caused the port to shut down (shutdown mode).

I also tested with a rogue switch connected to SW2. The port was shut down immediately because the sticky MAC address did not match. After disabling port security, BPDU Guard kicked in and also shut down the port when BPDUs were received.

On SW1 the port recovered automatically when the original PC was reconnected, while on SW2 I had to manually shut/no shut the interface to bring it back up after a violation.

This lab clearly demonstrated the differences between violation modes (protect vs shutdown) and how BPDU Guard complements port security to prevent rogue switches.