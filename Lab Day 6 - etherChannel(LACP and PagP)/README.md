Today I worked on implementing EtherChannel between two Cisco switches.
I configured both LACP and PAgP modes and verified bundling with show etherchannel summary. Two PCs connected on each switch in the same VLAN were able to communicate successfully.

I then simulated a failure by shutting down one physical interface. Traffic continued to flow without interruption thanks to the aggregated port-channel. This demonstrated both redundancy and load balancing capabilities.