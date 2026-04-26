# Cost Cleanup

## Cost risk

Low.

This lab avoided high-cost networking and compute resources.

## Resources created

- Resource group:
  - `rg-cloudops-network-dev`

- Virtual network:
  - `vnet-cloudops-dev`

- Subnet:
  - `subnet-app`

- Network Security Group:
  - `nsg-cloudops-app-dev`

- Network interfaces:
  - `nic-cloudops-app-01`
  - `nic-cloudops-app-02`

## Resources intentionally not created

To keep cost low, this lab did not create:

- Virtual machines
- Public IP addresses
- NAT Gateway
- Azure Bastion
- VPN Gateway
- Load Balancer
- Application Gateway

## Cleanup option

When the lab is fully documented and no longer needed, delete the resource group:

`rg-cloudops-network-dev`

This removes the VNet, subnet, NSG, and NICs together.

## Important note

Do not delete the resource group until all screenshots and documentation are saved.