# Testing is architecture

Testing reveals the shape of a system.

A design that is easy to exercise through stable public behavior is usually better separated and more understandable than one requiring extensive internal knowledge.

## Testing layers

- Unit tests for focused rules
- Contract tests for public schemas and protocols
- Integration tests through real ASP.NET Core hosts
- Snapshot tests for broad regression detection
- Architecture tests for solution and dependency constraints
- Generated samples to verify documentation and contracts

## Framework responsibility

A reusable platform should ship testing affordances alongside runtime features. Product teams should not reverse-engineer internal infrastructure merely to verify their endpoints.
