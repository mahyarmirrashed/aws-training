# Module 2: Compute in the Cloud

## Introduction

- Multiple disadvantages to purchasing computing resources rather than using cloud-based solutions
  - Researching into type of servers needed for specific application
  - Performing cost-analysis for number of servers needed based on current trends
  - Purchasing equipment upfront (need capital or incur liabilities)
  - Waiting for weeks/months for vendors to deliver on orders
  - Hiring team to install equipment and perform necessary wiring
  - Mitigating resource failures and managing backups
- EC2 only charges for running instances (not stopped or terminated instances)
- Hypervisor employs multitenancy: sharing underlying hardware between virtual machines
  - Managed by AWS to secure EC2 instances between each other
  - EC2 instances and hypervisors are akin to processes and operating systems
- Vertically scaling an instance allows for allocating/deallocating resources to that system (raw scaling)
- AWS makes money through its Compute-as-a-Service (CaaS) model

## Amazon EC2 Instance Types

- Amazon EC2 instance types are optimized for different tasks
  - General purpose provide balanced resources (diverse workloads)
- Compute optimized are excellent for compute intensive tasks (e.g. gaming servers, high-performance computing, scientific modelling)
- Memory optimized instances are excellent for memory-intensive tasks (e.g. databases)
- Accelerated computing excellent for floating-point number calculations, graphics processing, and data-pattern matching (e.g. bioinformatics) using hardware accelerators
- Storage optimized for high-performance of locally-stored data

## Amazon EC2 Pricing

- On-demand payment (only pay for \$/hour or \$/sec)
  - Ideal for getting started (testing workloads and getting baseline performance)
- Savings plans measured in (\$/hour) for 1-year or 3-year term
  - Contract with AWS to use resources constantly for some period of time
- Reserved instances for predictable, steady-state usage (e.g. CRON jobs, RSS publishing)
- Spot instances (spare Amazon EC2 pricing)
  - AWS can reclaim instances whenever they require it
  - Excellent for testing and batch processing that can withstand interruptions
- Dedicated hosts are physical devices for private use (no tenancy)
  - Usually needed for meeting some compliance requirements by regulators

## Scaling Amazon EC2

- Some datacenters reach utilizations of 10% due to fear of peak workloads
- Programmatically setting up EC2 instances allows for redundancy when instances inevitably fail
- Amazon EC2 Auto Scaling provides two options: dynamic scaling and predictive scaling
  - Dynamic scaling responds to changing demand
  - Predictive scaling automatically schedules right number of Amazon EC2 instances based on predicted demand
- Scaling up (vertical): providing more computing resources to instances
- Scaling out (horizontal): increasing numbers of instances running
- When backlogs do not exist, no need to add additional horizontal resources
- Amazon EC2 Auto-Scaling capacities:
  - Minimum capacity: number of EC2 instances to launch immediately after creating Auto Scaling group
  - Desired capacity: defaults to minimum capacity
  - Maximum capacity: although group may scale out in response to increased demand, but only a mazimum of four EC2 instances

## Directing Traffic with Elastic Load Balancing

- Amazon Elastic Load Balancing (ELB) automatically distributes incoming application traffic across multiple resources (e.g. EC2 instances)
  - Helps customers be served in most efficient manner
- Service is automatically highly available and scalable without change to hourly user costs
- When traffic reduces, ELB stops new traffic from arriving to terminating EC2 instances
  - Once requests complete on terminating instances, EC2 auto-scaling engine terminates instances without disruption to existing customers
- ELB also allows for decoupling front-end traffic from back-end traffic (one is not fully aware of the other)

## Messaging and Queuing

- Placing messages on buffer (does not require timed interaction between services)
- Tightly coupled architectures are extremely fault-susceptible
  - One error can degrade an entire system
- Loosely coupled architecture: single failure cannot cause cascading failures
- Amazon Simple Queue Service (SQS) and Amazon Simple Notification Service (SNS) assist in loosely coupling systems
- Payload: message contained within communicated data
- SQS queues: messages are placed until processed by receving application
- SNS topics: channel for messages to be delivered within Publisher-Subscriber model
- Monolithic applications are tightly coupled (single component failure can cause entire system to fail)
- Microservices approach to applications helps maintain application availability
  - Applications are loosely couple and prevent entire application from failing

## Additional Compute Services

- Serverless: cannot see or access underlying infrastructure
  - Management of underlying environment are taken care of by AWS
- Container orchestration tools: Amazon Elastic Container Service (ECS) or Amazon Elastic Kubernetes Service (EKS)
- Docker containers use operating-system level virtualization of computer resources
  - Acts as code packaging tool (specify dependencies and needed configurations)
  - Containers run on EC2 instances in isolation from each other
- Conatiner orchestration: management of stop, start, restart, and monitoring of containers running across all EC2 instances (clusters)
- Amazon Fargate: serverless compute platform for ECS or EKS
- Choice based on usage:
  - Amazon EC2: host traditional applications and full access to operating system
  - AWS Lambda: short-running functions, service-oriented applications, event-driven applications, no provisioning or managing servers
  - Amazon Fargate: container-based workloads in serverless environment
