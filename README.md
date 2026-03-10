<img width="1855" height="728" alt="MPLS" src="https://github.com/user-attachments/assets/ad08162e-038c-4761-b046-c4288e534bef" />

# MPLS L3VPN Lab – Headquarters to Branch Connectivity

## Project Overview

This project demonstrates a complete **MPLS Layer 3 VPN deployment** connecting a Headquarters network with a remote Branch through a simulated Service Provider MPLS backbone.

The lab was built from scratch using **Cisco IOS XRv 6.1.3 routers** and simulates how real Internet Service Providers deliver private connectivity between enterprise sites using **MPLS and MP-BGP**.

This project highlights core **Service Provider technologies used in real-world ISP environments.**

## Network Architecture

The topology consists of:

Customer Edge (CE)
Provider Edge (PE)
Provider Core (P)

The MPLS Service Provider cloud runs:

• OSPF as the IGP  
• LDP for label distribution  
• MP-BGP for VPN route exchange

Customer routing is handled using **VRF separation on PE routers**.

## Technologies Implemented

• MPLS Label Switching  
• LDP (Label Distribution Protocol)  
• MP-BGP VPNv4  
• VRF (Virtual Routing and Forwarding)  
• OSPF Area 0 (Provider Core)  
• Loopback based Router-ID design  
• End-to-End Site Connectivity Verification  

## Lab Topology

Headquarters CE ----- PE ----- P ----- PE1 ----- Branch CE

The service provider backbone transports traffic using **MPLS labels instead of traditional IP routing**.

## Devices Used

| Device | Role |
|------|------|
|HQ | Customer Edge Router (Headquarters) |
| PE | Provider Edge Router |
| P | MPLS Core Router |
| PE1 | Provider Edge Router |
| BR | Customer Edge Router (Branch) |

All service provider routers run:
Cisco IOS XRv 6.1.3

## Key Learning Objectives

This lab demonstrates how service providers:

• Build scalable MPLS backbones  
• Deliver Layer 3 VPN services to customers  
• Separate customer routing tables using VRFs  
• Use MP-BGP to exchange VPN routes  
• Forward packets using MPLS labels across the core network  

## MPLS Service Provider Design

Provider Core Protocols

IGP: OSPF Area 0  
Label Protocol: LDP  
VPN Control Plane: MP-BGP  

Customer routing between CE and PE routers uses standard IP routing.

## Verification Commands

Verify MPLS forwarding table

show mpls forwarding

Verify LDP neighbors

show mpls ldp neighbor

Verify BGP VPN routes

show bgp vpnv4 unicast all

Verify VRF routing table

show route vrf <VRF-NAME>

Verify end-to-end connectivity

ping
traceroute

## End-to-End Connectivity Test

Successful ping between:

Headquarters Loopback → Branch Loopback

This confirms that MPLS labels correctly transport VPN traffic through the provider network.

## Skills Demonstrated

Service Provider Networking  
MPLS Architecture  
Cisco IOS XR Configuration  
Routing Protocol Design  
Network Troubleshooting  
Enterprise WAN Connectivity  

## Lab Environment

Simulation Platform: GNS3 / EVE-NG  
Router Image: Cisco IOS XRv 6.1.3


## Author

Engineer Rogers Mulyowa 

