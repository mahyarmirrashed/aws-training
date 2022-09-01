# AWS CDK Concepts

## Identifiers

- Few types of identifiers: construct IDs, paths, unique IDs, logical IDs
- Construct IDs: most common identifier (passed as argument when instantiating constructs)
- Paths: hierarchy rooted in application class by constructs
  - Refers to collection of IDs from a given construct, its parent construct, its grandparent construct, so on until root of construct tree
  - CDK displays paths within templates as string (IDs from each level separated by slashes)
- Uniqueness ensures hashes generated to form logical IDs are also unique
- Unique IDs: CDK requires all identifiers within templates to be unique
  - CDKs usually generate unique identifier for each construct within application (eight-character hash)
- Logical IDs/names: unique IDs serving as logical identifiers of resources within generated templates
  - Changing construct ID within construct tree causes replacement of a deployed resource instances of construct (potentially causing service interruption or data loss)
  - Avoid changing logical ID of resource between deployments

## Environments

- CDK selects default Region using account within current CLI profile
  - Ability to manually environment by specifying different set of default values also exists

## Contexts

- Contexts: key-value pairs associated with stacks or constructs
- CDK uses context to cache information from cloud provider account (e.g. Availability Zones or Amazon Machine Image IDs to start instances)
- Custom created context values should be scoped to construct that created them (visible to child constructs but not siblings)
- Application layer provides methods to retrieve contexts
  - Unavailable contexts are resolved by CDKs CLI to fetch information

## Assets

- Assets: local files, directories, or Docker images that can be bundled into CDK libraries and applications
  - e.g. Directory containing handler code for an AWS Lambda function
- Synthesized applications include metadata information with instructions to CDK on where to find asset(s) on local disk
  - CDK generates source hash for assets (can be used to determine whether asset contents have changed)
  - By default, CDK duplicates asset into project output directory
- Images built from local Docker context directory using a `Dockerfile`
  - At build time, CDK builds and pushes Docker image to an equivalent of an Amazon ECR repository
