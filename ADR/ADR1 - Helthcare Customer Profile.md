# Use the microservice architecture style with containerization

## Context
Farmacy Family is a start up company and does not have experienced developers available.
The architecture style for the Farmacy Family system should be simple, maintainable and evolvable, be able to support domains partitioning.

##Decision
Microservice architecture apply to system a list of characteristics: scalability, domain partitioning, elasticity. These characteristics we considered as the primary quality attributes of our system.

##Consequences
We realize, that microservice architecture is not a good decision for simplicity and cost (Farmacy Family is a startup). But this architecture style is the best choice for cloud-native applications, which is ADR-2.
