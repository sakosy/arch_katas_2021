# Each component must be cloud-native application

## Context
Farmacy Foods and Farmacy Family are startups, and shouldn't pay a lot of money for the infrastructure. They needs elastic and easy extensible infrastructure. Public clouds are the best choice in this situation.

## Decision
Design all components as a cloud-native apps. In this case it will take minimal efforts for deploy in any public cloud. But also, application design shuld be built on principle "no vendor lock" - it should be possible to change cloud providers with minimum efforts as well.

## Consequences
In the modern world there are no alternatives for the startups. IT infrastructure is very expensive, needs to be servised by high-skilled administrators, because of COVID-19 lock-downs we have a serious delays in supply chains.
