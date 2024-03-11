# Agile Dead Trees: choosing a database for the order processing microservice

## Context

The orders processing microservice is responsible for processing the orders of users. An order can have multiple items.

Based on this requirements a relational database should be enought to handle these requirements.

## Rationale

The relational database was chosen due to:
    - The operations are mostly write with very few reads.
    - Strongly defined and relational data model.
    - Low access volume so no need to worry about scalability too much
    - Highly transactional data.

## Consequences

By using the relational database, the team will not need to invest time learning about the technology since it is very used to it. The main disadvantage of the relation database is horizontal scale, but it is not a concern for the use case right now and the advantages it has over a document database outweights the disadvantages.
