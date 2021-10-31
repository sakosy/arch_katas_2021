## The "Farmacy Family" System

**Team Name:** Elephant on Cycle

![Team_Logo](https://github.com/sakosy/arch_katas_2021/blob/main/Images/Elephant_on_Cycle.png)

**Team Members:** *Sergey, Natalya, Sattar, Samvel*

**Who we are:** We are colleagues from the largest Telco company in Russia. We are passionate in Big Data technologies on the different positions: Architects, Product Owners, Developers. We are working with Petabyte-scale clusters, hundreeds of servers and thousends of ETL/ML/SQL tasks. We are trying to make our best to make future better than ever before. We are happy to present you our solution below.

-   [Glossary](https://github.com/sakosy/arch_katas_2021#glossary)
-   [Overview](https://github.com/sakosy/arch_katas_2021#overview)
-   [Business Case and Goals](https://github.com/sakosy/arch_katas_2021#business-case-and-goals)
-   [Stakeholders](https://github.com/sakosy/arch_katas_2021/blob/main/stakeholders.md)
-   [System Requirements](https://github.com/sakosy/arch_katas_2021#system-requirements)
    -   [Functional Requirements](https://github.com/sakosy/arch_katas_2021#functional-requirements)
    -   [Architecture Characteristics Requirements](https://github.com/sakosy/arch_katas_2021#architecture-characteristics-requirements)
    -   [Constraints](https://github.com/sakosy/arch_katas_2021#constraints)
    -   [Assumptions](https://github.com/sakosy/arch_katas_2021#assumptions)
-   [Architecture Decision Records](https://github.com/sakosy/arch_katas_2021#architecture-decision-records)
-   [Architecture](https://github.com/sakosy/arch_katas_2021#architecture)
	-   [Customer Jurney](https://github.com/sakosy/arch_katas_2021#customer-journey)
	-   [System Context](https://github.com/sakosy/arch_katas_2021#system-context)
	-   [Container Diagram](https://github.com/sakosy/arch_katas_2021#container-diagram)

## Glossary

- Farmacy Foods (FFoods) - Order management system.
- Farmacy Family (FFamily) - The system, needs to be designed. It will extend functionality of FFoods.
- Transactional Customer - A customer, who makes purchase using FFoods service. He/She used just FFoods.
- Engaged Customer - Transactional Customer, registeered in FFamily aswell.
- Support Community - engaged members within a community.
- Client (Customer) - low income, poverty level, homeless, college students, educators, senior citizens.
- Community - small group of engaged customers within a neighborhood area
- Medcal Data Platform - an aggregation platform for EHRs from various EHR providers (e.g. [Nuna](https://www.nuna.com/))

## Overview

FFamily should add tighter engagement with their customers.

FFamily is an enhancement of the existing FFoods system deals with:
 - products catalog 
 - order management 
 - order shipping
 - payments
 - smart fridges management
 - etc.

 FFoods has been designed before, but not developed yet (we play in the "brown fields", and it's possible to submit requirements to FFoods).

 FFamily needs to be aware of seamless integration with FFoods.

## Business Case and Goals

The overall goal of FFamily is to connect, gather, analyze, and communicate.

Primary goals are:
- develop relationships between engaged customers and nurture those relationships;
- convert transactional customers to engaged customers;
- generate analytical data from medical information to demonstrate the benefits of FFoods;


Users: Hundreds, separated by distinct geographic zones.
Additionally, different clusters of customers frequently consolidate around similar dietary requirements.
Shouldfocus on ensuring that entire offering is accommodating to low income, poverty, and homeless.

FFamily should provide the Customer Relationship Management system (CRM) and Customer Data Profile system (CDP). Also it should provide the ability to get Data-Driven decisions and analytics.

The desired solution from the functional perspective:

![Marketecture](https://github.com/sakosy/arch_katas_2021/blob/main/Images/marketecture.png)

FFoods + FFamily will provide a way to create an infinity customer journey on both systems.
It should be possible to increase Customer Lifetime Value (CLV), FFoods income and get more investors based on better analytics.

## Stakeholders

There is a list of all stakeholders for the _Farmacy Family_

| FFoods Stakeholders | FFamily Stakeholders | Concerns |
|----|----|--------|
| Ghost Kitchen | Ghost Kitchen | updates refilling and delivery info |
| Subscribers | Transactional Customers | need to be informed about engagement benefits & registration process |
| Known users | Transactional Customers | need to be informed about engagement benefits & registration process |
| Occasional users | Transactional Customers | Visually select a meal, get info about it and pay in the most convenient way at the same time |
| -- | Engaged Customers | requests\receives advices, overall health reports |
| Owner | Owner | gets advanced analytics to be sure that investments work well |
| -- | Operators | need to communicate with customers about their issues |
| | | communicate with community |
| Nutritionists | Dietitian | gives advice to the community |
| | | gives personal advice |
| | | get selective access to medical information |
| -- | Medical Clinics | gather results of baseline tests for clients |
| -- | Gov regulators | must be sure that confidential medical info processed regarding the law |
| -- | Investors | gets advanced analytics to be sure that investments work well |
| Developers | Maintenance Team | Ease of maintaining and developing the system |
| Admins | Maintenance Team | Ease of monitoring |
| Food suppliers | Food suppliers | updates delivery info |
| 3rd party kitchens | 3rd party kitchens | Same as for Ghost Kitchen |
| -- | Farmacy Foods | improve distribution and food waste from having the wrong mix of foods in a particular fridge |

## Constraints

| # | Description |
|----|----|
| CNS-1 | Add Farmacy Family user interface to existing Foods interface, which is currently a Reactive monolith. Create a holistic UX for both food and Farmacy Family to support engagement model |
| CNS-2 | Farmacy Foods is a startup, so it will not be able to spend a lot of money for the development |
| CNS-3 | Some data can be considered as information about any ongoing or chronic conditions, so Farmacy Foods complies the HIPAA [Security rule](https://www.asha.org/practice/reimbursement/hipaa/hitech-act/) |


## Assumptions

| # | Description |
|----|----|
| ASM-1 | Farmacy Food & Farmacy Family wants to inform customers about most of their activities |
| ASM-2 | kitchens (3rd party included) wants to send updates about fridges refillment and Farmacy Food support it |
| ASM-3 | Food suppliers wants to send updates about fridges refillment and Farmacy Food support it |
| ASM-4 | Support Community includes all _Communities_ of Farmacy Family Customers |
| ASM-5 | Community includes customers in some concrete neighborhood |
| ASM-6 | Community may includes customers with same diet |
| ASM-7 | Dietitians will guides classes and any other education |

## System Requirements

### Functional Requirements

| # | Functional Requirement |
|----|----|
| FR-1 | Manage customer profiles |
| FR-2 | Personalization around preferences and dietary needs of the customer |
| FR-3 | Support geographical trend analysis to hone Farmacy Family’s ability to optimize the foods delivered to fridges (an additional integration point TO Farmacy Foods)|
| FR-4 | Support push and pull models for community engagement |
| FR-5 | Manage forums, emails, reference material, class information, and other media |
| FR-6 | Support gathering transactional member information |
| FR-7 | The nutritional company(eDietian) has access to the client's profile |
| FR-8 | Messaging between a client and dietitian |
| FR-9 | Customers can add medical information in their profiles |
| FR-10 | Customers have the ability to share information with medical service providers |
| FR-11 | Customers can customize how much profile information they want to allow the community to see at a fine-grained level |
| FR-12 | Selective access to medical information about the customer from a partner |
| FR-13 | Third party providers(clinics, doctors, etc) have access to extra analytical data(Geo data, preferences, etc) |
| FR-14 | Clinics should be able to establish baseline tests for clients. We have to gather results every 3 months. |
| FR-15 | Demonstrate any changes in overall health analyzed in clinics |
| FR-16 | Send an email elucidating additional benefits available for becoming an engaged customer when a transactional customer purchases a meal |
| FR-17 | Generate analytical data from medical information to demonstrate the benefits of Farmacy Foods |
| FR-18 | Recognize Transactional Customers that are not part of Farmacy Family |
| FR-19 | Develop relationships between engaged customers |
| FR-20 | Convert transactional customers to engaged customers |
| FR-21 | Make connections between similar demographics |
| FR-22 | Get from clinics info based on extended data, for example regional dietary observations |


### Architecture Characteristics Requirements
- **Scalability:** We should care about potential growth of analytical data and communication history volume (FR-5, FR-8, FR-9).
- **Security:** We have to operate with customer's private medical profiles. So, this type of data must be processed securely (FR-10, FR-13).
- **Domain partitioning:** We need to build independent domain areas by requirements: onboarding, community, integration. Each of them can be implemented independently (FR-5, FR-8, FR-9, FR-10).
- **Elasticity:** The engagement could increase a number of customers drastically, so we should be able to start from just dozens of users and process up to thousands without any lacks. This follows from the system goals.

## Architecture Decision Records

## Architecture

### Customer Journey

#### Transactional Customer

#### Engaged Customer

#### Dietitian
![Dietitian CJM](https://github.com/sakosy/arch_katas_2021/blob/main/Images/Dietitian_CJM.png)

#### Clinic
![Clinic CJM](https://github.com/sakosy/arch_katas_2021/blob/main/Images/cjm4clinic.png)

#### Operator
![Operator CJM](https://github.com/sakosy/arch_katas_2021/blob/main/Images/CJM4_Operator.png)

### System Context
This is the "helicopter view" on the designed system and environment (C4 level 1).
You can see interactions between Farmacy Family and other actors (stakeholders).

![System Context](https://github.com/sakosy/arch_katas_2021/blob/main/Images/FF-C4.System_Context.png)

### Container Diagram
