Today I worked on implementing SVIs (Switch Virtual Interfaces) on Cisco IOSvL2 switches and enabling Layer 3 routing.

At first, the PCs in different VLANs could not ping each other. The issue was that I didn’t enable ip routing on the switch — by default, the IOSvL2 image only forwards within VLANs. Once I activated routing, the switch started behaving like a Layer 3 switch, and inter-VLAN communication worked correctly.

Verification was done by:

Pinging between hosts in different VLANs (successful).

Checking the routing table on the switch to confirm directly connected VLAN networks were installed.

In summary, enabling ip routing was the key step that allowed the switch to route traffic between VLANs, completing the lab successfully.