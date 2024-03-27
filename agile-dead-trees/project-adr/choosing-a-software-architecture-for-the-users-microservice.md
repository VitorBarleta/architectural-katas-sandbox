# Agile Dead Trees: Choosing a sofware architecture for the users microservice

Status: Approved

## Context

The users microservice will be responsible for handling user creation, authentication, profile edition, and the cart.

Architecture styles considered:
- Vertical Slice Architecture
- Clean Architecture

The chosen architecture is the Clean Architecture

## Rationale

Because the Users microservice is rather complex and has a strong domain logic with events and such, the Clean Architecture will offer more abstraction and thus, better flexibility.

The Vertical Slice architecture is too simple and would not be fit for such a complex business logic the this microservice requires.

## Consequences

The Clean Architecture is harder to work with in a big team, since multiple peaple can change the same file when adding a feature, however, we think that the abstraction that it provides is more important and outweights the downside of the possible source control conflicts.
