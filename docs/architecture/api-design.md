# API design

## Principles

- Names should reveal semantics.
- Similar concepts should use consistent signatures.
- Defaults should be safe and predictable.
- Optionality should be explicit.
- Public contracts should not expose internal mechanics.
- Extension points should be narrow and deliberate.
- Error behavior is part of the API.
- OpenAPI output is part of the API.
- Migration paths matter as much as initial elegance.

## Attribute API example

Prefer:

```csharp
[RequiredWhen(
    nameof(JobType),
    ConditionOperator.NotEqualsTo,
    JobType.PythonShell)]
```

over an attribute that exposes implementation-oriented delegates or opaque condition objects.

The semantic form remains readable in domain models and can be interpreted by validation, OpenAPI, samples, and tooling.
