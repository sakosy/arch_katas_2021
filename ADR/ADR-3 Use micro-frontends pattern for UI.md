# Use micro-frontends pattern for UI

## Context
We have two separate applications: Farmacy Foods (reactive monolith) and Farmacy Family which provide low coupeled functionality, but it shouldn't be separate mobile apps or web sites for the customers. This will provide the best user experience. Although, development teams can work separetelly, technology stack can be changed separetelly even if we have common desigh patterns for UI|UX.

## Decision
Use micro-frontends pattern, which provide standartized common UI container which can incorporate different frontends from different apps.

## Consequences
We still have a general UI container ("single point of UI") which should be designed carefully.
