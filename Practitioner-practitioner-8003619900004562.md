# Practitioner: DR JANE SMITH - HL7 v2 SIU to FHIR Appointment - AU Core (Proof of Concept) v0.1.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Practitioner: DR JANE SMITH**

## Example Practitioner: Practitioner: DR JANE SMITH

Profile: [AU Core Practitioner](http://hl7.org.au/fhir/core/2.0.0/StructureDefinition-au-core-practitioner.html)

DR JANE SMITH (HPI-I: 8003619900004562)

-------



## Resource Content

```json
{
  "resourceType" : "Practitioner",
  "id" : "practitioner-8003619900004562",
  "meta" : {
    "profile" : ["http://hl7.org.au/fhir/core/StructureDefinition/au-core-practitioner"]
  },
  "identifier" : [{
    "type" : {
      "coding" : [{
        "system" : "http://terminology.hl7.org/CodeSystem/v2-0203",
        "code" : "NPI"
      }],
      "text" : "HPI-I"
    },
    "system" : "http://ns.electronichealth.net.au/id/hi/hpii/1.0",
    "value" : "8003619900004562"
  }],
  "name" : [{
    "text" : "DR JANE SMITH",
    "family" : "SMITH",
    "given" : ["JANE"],
    "prefix" : ["DR"]
  }]
}

```
