# Organization: Simulated Hospital - HL7 v2 SIU to FHIR Appointment - AU Core (Proof of Concept) v0.1.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Organization: Simulated Hospital**

## Example Organization: Organization: Simulated Hospital

Profile: [AU Core Organization](http://hl7.org.au/fhir/core/2.0.0/StructureDefinition-au-core-organization.html)

Simulated Hospital (http://example.org/fhir/sid/organization#SIMHOSP)

-------

| | |
| :--- | :--- |
| Active: | true |
| Contact Detail | * ph: 07 0000 0000(Work)
* 1 Simulated Way, Brisbane, QLD 4000(work)
 |



## Resource Content

```json
{
  "resourceType" : "Organization",
  "id" : "organization-simhosp",
  "meta" : {
    "profile" : ["http://hl7.org.au/fhir/core/StructureDefinition/au-core-organization"]
  },
  "identifier" : [{
    "system" : "http://example.org/fhir/sid/organization",
    "value" : "SIMHOSP"
  }],
  "active" : true,
  "name" : "Simulated Hospital",
  "telecom" : [{
    "system" : "phone",
    "value" : "07 0000 0000",
    "use" : "work"
  }],
  "address" : [{
    "use" : "work",
    "type" : "physical",
    "text" : "1 Simulated Way, Brisbane, QLD 4000",
    "line" : ["1 Simulated Way"],
    "city" : "Brisbane",
    "state" : "QLD",
    "postalCode" : "4000",
    "country" : "AU"
  }]
}

```
