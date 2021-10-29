## The "Farmacy Family" System

**Team:** Elephant on Cycle
**Team Members:** *Sergey, Natalya, Sattar, Samvel*

-   [Glossary](https://github.com/sakosy/arch_katas_2021#glossary)
-   [Overview](https://github.com/sakosy/arch_katas_2021#overview)
-   [Business Case and Goals](https://github.com/sakosy/arch_katas_2021#business-case-and-goals)
-   [Stakeholders](https://github.com/sakosy/arch_katas_2021/blob/main/stakeholders.md)
-   [System Requirements](https://github.com/sakosy/arch_katas_2021#system-requirements)
    -   [Functional Requirements](https://github.com/sakosy/arch_katas_2021#functional-requirements)
    -   [Architecture Characteristics Requirements](https://github.com/sakosy/arch_katas_2021#architecture-characteristics-requirements)
    -   [Constraints](https://github.com/sakosy/arch_katas_2021#constraints)
    -   [Assumptions](https://github.com/sakosy/arch_katas_2021#assumptions)
-  [Architecture Decision Records](https://github.com/sakosy/arch_katas_2021#architecture-decision-records)
- [Architecture](https://github.com/sakosy/arch_katas_2021#architecture)
	- [Use Case Model](https://github.com/sakosy/arch_katas_2021#usecase-model)
	- [System Context](https://github.com/sakosy/arch_katas_2021#system-context)

## Glossary

- Farmacy Foods (FFoods) - Order management system.
- Farmacy Family (FFamily) - The system, needs to be designed. It will extend functionality of FFoods.
- Transactional Customer - A customer, who makes purchase using FFoods service. He/She used just FFoods.
- Engaged Customer - Transactional Customer, registeered in FFamily aswell.
- Support Community - engaged members within a community.
- Client - low income, poverty level, homeless, college students, educators, senior citizens.
- Community - small group of engaged customers within a neighborhood area

## Overview

FFamily should adds tighter engagement with their customers.

FFamily is an enhancement of the existing FFoods system deals with:
 - products catalog 
 - order management 
 - order shipping
 - payments
 - smart fridges management
 - etc.

 FFoods has been designed before, but not developed yet (we play in the "brown fields" and it's possible to submit requirements to FFoods).

 And FFamily needs to be aware of seamless integration with FFoods.

## Business Case and Goals

The Company primary goals are:
- develop relationships between engaged customers and nurture those relationships
- convert transactional customers to engaged customers
- generate analytical data from medical information to demonstrate the benefits of FFoods

Thus, the overall goal of FFamily is to connect, gather, analyze, and communicate.

Users: Hundreds, separated by distinct geographic zones.
Additionally, different clusters of customers frequently consolidate around similar dietary requirements.
A focus on ensuring that entire offering is accommodating to low income, poverty, and homeless.

FFamily should provide functionality of Customer Relationship Management system (CRM) and Customer Data Profile system (CDP). Also it should provide the ability to get Data-Driven decisions.

Thus, it should be possible to increase Customer Lifetime Value (CLV) and get more investors based on better analytics.

The desired solution from the functional perspective:

[![Marketecture](https://github.com/sakosy/arch_katas_2021/images/marketecture.jpg)](https://github.com/sakosy/arch_katas_2021/images/marketecture.jpg)

## Stakeholders

## System Requirements

### Functional Requirements

| # | Functional Requirement
|----|----|
| FR1 | Manage customer profiles |
| FR2 | Personalization around preferences and dietary needs of the customer |
| FR3 | Support geographical trend analysis |
| FR4 | Support push and pull models |
| FR5 | Support subscriptions, forums, reference material, class information, and other media |
| FR6 | Support transactional member information |
| FR7 | The nutritional company(eDietian) has access to the client's profile |
| FR8 | Messaging between a client and dietitian |
| FR9 | Customers can add medical information in their profiles |
| FR10 | Customers have the ability to share information with medical service providers |
| FR11 | Customers can customize how much profile information they want to allow the community to see |
| FR12 | Third party providers(clinics, doctors, etc) have access to extra analytical data(Geo data, preferences, etc) |

### Architecture Characteristics Requirements
- Scalability
- Security (?)

## Architecture Decision Records

## Architecture