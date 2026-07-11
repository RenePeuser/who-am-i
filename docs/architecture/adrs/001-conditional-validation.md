# ADR-001: Conditional property validation

## Status

Proposed / evolving

## Context

Contracts require semantic rules such as:

- a property must be null when another property has a value;
- a property is required unless a particular mode is selected;
- two properties must differ;
- a value must satisfy a constraint only under a source-property condition.

C# attributes cannot naturally accept runtime delegates or expression trees because attribute arguments are restricted to compile-time representable values.

## Decision direction

Use a reusable conditional-validation base that accepts:

- source property name;
- condition operator;
- optional comparison value;
- optional sample values.

Derived semantic attributes implement the target constraint.

```csharp
public sealed class MustBeNullWhenAttribute(...) 
    : ConditionalPropertyValidationAttribute(...)
{
    internal override bool SatisfiesConstraint(
        ConditionalPropertyValidationContext context)
        => context.TargetValue is null;
}
```

## Consequences

### Positive

- Readable domain contracts
- Reusable condition evaluation
- Shared diagnostics
- OpenAPI and sample integration
- Semantic derived attributes

### Negative

- Property names use `nameof` rather than strongly typed expressions
- Reflection is required
- Comparison-value conversion requires careful diagnostics
- Operator and attribute vocabulary must remain stable
