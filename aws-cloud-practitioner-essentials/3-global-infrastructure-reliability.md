# Module 3: Global Infrastructure and Reliability

## Introduction

- AWS resources are high availability and fault tolerant (located around the globe)
- Customers are always\* able to run their AWS services

## AWS Global Infrastructure

- AWS connects data centers with high-speed transatlantic fiber optic cables
- AWS regions are isolated within regions (without explicit permission)
  - Allows compliance with regional regulations
- Proximity (speed of light restrictions)
  - Low proximity results in high latency for users
  - If most users are Canadian, locate data centers in Canada or United States
- Feature availability (some regions receive new features first in rollout phasing)
- Some locations are more expensive for AWS to operate than other countries
- AWS labels regions as an Availability Zones
  - Multiple Availability Zones can exist into same region
  - Pro tip: run across at least two Availability Zones in a Region

## Edge Locations

- Cache copies of data within other AWS data centers
  - Create personal Content Delivery Network (CDN)
- AWS CDN: Amazon Cloudfront (deliver applications, APIs, videos) with low latency and high transfer speeds
- Amazon uses Edge Locations to speed up access from customers globally
- Route 53: AWS' DNS service for accessing data centers
- AWS Outposts: use AWS within personal data centers (for compliance with some privacy regulations)

## Provisioning AWS Resources

- Multiple methods of interacting with AWS resources
  - AWS management console: browser-based and visual (easy to digest, getting started, testing environments, view AWS bills, etc.)
  - AWS CLI: make API calls through terminal
  - AWS SDKs: interact with AWS through various programming languages
- AWS Elastic Beanstalk: tool to help provision EC2 instances, balancers, and auto-scaling (helps save configurations)
  - Focus on business application, not infrastructure
- AWS CloudFormation: infrastructure as code tool to define wide variety of AWS resources
