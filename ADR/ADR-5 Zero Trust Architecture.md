# Zero Trust Architecture

## Status
Proposed

## Context
We work with medical data so that we can't trust to requests from the same subnetwork.

## Decision
We need to enable authentication between all modules.

## Consequences
This will complicate the exchange of data between modules, but will avoid data leakage.


Adding a Zero Trust Architecture should be low-cost because we are using a microservice architecture.
