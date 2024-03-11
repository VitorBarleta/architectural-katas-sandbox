# Agile Dead Trees

A publisher wants to unify its authoring CMS and customer store experience.

Users: dozens of publisher employees, hundreds of authors, thousands/millions of customers

Requirements: authors publish chapters; reviewers see the chapters, make review comments, and notify authors on review; authors can reject proposed review changes; customers can buy books (either e- form or dead trees form) online, including those available in "beta"; publisher can push authors' chapters to those customers who bought the "beta"

## Architecture

### Context

The company wants to unify its authoring and store systens into one, meaning that the business is well stablished, only made more clear by the fact that they have hundreds of authors and possible millions of customers. Given the scale of the solution there are a few strategies and architectures that can be used to accomplish this unification.

- Monolith: due to its strenghts in regards of complexity (low) and the fastest to develop.
- Microservices: due to its scalability and adaptability.
- Modular-Monolith: due to its low complexity in comparison to the microservices architecture and due to its modularity, it is very adaptable.

### Rationale

The chosen architecture is the microservices, due to:

- The project needs scalability, not only for a possible future growth of customers, but mainly due to different parts of the application being more accessed than others, which makes the Monolith architecture not suitable.
- The project is not a small project and its scope is very well defined, which makes the Modular Monolith architecture not suitable because its a Monolith nonetheless and its best use is when you need fast feature deployment, with a not well defined scope and the hability to grow into a microservices architecure.
- The microservices architecture provides the full scalability that the solution needs with the down side of its complexity, but in my opinion, the advantages more than outweight the disadvantages.

### Consequences

By choosing the Microservices architecture, we will need to invest effort making sure that the comunication between modules are not creating dependencies between said modules and making sure that the comunication is reliable when need be. This will create more work for the cloud and infrastructure team and also for the DevOps team.

