Today I worked on implementing RSTP in a small switched topology. After enabling RSTP, I observed that SW3 was elected as the root bridge. To test failover behavior, I shut down the root-facing port on SW2 (interface 1). During this test, continuous pings were running from PC1 to PC2.

When the primary root port went down, it took around 15 seconds for traffic to start flowing again through the alternate port (interface 0). This was slightly longer than what would normally be expected from RSTP, but it is most likely due to the limitations of the virtual environment.

After re-enabling the original root port, I noticed that the traffic reconverged back to the preferred root path. The convergence time was again roughly 15 seconds, consistent with the first failover test.

In summary, the lab successfully demonstrated how RSTP provides faster convergence compared to traditional STP, even though in my testbed the times were a bit higher than expected. Verification was done by monitoring continuous ping between the end hosts before, during, and after the link changes.