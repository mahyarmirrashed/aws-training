# Module 5: AWS CDK Development

## Working with the AWS CDK

- AWS CDK Explorer: provides tree representation of CDK stacks and resources defined in CDK constructs
- View multiple folders simulatenously in VSCode editor

## Power of the AWS CDK

- Using higher-level constructs, able to avoid annoying things like CIDR (Classless Inter-Domain Routing) blocks

## Testing Constructs

- As of writing, TypeScript is only supported language for testing AWS CDK infrastructure (e.g. using JEST)
  - Able to configure snapshot testing

## Designing Best Practices

- Best practices: effective, consistent, and repeatable approach to using AWS CDK
- Testing: treat test code like application code
  - Do not assert too much in single test (single responsibility tests)
  - Test names should indicate exactly what is broken
  - Perform validation as soon as possible and raise exceptions as early as possible
- Tagging: tag stacks (CDK applies tags recursively throughout stack)
- Constructs: high-level constructs can be excessive for small projects
- Patterns: enforce software design patterns with defaults and organizational policies during construct development
- Deployments: include output of `cdk diff` in code reviews
  - Deploy AWS CDK changes through CI/CD pipeline
- Limitations: high-level constructs only support some of options of the AWS CloudFormation resource they modify (add property override or use low-level construct directly)
- AWS CDK follows Shared Responsibility Model
  - Understand how certain constructs that you use affect your applications
  - AWS Construct library offers a few features for managing access and permissions (IAM Construct library for tools needed)
