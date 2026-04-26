# Validation Steps

## 1. Resource group validation

Created a dedicated networking resource group:

- Resource group: `rg-cloudops-network-dev`

Applied governance tags:

- `Department = IT`
- `Environment = Dev`
- `Owner = DanielTurtultub`
- `CostCenter = CloudOpsLab`
- `Project = azure-secure-cloud-operations-capstone`

Evidence:

- `screenshots/01-resource-group-tags.png`

## 2. Virtual network and subnet validation

Created a virtual network:

- VNet: `vnet-cloudops-dev`
- Address space: `10.20.0.0/16`

Created an application subnet:

- Subnet: `subnet-app`
- Address range: `10.20.1.0/24`

Evidence:

- `screenshots/02-vnet-subnets-created.png`

## 3. Network Security Group validation

Created a Network Security Group:

- NSG: `nsg-cloudops-app-dev`

Evidence:

- `screenshots/03-nsg-overview.png`

## 4. Subnet association validation

Associated the NSG to the subnet:

- NSG: `nsg-cloudops-app-dev`
- VNet: `vnet-cloudops-dev`
- Subnet: `subnet-app`

Evidence:

- `screenshots/04-nsg-associated-to-subnet.png`
- `screenshots/05-subnet-now-protected-by-nsg.png`

## 5. Custom inbound rule validation

Created custom inbound rules:

- `Deny-SSH-Internet`
- `Deny-RDP-Internet`
- `Allow-HTTPS-VNet`

Evidence:

- `screenshots/06-nsg-custom-inbound-rules.png`

## 6. Private NIC validation

Created two private network interfaces:

- `nic-cloudops-app-01`
- `nic-cloudops-app-02`

Both NICs were created in:

- VNet: `vnet-cloudops-dev`
- Subnet: `subnet-app`

Both NICs received private IP addresses from the subnet.

Evidence:

- `screenshots/07-private-nics-created.png`

## Result

The lab successfully validated a low-cost Azure network foundation using a VNet, subnet, subnet-level NSG, custom inbound rules, and private NICs.