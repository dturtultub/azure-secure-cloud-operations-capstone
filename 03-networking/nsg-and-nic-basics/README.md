# Azure NSG + NIC Network Foundation

## Goal

Build a low-cost Azure networking foundation using a virtual network, subnet, Network Security Group, custom inbound rules, and private network interfaces.

## Why this matters

Cloud administrators need to understand how Azure resources connect to private networks and how network traffic is filtered before deploying virtual machines or applications.

This lab demonstrates subnet-level network security, private IP assignment, and the relationship between virtual networks, subnets, network interfaces, and Network Security Groups.

## Skills demonstrated

- Virtual network creation
- Subnet design
- Network Security Group creation
- Subnet-level NSG association
- Custom inbound security rules
- Private network interface creation
- Private IP assignment
- Low-cost network foundation design
- Least-exposure network security basics

## Resources used

- Resource group: `rg-cloudops-network-dev`
- Virtual network: `vnet-cloudops-dev`
- Address space: `10.20.0.0/16`
- Subnet: `subnet-app`
- Subnet range: `10.20.1.0/24`
- Network Security Group: `nsg-cloudops-app-dev`
- Network interfaces:
  - `nic-cloudops-app-01`
  - `nic-cloudops-app-02`

## Evidence

| Screenshot | What it proves |
|---|---|
| `screenshots/01-resource-group-tags.png` | Created a dedicated networking resource group with standardized governance tags. |
| `screenshots/02-vnet-subnets-created.png` | Created a virtual network and application subnet using private IP addressing. |
| `screenshots/03-nsg-overview.png` | Created a dedicated Network Security Group for the application subnet. |
| `screenshots/04-nsg-associated-to-subnet.png` | Associated the NSG to `subnet-app` from the NSG side. |
| `screenshots/05-subnet-now-protected-by-nsg.png` | Verified from the VNet subnet view that `subnet-app` is protected by the NSG. |
| `screenshots/06-nsg-custom-inbound-rules.png` | Added custom inbound rules to deny direct SSH/RDP from the Internet and allow internal HTTPS traffic. |
| `screenshots/07-private-nics-created.png` | Created two private network interfaces in the subnet without public IP addresses. |

## Custom inbound security rules

| Priority | Rule | Port | Source | Destination | Action |
|---:|---|---:|---|---|---|
| 100 | `Deny-SSH-Internet` | 22 | Internet | Any | Deny |
| 110 | `Deny-RDP-Internet` | 3389 | Internet | Any | Deny |
| 200 | `Allow-HTTPS-VNet` | 443 | VirtualNetwork | VirtualNetwork | Allow |

## Key design decision

The NSG was associated at the subnet level instead of separately attaching a security group to each network interface.

This design is simpler and easier to manage when multiple resources in the same subnet need identical security rules.

## Real-world explanation

In a real cloud environment, administrators often group related application resources into a subnet and apply shared security rules at the subnet level.

This reduces duplicated configuration and helps enforce consistent network access rules across multiple resources.

## What this proves

This lab proves the ability to:

- Build a basic Azure network foundation
- Segment a VNet using a subnet
- Apply a Network Security Group to a subnet
- Configure custom inbound security rules
- Create private network interfaces
- Explain how one subnet-level NSG can protect multiple resources
- Avoid unnecessary public exposure by not creating public IPs

## Resume bullet

Built a secure Azure network foundation using a VNet, application subnet, subnet-level Network Security Group, custom inbound rules, and private NICs to demonstrate least-exposure network access design.

## Interview explanation

I built a low-cost Azure network foundation with a virtual network, application subnet, and subnet-level Network Security Group. I added custom inbound rules to deny direct SSH and RDP from the Internet while allowing internal HTTPS traffic inside the virtual network. I also created private NICs in the subnet to show how multiple resources can share one subnet-level NSG when they need the same rules.

## Common mistake

A common mistake is assuming each virtual machine needs its own Network Security Group.

If multiple resources are in the same subnet and require identical rules, one subnet-level NSG can be enough.

Another common mistake is assuming that a public IP and private IP require two NICs. A single NIC can have a private IP and can optionally be associated with a public IP.