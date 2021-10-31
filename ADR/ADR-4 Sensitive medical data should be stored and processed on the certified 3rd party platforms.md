# Sensitive medical data (part of customer profiles) should be stored and processed on the certified 3rd party platforms

## Context
[CNS-3]	Some data can be considered as information about any ongoing or chronic conditions, so it complies the HIPAA Security rule. 
Farmacy Faminly can 

- provide the infrastructure and processes that meett the requirements https://www.hhs.gov/sites/default/files/ocr/privacy/hipaa/administrative/securityrule/security101.pdf
- partner with a 3rd party platforms, e.g. helthcare data aggregator like [nuna](https://www.nuna.com/)

## Decision
We've chosen to partner with a 3rd party platform. Farmacy Family is a startup and may not have enough resources yet to meet all the requiments of the HIPAA Security Rule. All the EHR data needed would be recieved online from the partner's platform  

## Consequences
- Farmacy Family still has to use FHIR protocol
- data variety may be limited
- additional requirements to the partner's platform emerge
