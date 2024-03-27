# Choosing a software Architecture: The Books microservice

Status: Approved

## Context

The books microservice will be responsible for storing all the books and allow the publishers to edit the books.

The architectures considered are:
- Clean Architecture
- Vertical Slice

The choice is Clean Architecture.

## Rationale

Since this microservice will have its own database, services and events, the vertical slice architecture is too simplistic but the Clean architecture is too much. So we are going with the Clean Architecture but in a single project and enforce the Clean Architecture rules using ArchUnitNet. This approach will provide all the benefits of the clean architecture without the complexity of managing multiple projects and its dependencies.

## Consequences

By going with the Clean Architecture but not creating multiple projects, the solution becomes simpler to find things, since instead of projects with their own dependencies and references, we are going to have folders. The downside is the need to enforce the Clean Architecture using additional tests using the ArchUnitNet library in which the team is going to have to invest some time learning.
