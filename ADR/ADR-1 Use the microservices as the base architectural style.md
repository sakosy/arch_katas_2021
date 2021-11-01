# Use the microservices as the base architectural style

## Context
Farmacy Family is a start up company and does not have experienced developers available. But also we have a low coupled domains: onboarding, community, integration.
We need to be able to use agile methodologies for development team: prioritize our goals and implement system's features independently.

## Decision
Microservice architecture provide to system a list of characteristics which has been choosen as significant for the Farmacy Family: **scalability, domain partitioning, elasticity**. These characteristics we considered as the primary quality attributes of our system. We will use microservices to implement system components with independent code bases, ci|cd processes, databases etc.

## Consequences
We realize, that microservice architecture is not a good decision for simplicity and cost (Farmacy Family is a startup). But this architecture style is the best choice for cloud-native applications, which is ADR-2.
