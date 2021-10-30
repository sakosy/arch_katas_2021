## The "Farmacy Family" System

**Team:** Elephant on Cycle
![Team_Logo](https://github.com/sakosy/arch_katas_2021/images/Elephant_on_Cycle.png)

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

There are list of all stakeholders for the _Farmacy Family_

| ArchCollider Stakeholder | Our Stakeholder | Concerns |
|----|----|--------|
| Ghost Kitchen | Ghost Kitchen | updates refillment info |
| Subscribers | Transactional Customers | Create a menu and getting meals on time |
| | | Get notification about arriving or delayed food to save their time |
| | | Be informed about meal ingredients |
| Known users | Transactional Customers | Browse catalog and buy food with guarantee of getting it when they come to pick it up |
| | | Ease of buying process |
| | | Be informed about meal ingredients |
| Occasional users | Transactional Customers | Visually select a meal, get info about it and pay in the most convinient way at same time|
| Owner | Operators | Attract all type of users |
| | | Improve quality of provided food and service |
| | | Information about users preferences |
| | | Support for accounting system |
| Nutritionists | Dietitian | Search in catalog by specific components |
| | | Calculation % of fats\carbs\vitamins\... |
| -- | Medical Clinics | need to be added |
| -- | Gov regulators | need to be added |
| -- | Investors | need to be added |
| Developers | Maintenance Team | Ease of maintaining and developing the system |
| Admins | Maintenance Team | Ease of monitoring |
| | | Ease of configuration and scaling |
| Food suppliers | Food suppliers | Predicted plan of purchases and delivery |
| 3rd party kitchens | 3rd party kitchens | Same as for Ghost Kitchen |

## Assumptions

| # | concerns |
|----|----|
| ASM-1 | kitchens refills fridges |


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
- Domain partitioning
- Elasticity

## Architecture Decision Records

## Architecture
