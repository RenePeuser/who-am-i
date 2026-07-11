# Error handling

## Objective

Provide consistent, structured, observable error contracts across services.

## Core concepts

- RFC 7807 / Problem Details responses
- Central exception mapping
- Consistent status-code selection
- Correlation and contextual metadata
- Logging integration
- Sanitized client-facing details
- Extensible domain-specific problem information
- Testable error behavior

## Public package

[`Siemens.AspNet.ErrorHandling`](https://www.nuget.org/packages/Siemens.AspNet.ErrorHandling/7.6.0-alpha.61) documents the use of RFC 7807 to provide consistent and interpretable error responses.

## Architectural benefit

Centralized error handling separates endpoint code from protocol mechanics and ensures that observability, client contracts, and security rules evolve consistently.
