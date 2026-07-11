# Enterprise Minimal API platform

## Objective

Provide a production-ready foundation for large ASP.NET Core Minimal API systems.

## Platform capabilities

- Endpoint and contract conventions
- API versioning
- OpenAPI document and schema transformation
- Authentication and authorization integration
- Validation dispatch and reusable rules
- Error handling and Problem Details
- Request/response samples
- Health checks and diagnostics
- Logging and observability integration
- Test-host and client integration
- Cloud hosting support, including AWS Lambda scenarios

## Why a platform?

Minimal APIs deliberately expose a small programming model. Enterprise systems still need strong conventions and reusable infrastructure.

Without a platform, each endpoint or service can make different decisions about:

- route design;
- validation;
- status codes;
- error contracts;
- versioning;
- schema generation;
- logging;
- testing.

The platform turns those decisions into a consistent engineering system.

## Scale

The current work supports a broad platform with roughly 450 endpoints and multiple cloud providers. The challenge is sustained consistency, not merely endpoint count.

## Public package

[`Siemens.AspNet.MinimalApi.Sdk`](https://www.nuget.org/packages/Siemens.AspNet.MinimalApi.Sdk/) exposes part of this engineering direction publicly through NuGet.
