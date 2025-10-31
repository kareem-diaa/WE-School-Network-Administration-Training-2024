# Day 3 – VLAN, EtherChannel, and OSPF Configuration

## Overview
This lab implemented advanced switching and routing concepts including VLAN segmentation, link aggregation with EtherChannel, and OSPF routing between routers.

## Objectives
- Create and assign VLANs to specific ports.
- Configure EtherChannel using LACP.
- Establish OSPF routing for dynamic network discovery.
- Test communication across VLANs and routers.

## Steps Overview
1. Create VLANs and assign access ports.
2. Configure trunk links and EtherChannel.
3. Enable OSPF and assign router IDs.
4. Verify connectivity across the network.

## Key Commands
```bash
vlan 10
name HR
interface range f0/1 - 4
switchport mode access
switchport access vlan 10

interface range g0/1 - 2
channel-group 1 mode active
interface port-channel 1
switchport mode trunk

router ospf 1
network 192.168.1.0 0.0.0.255 area 0
show ip ospf neighbor
````

## Verification

* Use `show vlan brief` to verify VLAN assignments.
* Use `show etherchannel summary` to confirm bundle status.
* Run `show ip route` to confirm OSPF learned routes.
* Ping across VLANs to ensure routing works.

## Outcome

VLANs successfully isolated traffic, EtherChannel increased bandwidth and redundancy, and OSPF provided dynamic routing between routers. This completed a scalable, efficient Layer 2/3 network.

## Notes

* Always match EtherChannel mode on both ends.
* Use unique router IDs for OSPF neighbors.
* Save configuration after verifying functionality.
