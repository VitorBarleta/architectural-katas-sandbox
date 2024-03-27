# Choosing a software architecture: The Notification Microservice

Status: Approved

## Context
This project is going to be responsible for listening to events and sending the notifications (Email, SMS, and push) accordingly.

For this project the only reasonable architecture for now is the Vertical Slice Architecture.

## Rationale

The layered architectural styles such as Clean Architecture, Onion Architecture, Hexagonal Architecture are simply to complex for the purpose of listening to events and sending notifications. There are no data access layers, maybe a content management system in the future for storing the message templates, but that is it.

## Consequences

The Vertical Slice architecture will be simpler to work with due to the simplicity of the problem it solves and it does not require the higher level of abstraction that the layered architectures provide, and the team will have no problem working on multiple features at the same time in this project.
