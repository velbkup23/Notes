# Notes

In place upgrade of Pooled session host is not supported but upgrade of Single session hosts are allowed. In place upgrade of Client OS can be done from Windows updates or by downloading the disk and upgrading in Hyper-V. Upgrade of server OS can be done by using an upgrade image from Azure Marketplace.

A maximum of 200 session hosts can be created in an availability set. Availability set can have a maximum of 3 fault domains and 20 update domains.

AVD metadata is a non-regional resource, it's replicated to the replica region within the geography. Service will be affected during the fail over.

Ephemeral Disks are not supported directly in AVD but through Nerdio. They are good for Random read/write operations in comparison to standard SSD, in regards to IOPS and latency.

Total number of vCPUs in an azure region?

A Host pool type cannot be changed from Personal to Pooled or vice-versa

Networking:
- After changing the Private endpoint in a host pool, RDAgent bootloader service must be restarted in the Session hosts for it to take effect. This service restart or session host restart will be needed after reconfiguring hostpool's network configuration.
- Using Private link and RDP shortpath for managed network is in preview; all other RDP shortpath options using STUN or TURN are not supported with Private link.
- 





 



