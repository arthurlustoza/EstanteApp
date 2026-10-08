# ADR 0001: Use of Jetpack Compose for UI

- Status: Accepted
- Date: 2026-10-08

## Context
Since the application targets Android devices, it is crucial that the user interface be built using a modern framework like Jetpack Compose, ensuring a contemporary and highly optimized UI.

## Decision
Use Jetpack Compose: Structures characterized by good organization and planning.

## Alternative Considered
- XML ​​with Views: Requires more code and relies on a structure that is no longer aligned with current market standards.

## Consequences
- Pros: Widely adopted approach with active, ongoing support.
- Cons: The Compose compiler (kotlin-compiler-plugin) adds overhead and increases build times for the project.