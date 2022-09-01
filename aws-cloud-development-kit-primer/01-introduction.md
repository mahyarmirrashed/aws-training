# Module 1: AWS Cloud Development Kit Introduction

## What is AWS CDK?

- Allows provisioning cloud infrastructure resources through command line tools
- CDK: compiler for turning source code into AWS CloudFormation template
  - Three main components: App, Stack, and Construct
- AWS CloudFormation templates: create cloud infrastructure
- Construct: basic building blocks for CDK applications
  - Represents cloud component and encapsulates everything CloudFormation needs to create the component
  - Construct can be fundamental resource or a higher-level component consisting of multiple AWS CDK resources
- Stacks: unit of deployment
  - All resources defined within scope of stack—either directly or indirectly
- Applications: CDK application represented by AWS CDK App class

## Importance of AWS CDK for Your Organization

- Design reusable components that reach security, compliance, and governance requirements
- Shareable across organization (standardization of defined components)

## Advantages of using AWS CDK

- Achieve faster deployment by using expressive programming languages for infrastructure definement
- Incorporating features such as objects, loops, and conditionals
- Writing runtime code and defining AWS resources with same programming languages
- Organizing project into logical modules/components
- Test infrastructure using open-standard protocols and code review workflows

## AWS CDK Interaction with Programming Languages

- [AWS JSii](https://github.com/aws/jsii) to provide mapping to each supported programming language
