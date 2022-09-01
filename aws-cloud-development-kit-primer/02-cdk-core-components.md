# Module 2: AWS CDK Core Components

## What are Constructs?

- Construct represents single cloud resource or higher-level resource of multiple cloud resources
- CDKs use compositions to define complex constructs
  - Define constructs inside scopes of other constructs
- Construct tree: hierarchy of constructs through scoping pattern
- CDK application: root of construct tree
  - Typically consists of one or more stacks (actual unit of deployment)
- Constructs are implemented in classes extending `Construct` base class
  - Define construct by instantiating class (or extension)
  - All constructs take scope, identification strings, and properties
- Scope: construct in which current construct is created
  - Usually define construct in its own scope (e.g. pass `this` or `self`)
- ID: local identifier of construct that must be unique within scope
  - CDK uses identifier to calculate AWS CloudFormation logical ID for each resource defined within scope (e.g. `vpc-UUIDv4`)
- Props: set of initialization properties specific to construct and initial configuration (read through documentation)
- Build own constructs for: organizing project, streamlining deployment processes, packaging constructs into modules

## Using Predefined Constructs for AWS Resources

- CDK libraries have three levels of constructs: CDK pattern constructs (opinionated), resource constructs (high-level), and CloudFormation resource constructs (low-level)
- L3 Pattern Constructs: designed to complete common tasks using various resources
  - Best-practice patterns by default (from cloud provider)
- L2 Resource Constructs: represents resources, offers convenient defaults, and reduces need to know details about represented resources
- L1 Cloud-level Resources: directly represent cloud resources available (with all applicable configurations)

## Apps and Stacks

- CDK worflow includes few extra steps to synthesizing stack templates and deployments
  1. Create application from template (optional)
  2. Add code to application to create resources within stack
  3. Synthesize one or more stacks within application to create template
  4. Deploy one or more stacks to cloud account
- Typically define application instance in program entry point, then define constructs where application is used as parent scope
- Bypass infrastructure resource limit using nested stacks
  - Nested stacks can contain 200 resources while only counted as single resource within parent stack
  - During application synthesis, each nested stack is treated as its own template
  - Nested stacks are not treated as independent deployments and cannot be individually deployed or listed
- 
