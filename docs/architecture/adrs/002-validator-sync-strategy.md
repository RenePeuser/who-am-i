# ADR-002: Validator synchronization strategy

## Status

Open for team decision

## Context

Validation rules exist in an infrastructure repository and in a backend validation engine. Names and concepts may match, differ, or exist on only one side.

## Options

### A. Maintain an explicit mapping table

Keep the backend vocabulary and map infrastructure names to backend validators.

**Advantages**

- Avoids unnecessary renaming
- Preserves backend semantics
- Makes compatibility explicit

**Disadvantages**

- Permanent mapping maintenance
- More cognitive overhead
- Potential drift

### B. Adopt infrastructure validator names in the backend

Align names directly.

**Advantages**

- Simple cross-repository comparison
- Reduced mapping logic

**Disadvantages**

- Backend API churn
- Infrastructure names may not be ideal semantic APIs
- Migration and compatibility costs

### C. Define a canonical validation vocabulary

Create a versioned canonical rule catalogue and map both implementations to it.

**Advantages**

- Clear long-term ownership
- Separates concepts from implementation names
- Supports governance and tooling

**Disadvantages**

- Highest initial effort
- Requires team agreement and migration planning

## Decision criteria

- API clarity
- backward compatibility
- code-generation requirements
- OpenAPI representation
- governance ownership
- migration cost
- frequency of rule changes
