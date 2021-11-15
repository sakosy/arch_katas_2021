## The "Farmacy Family" System

-   [Team Elephant on a Cycle](https://github.com/sakosy/arch_katas_2021#team-Elephant-on-Cycle)
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
	-   [Components Diagram](https://github.com/sakosy/arch_katas_2021#components-diagram)


## Team: Elephant on a Cycle

![Team_Logo](https://github.com/sakosy/arch_katas_2021/blob/main/Images/Elephant_on_Cycle.png)

**Ride, Eat, Design, repeat!**

**Team Members** 

[Sergey](https://www.linkedin.com/mwlite/in/sergey-kosyy-275265198), 
[Natalia](https://www.linkedin.com/mwlite/in/nmkh), 
[Sattar](https://www.linkedin.com/mwlite/in/sattar-gyulmamedov-0a1163), 
[Samvel](https://www.linkedin.com/in/samvel-mkhitaryan-ab081616a/)

**Who we are:** We are colleagues from the largest Telco company in Russia. We are passionate in Big Data technologies on the different positions: Architects, Product Owners, Developers. We are working with Petabyte-scale clusters, hundreeds of servers and thousends of ETL/ML/SQL tasks. We are trying to make our best to make future better than ever before. We are happy to present you our solution below.

## Glossary

- Farmacy Foods (FFoods) - Order management system.
- Farmacy Family (FFamily) - The system, needs to be designed. It will extend functionality of FFoods.
- Transactional Customer - A customer, who makes purchase using FFoods service. He/She used just FFoods.
- Engaged Customer - Transactional Customer, registeered in FFamily aswell.
- Support Community - engaged members within a community.
- Client (Customer) - low income, poverty level, homeless, college students, educators, senior citizens.
- Community - small group of engaged customers within a neighborhood area
- Medical Data Platform - an aggregation platform for EHRs from various EHR providers (e.g. [Nuna](https://www.nuna.com/))

## Overview

FFamily is an enhancement of the existing FFoods system deals with:
 - products catalog 
 - order management 
 - customer management
 - order shipping
 - payments
 - smart fridges management
 - etc.

FFamily should add tighter engagement with the customers.

FFoods has been designed before, but not developed yet (we play in the "brown fields", and it's **possible to submit requirements to FFoods**).

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

FFoods + FFamily will provide a way to **create an infinity customer journey** on both systems.
It should be possible to increase **Customer Lifetime Value (CLV)**, FFoods income and get more investors based on better analytics.

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
| ASM-1 | Farmacy Food & Farmacy Family want to inform customers about most of their activities |
| ASM-2 | Kitchens (3rd party included) want to send updates about fridges refillment and Farmacy Food support it |
| ASM-3 | Food suppliers want to send updates about fridges refillment and Farmacy Food support it |
| ASM-4 | Support Community includes all _Communities_ of Farmacy Family Customers |
| ASM-5 | Community includes customers in some concrete neighborhood |
| ASM-6 | Community may includes customers with same diet |
| ASM-7 | Dietitians will guide classes and any other education |
| ASM-8 | Improve the distribution and potential food waste from having the wrong mix of foods in a particular fridge - this is a task for Farmacy Foods, not Family: It manages the Product Catalog, it can manages Product compatibility card. |
| ASM-9 | For Communications with Customers Dietitians, Farmacy Food & Family Operators would use Farmacy Family App. Customers would use original apps of channels  |
| ASM-10 | For Classes & Eductional materials we can use MOOC |

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
| FR-7 | The nutritional company (eDietian) has access to the client's profile |
| FR-8 | Messaging between a client and dietitian |
| FR-9 | Customers can add medical information in their profiles |
| FR-10 | Customers have the ability to share information with medical service providers |
| FR-11 | Customers can customize how much profile information they want to allow the community to see at a fine-grained level |
| FR-12 | Selective access to medical information about the customer from a partner |
| FR-13 | Third party providers (clinics, doctors, etc) have access to extra analytical data (Geo data, preferences, etc) |
| FR-14 | Clinics should be able to establish baseline tests for clients. We have to gather results every 3 months. |
| FR-15 | Demonstrate any changes in overall health analyzed in clinics |
| FR-16 | Send an email elucidating additional benefits available for becoming an engaged customer when a transactional customer purchases a meal |
| FR-17 | Generate analytical data from medical information to demonstrate the benefits of Farmacy Foods |
| FR-18 | Recognize Transactional Customers that are not part of Farmacy Family |
| FR-19 | Develop relationships between engaged customers |
| FR-20 | Convert transactional customers to engaged customers |
| FR-21 | Make connections between similar demographics |
| FR-22 | Get from clinics info based on extended data, for example regional dietary observations |
| FR-23 | Customers may have access to their overall health reports |

FR-1,3,4,6,11,12,21 related to Farmacy Foods integration, Engaged Customer additional activities and weren't shown in our project. 

### Architecture Characteristics Requirements
| # | Title | Requirement |
|----|----|----|
| AR1 | Scalability         | We should care about potential growth of analytical data and communication history volume (FR-5, FR-8, FR-9). |
| AR2 | Security            | We have to operate with customer's private medical profiles. So, this type of data must be processed securely (FR-10, FR-13). |
| AR3 | Domain partitioning | We need to build independent domain areas by requirements: onboarding, community, integration. Each of them can be implemented independently (FR-5, FR-8, FR-9, FR-10). |
| AR4 | Elasticity          | The engagement could increase a number of customers drastically, so we should be able to start from just dozens of users and process up to thousands without any lacks. This follows from the system goals. |

### Fitness Functions

We will use the following pattern to determine Fithess Function for each AR:

- What we should measure?

- How we can measure?

- How we know that something wrong?

We should integrate fitness function measures into Continuous Delivery (CD) pipelines on the "TEST" stand. Also, we can monitor some of them on "PROD" stand.

**AR1**

**AR2**

**AR3**

**AR4**

- *What we should measure?*

	FF4.1 Number of application instances grows up when the number of requests (users, integrated systems requests) grows up.

	FF4.2 Number of application instances fall down when the number of requests (users, integrated systems requests) falls down.

	FF4.3 The Latency in any synchronous requests to any API/Data Store/Message Queue dos not exceeded 20% in 95% percentile in 5 min. intervals.

	FF4.4 The percentage of invalid responces (http code not equal 200) not exceeded 20% in 95% percentile in 5 min. intervals.

- *How we can measure?*

	On the "TEST" environment:

	Run HTTP Requests Generator to API from the "normal rate" (for example, 100 rpc) for just one instance and increase (for example, lineary each 10sec. multiply on 2) number of requests. After some iteratons (determine on practice) slow down generator in the same manner.

	Measure the number of instances | pods (using k8s interface or service-discovery system).  

	On the both - "TEST" and "PROD" environments:

	Measure Requests latency, HTTP Return Codes (200)

- *How we know that something wrong?* 

	On **"TEST" & "PROD"** environments: 

	Requests latency exceed required limits. 

	HTTP 200 Return Codes exceed required limits. 

	On *"TEST"* environment: 

	The number of instances has not been increased to 2 or has not been decreased to 1.

## Architecture Decision Records

| # | Description |
|----|----|
| ADR-1 | [Microservices as the base architectural style](https://github.com/sakosy/arch_katas_2021/blob/main/ADR/ADR-1%20Use%20the%20microservices%20as%20the%20base%20architectural%20style.md) |
| ADR-2 | [Components must be cloud-native](https://github.com/sakosy/arch_katas_2021/blob/main/ADR/ADR-2%20Each%20component%20must%20be%20cloud-native.md) |
| ADR-3 | [Micro-frontends pattern for UI](https://github.com/sakosy/arch_katas_2021/blob/main/ADR/ADR-3%20Use%20micro-frontends%20pattern%20for%20UI.md) |
| ADR-4 | [Sensitive medical data should be stored and processed on the certified 3rd party platforms](https://github.com/sakosy/arch_katas_2021/blob/main/ADR/ADR-4%20Sensitive%20medical%20data%20should%20be%20stored%20and%20processed%20on%20the%20certified%203rd%20party%20platforms.md) |
| ADR-5 | [Zero-Trust Architecture](https://github.com/sakosy/arch_katas_2021/blob/main/ADR/ADR-5%20Zero%20Trust%20Architecture.md) |
| ADR-6 | [SaaS Omnichannel Provider as Messaging Gateway](https://github.com/sakosy/arch_katas_2021/blob/main/ADR/ADR-6%20SaaS%20Omnichannel%20Provider%20as%20Messaging%20Gateway.md) |

Application ADR-1 & ADR-2 can be reflected on more detailed diagrams.

Despite the fact that ADR-5 depicted on Dietitian CJM Diagram this decision applied to all subsystems.


## Architecture

### Use Cases List as Customers Journeys

| # | Description | Link |
|----|----|--------|
| UC-1 | Transactional Customer converts to Engaged Customer | [Transactional Customer CJM](https://github.com/sakosy/arch_katas_2021/blob/main/Images/FF-CJM.TransactionalCustomer.png) |
| UC-2 | Engaged Customer gets Report | [Engagement Customer CJM](https://github.com/sakosy/arch_katas_2021/blob/main/Images/FF-CJM.EngagedCustomer.png) |
| UC-3 | Dietitian comunicates with Customers | [Dietitian CJM](https://github.com/sakosy/arch_katas_2021/blob/main/Images/Dietitian_CJM.png) |
| UC-4 | Clinic gather analysis results | [Clinic CJM](https://github.com/sakosy/arch_katas_2021/blob/main/Images/cjm4clinic.png) |
| UC-5 | Operator communicates with Customers | [Operator CJM](https://github.com/sakosy/arch_katas_2021/blob/main/Images/CJM4_Operator.png) |

Our diagrams right now may have some logical and other lacks, because we have some open questions.

### System Context
This is the "helicopter view" on the designed system and environment (C4 level 1).
You can see interactions between Farmacy Family and other actors (stakeholders).

![System Context](https://github.com/sakosy/arch_katas_2021/blob/main/Images/FF-C4.System_Context.png)

### Container Diagram
This is  the next C4 level, which provide as with understanding of required modules and communication protocols between them.
Not all components are described well enought, but in general, we recommend using ADR's principles to design each of them.

![System Context](https://github.com/sakosy/arch_katas_2021/blob/main/Images/FF-C4.ContainerDiagram.png)

### Components Diagrams

![Container: API 4 Farmacy Foods](https://github.com/sakosy/arch_katas_2021/blob/main/Images/Component%20-%20API%204%20FFoods.png)
