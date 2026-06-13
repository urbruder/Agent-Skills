# Code Review Framework

## Review categories

### Correctness
Edge cases, null handling, data types, error states, race conditions.

### Maintainability
Naming, duplication, function size, cohesion, coupling, structure.

### Security
Input validation, injection risks, secrets, auth, permissions, unsafe deserialization, dependency risks.

### Performance
N+1 queries, unnecessary loops, memory use, blocking calls, caching.

### Documentation
Explain intent, public interfaces, non-obvious decisions, setup, and tests.

## Refactor principles

- preserve behavior first
- make small coherent functions
- improve names
- remove duplication
- separate concerns
- isolate side effects
- make errors explicit
- add tests around risky behavior

## Output modes

- review only
- refactor only
- review plus refactor
- add tests
- add docs
- security review
- performance review

## Caution

Do not silently change behavior. Call out breaking changes.
