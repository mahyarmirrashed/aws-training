# Module 9: Migration and Innovation

## AWS Cloud Adoption Framework (CAF)

- AWS Professionals provide advice to company to enable smooth migration
- Perspectives: business, people, governance, platform, security, and operations
  - Uncover gaps between knowledge and individuals
- CAF Action Plan: uses gaps as input guides for organization during cloud migration

## Migration Strategies

- 6 strategies for migration: rehosting, replatforming, refactoring/re-architecting, repurchasing, retaining, retiring
- Rehosting: lift and shift (move as-is on AWS), easy to optimize later
- Replatforming: lift, tinker, and shift (make a few cloud optimizations and no new code)
- Retiring: applications that are no longer being used (end-of-life applications)
- Retaining: applications about to be deprecated (turn off in future, no need to migrate)
- Repurchasing: abandon legacy software vendors (high upfront cost)
- Refactoring: adding new code (dramatic changes to codebase, highest upfront cost)

## AWS Snow Family

- Copying over internet, may take days, weeks, or months (high cost and slow)
- AWS Snowcone: holds about 8 TB of data (for shipping data)
- AWS Snowball Edge: storage-optimized or compute-optimized (simple processing of data on-site)
- AWS Snowmobile: holds about 100 PB for huge database migrations
- All Snow devices are secure and tamper-proof
