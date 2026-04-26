# Networking Learning Notes

## Core model

Azure VM networking uses:

- Virtual network
- Subnet
- Network interface
- Private IP address
- Optional public IP address
- Network security group

## VNet and subnet

A virtual network is the private network boundary in Azure.

A subnet is a smaller IP range inside the virtual network.

In this lab:

- VNet: `vnet-cloudops-dev`
- VNet address space: `10.20.0.0/16`
- Subnet: `subnet-app`
- Subnet address range: `10.20.1.0/24`

## NIC rule

A virtual machine needs at least one network interface.

A network interface receives a private IP address from the subnet.

A public IP address is optional.

Public IP plus private IP does not mean two NICs.

## NSG rule

A network security group controls inbound and outbound traffic.

An NSG can be associated with:

- A subnet
- A network interface

If several resources in the same subnet need identical security rules, one subnet-level NSG can be enough.

## Rules created

Custom inbound rules:

- `Deny-SSH-Internet`
- `Deny-RDP-Internet`
- `Allow-HTTPS-VNet`

## Key lesson

One subnet-level NSG can apply the same security rules to multiple resources in the subnet.

This is more efficient than creating a separate NSG for every VM when the rules are identical.