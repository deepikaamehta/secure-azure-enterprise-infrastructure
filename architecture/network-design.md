# Nexora Technologies — Azure Network Design

## 1. Overview

Nexora Technologies will use a hub-and-spoke network architecture in Microsoft Azure.

The architecture separates production and development workloads while providing a central location for shared networking services.

## 2. Azure Region

Primary region: Canada Central

## 3. Virtual Network Address Plan

| Virtual Network | Address Space | Purpose |
|---|---|---|
| vnet-nexora-hub | 10.0.0.0/16 | Shared network services |
| vnet-nexora-prod | 10.1.0.0/16 | Production workloads |
| vnet-nexora-dev | 10.2.0.0/16 | Development workloads |

All three address spaces are non-overlapping.

## 4. Proposed Subnet Design

| VNet | Subnet | CIDR | Purpose |
|---|---|---|---|
| Hub | AzureBastionSubnet | 10.0.0.0/26 | Azure Bastion, if deployed |
| Hub | snet-shared-services | 10.0.1.0/24 | Shared infrastructure |
| Production | snet-prod-web | 10.1.1.0/24 | Production web workloads |
| Production | snet-prod-app | 10.1.2.0/24 | Production application workloads |
| Development | snet-dev-app | 10.2.1.0/24 | Development workloads |

## 5. Connectivity

- Establish bidirectional VNet peering between the hub and production.
- Establish bidirectional VNet peering between the hub and development.
- Do not configure direct production-to-development peering.
- Do not assume that hub peering automatically enables communication between spokes.
- Evaluate routing and firewall requirements before enabling cross-spoke traffic.

## 6. Security Considerations

- Use Network Security Groups (NSGs) to restrict traffic.
- Apply least-privilege access through Azure RBAC.
- Avoid exposing virtual machine management ports directly to the internet.
- Evaluate Azure Bastion for secure administrative access.
- Separate production and development network resources.

## 7. Cost Considerations

This is a learning environment.

Costly services such as Azure Bastion and Azure Firewall will be evaluated before deployment. The architecture may document these services without keeping them running.

Small virtual machines, limited deployment hours, and cleanup procedures will help control costs.

## 8. Validation Plan

- Verify VNet address spaces do not overlap.
- Confirm hub-to-spoke peering is connected.
- Inspect effective NSG rules.
- Test approved and denied network connections.
- Capture screenshots and document test results.