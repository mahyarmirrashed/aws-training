# Module 4: Networking

## Introduction

- Amazon Virtual Private Cloud (VPC): allows provisioning of logically isolated resources
- Public vs. private subsets for isolated regions or resources

## Connectivity to AWS

- VPC: private IP range for AWS resources
- Subnets: chunk of IP resources to group resources together
  - Control visibility to outside world
- Attach internet gateway to expose VPC to internet traffic
- Virtual private gateway (VPN connection from authorized sources)
  - Still uses shared internet (and shared bandwidth)
- AWS direct link creates private fiber connection from personal data center to AWS
  - Physical line connecting private network directly to VPC
  - Allows mitigating regulatory restrictions and bandwidth issues

## Subnets and Network Access Control Lists

- Only practical use for subnets is to control access to gateways
- Network Access Control List (Network ACL): passport control officers for subnets
  - Acts on incoming and outgoing packets
- Security groups: block within subnet boundaries
- EC2 instances, by default, block all IP addresses from all ports
  - Explicitly allow certain types of messages
  - Only checks incoming traffic, not outgoing (by default)
- Security groups are stateful: remember who to let in/out
- Network ACLs are stateless: checks every packet crossing border

## Global Networking

- Amazon Route 53 allows users to map website addresses to nearest edge locations to them (with option for different routing policies)
- Ability to buy domains through Route 53
