# Choosing a software Architecture: The Review microservice

Status: Approved

## Context

The review microservice will allow reviewers to read the chapters and make recomendations to the creator before publishing.

The Vertical Slice architecture is the best option for now because the project is very simple in the way that it will receive the book, chapter and the review information and store it for the creator to see and take actions.

## Rationale

Although the microservice will have storage, the data is not highly relational and the business requirements are not complex enough to justify an architecture with a higher level of abstraction.

## Consequences

The project is going to be simple to work with, all the features are going to be very concise and The team will not have problems working on different features at the same time.
