# Day 2 – Setting Up the Network Topology

## Overview
This lab focused on building a small local network topology using routers, switches, and PCs. The objective was to connect multiple devices, assign IP addresses, and verify connectivity.

## Objectives
- Build physical and logical topology connections.
- Configure switch and router interfaces.
- Assign IP addresses to PCs.
- Test end-to-end connectivity using `ping`.

## Steps Overview
1. Connect router, switch, and PCs using proper cabling.
2. Configure IP addresses on interfaces.
3. Assign default gateway on PCs.
4. Verify connections and test communication.

## Key Commands
```bash
interface g0/1
ip address 192.168.1.1 255.255.255.0
no shutdown

interface g0/2
ip address 192.168.2.1 255.255.255.0
no shutdown

show ip interface brief
ping 192.168.2.2
````

## Verification

* Use `show ip interface brief` to ensure interfaces are up.
* Ping between PCs across the switch to confirm reachability.
* Verify that default gateways are properly configured.

## Outcome

A fully operational local network with successful device interconnectivity. Learned IP addressing, interface configuration, and connectivity troubleshooting.

## Notes

* Ensure cables are properly connected and interfaces are not administratively down.
* Document all IP addressing schemes for troubleshooting.
