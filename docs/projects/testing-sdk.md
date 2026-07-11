# AspNetCore.Simple.MsTest.Sdk

## Purpose

`AspNetCore.Simple.MsTest.Sdk` reduces boilerplate in ASP.NET Core API tests and makes request/response regression tests readable, repeatable, and maintainable.

[View on NuGet](https://www.nuget.org/packages/AspNetCore.Simple.MsTest.Sdk)

## Core capabilities

- ASP.NET Core integration-test hosting
- HTTP request helpers
- Expected status-code validation
- JSON response comparison
- Snapshot and approval-style testing
- Schema validation
- Content-type assertions
- Response-type assertions
- Reusable request and response files
- Filtering and tooling for large endpoint suites
- Structured assertion output designed to be understandable by humans and automation

## Design goal

A test should communicate the scenario, input, expected response, and expected protocol behavior without pages of setup code.

```csharp
await Client.AssertPostAsync<CreateRequest>(
    "/api/v1/capabilities",
    "Requests/Create.json",
    "Responses/Create.json",
    expectedStatusCode: HttpStatusCode.Created);
```

## Why build a custom SDK?

Large API suites repeat the same mechanics:

1. construct a test host;
2. create an HTTP request;
3. load test data;
4. send the request;
5. validate the status code;
6. normalize and compare JSON;
7. assert headers and schemas;
8. generate useful diagnostics.

Centralizing this flow improves consistency, readability, and failure analysis.

## Public impact

As of July 2026, the NuGet package has exceeded 700,000 cumulative downloads. Package statistics change continuously; use the live NuGet page for current figures.
