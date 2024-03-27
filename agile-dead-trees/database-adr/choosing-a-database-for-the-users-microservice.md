# Agile Dead Trees: Users microservice database choice

Status: Approved

## Context

The users microservice will handle user creation, update, login, permissions, password reset and others. Given that the data is highly relational, the best solution is to go with a relational database such as PostgreSQL.

## Rationale

The option to go with PostgreSQL is because:

    - The data is going to be 100% relational, such as Users, Claims, Roles, Tokens, etc.
    - Has all the features needed for solving the problem with high performance and high reliability.
    - Does not require a license. Although it is not important right now, since we are going to use a cloud host server, it we opt in the future to migrate to on-premise, there is no need to pay the lincense fee.
    - Is the database that the development team is most accostumed to, so less learning curve for the entire team.

## Consequences

By choosing the PostgreSQL database, we do not need to invest much time learning the technology since the teaam is very familiar with it. Also, PostgreSQL is one of, if not the most feature rich relation databases out there, so we are not making compromises by choosing a database simply because we know it better than the others.
