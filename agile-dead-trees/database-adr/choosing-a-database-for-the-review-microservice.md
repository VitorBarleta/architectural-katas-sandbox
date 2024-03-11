# Agile Dead Trees: Choosing a database for the review microservice

## Context

The review microservice is responsible for allowing reviewers write comments about a chapter and later this comments will be reviewed by the author and can be accepted of rejected.

Given the nature of the problem, a relational database or a document database can be used. For this scenario, a relational database like PostgreSQL is enought to fulfill the needs of the microservice.

## Rationale

The relational database was chosen due to:
    - A document database would work, but performance is not a concern in this case since the volume of data is very small.
    - The data model is highly relational, with chapters having many comments and comments could be made in many chapters. Also, a comment could have replies.
    - Volume of data is very low and volume of accesses are also not as high as the other microservices, so scalability is not a problem for now since we could still scale vertically.
    - Offers better search capabilities if there is a need to search keywords inside comments.

## Consequences

Since the technology is very well known by the development team, the learning curve is very mild if any, and also it offers better benefits for the current problem.
