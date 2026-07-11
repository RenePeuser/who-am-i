# Siemens

**Period:** 2020–present  
**Positioning:** Principal backend / platform engineer and technical consultant

> This page intentionally stays at a public, non-confidential abstraction level.

## Mission

Design and evolve reusable backend foundations for a large enterprise cloud and AI ecosystem.

## Areas of responsibility

- Architecture and implementation of reusable ASP.NET Core and Minimal API SDKs
- Metadata-driven capability modeling
- Multi-provider abstractions across AWS, Azure, GCP, OpenAI, Snowflake, Fabric, and internal platforms
- OpenAPI generation and schema transformation
- Validation engines and reusable validation rules
- Test infrastructure and integration-testing SDKs
- Error-handling and Problem Details infrastructure
- Deployment lifecycle modeling and orchestration integration
- Performance, reflection, startup, and build optimization
- Pair programming, code reviews, documentation, and technical enablement

## Selected engineering outcomes

### Large Minimal API ecosystem

Contributed to a platform with hundreds of endpoints and a broad capability model. The engineering challenge is not simply endpoint implementation; it is maintaining consistency across contracts, validation, schemas, provider behavior, lifecycle operations, testing, and generated clients.

### Capability meta-framework

Designed and evolved a framework in which capability types can be represented through metadata and conventions. This makes it possible to introduce new capability families without rebuilding every infrastructural concern independently.

### OpenAPI and request polymorphism

Implemented and refined OpenAPI support for typed create requests, discriminators, `oneOf` schemas, provider mappings, duplicate prevention, and self-reference handling.

### Validation platform

Built and expanded reusable rules for strings, collections, identifiers, property relationships, conditional requirements, numeric limits, and domain-specific constraints. Work includes aligning rule vocabularies across infrastructure and backend repositories.

### Testing platform

Developed abstractions for API integration testing, response assertions, schemas, snapshots, content types, status codes, request samples, and reusable test clients.

### Cloud and deployment model

Worked on capability and deployment behavior spanning AWS, Azure, GCP, Snowflake, Fabric, OpenAI, and internal platforms. Relevant services include AWS Lambda, DynamoDB, Cognito, API Gateway, Step Functions, SSM Parameter Store, and cloud-specific AI services.

## Engineering style

I combine implementation with architecture enablement:

- design the reusable core;
- provide strong examples and tests;
- remove accidental complexity;
- coach teams through reviews and pair programming;
- encode conventions in executable tooling.
