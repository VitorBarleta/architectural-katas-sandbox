# Choosing a software Architecture: The Order Processing microservice

Status: Approved

## Context

The order processing microservice will be responsible for processing the payment when users check out their cart items. This microservice will listen to events and receive the payment information to send to a payment gateway.

The architectures considered are:
- Clean Architecture
- Vertical Slice

The choice is Clean Architecture.

## Rationale

Since this microservice will have its own database and services, the vertical slice architecture is too simplistic but the Clean architecture is too much. So we are going with the Clean Architecture but in a single project and enforce the Clean Architecture rules using ArchUnitNet. This approach will provide all the benefits of the clean architecture without the complexity of managing multiple projects and its dependencies.

## Consequences

By going with the Clean Architecture but not creating multiple projects, the solution becomes simpler to find things, since instead of projects with their own dependencies and references, we are going to have folders. The downside is the need to enforce the Clean Architecture using additional tests using the ArchUnitNet library in which the team is going to have to invest some time learning.
