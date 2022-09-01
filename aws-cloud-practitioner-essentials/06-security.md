# Module 6: Security

## Shared Responsibility Model

- Both AWS and customers are responsible for maintaining the security of resources
- AWS is responsible for security "of" the cloud
- Customer is responsible for security "in" the cloud

## User Permissions and Access

- Root user: creator of AWS account
  - Permission to do everything (dangerous role)
  - Best to secure with MFA (Multi-Factor Authentication)
- AWS IAM (Identity and Access Management): granular control over user roles and permissions
  - Associate IAM policy to users (JSON document)
- Least privilege principle: grant user access only to what they need
- IAM groups: attach policy to group
  - Users placed in group inherit group privileges
- AWS IAM roles: assumed for temporary amounts of time
  - No username or password for access to temporary permissions
  - Identity that acquires role only is locked down to allow/deny listed within role's policy
- Best practice: create individual IAM users for each person needing access to AWS

## AWS Organizations

- AWS organizations: central location for managing AWS accounts
- Consolidated billing for all member accounts (bulk discounts)
- Hierarchical groupings of accounts: creating OUs (Organizational Units)
- Service control policies: place restrictions on AWS services, resources, and API actions each account can maximally access

## Compliance

- AWS has already implemented some best practices and policies
  - Already complies with long list of compliance programs
- AWS provides white papers and documentation proving following best practices
- AWS Artifact provides access to on-demand compliance reports and agreements made between customers and AWS

## Denial-of-Service Attacks

- AWS already provides some basic security measures to mitigate DDoS attacks
- Common types of attacks: UDP flood, HTTP-level attack, Slowroris attacks
- AWS Shield and AWS WAF: use machine-learning to proactively protect against attacks

## Additional Security Services

- AWS KMS (Key Management Service): encrypt DynamoDB tables
- Amazon Inspector provides diagnostic data of security best practices employed within AWS organizations
- Amazon GuardDuty continuously analyzes network and account activities to intelligently detect threats
