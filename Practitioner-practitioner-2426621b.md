# Practitioner: DR RAJ JONES - HL7 v2 SIU to FHIR Appointment - AU Core (Proof of Concept) v0.1.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Practitioner: DR RAJ JONES**

## Example Practitioner: Practitioner: DR RAJ JONES

Profile: [AU Core Practitioner](http://hl7.org.au/fhir/core/2.0.0/StructureDefinition-au-core-practitioner.html)

DR RAJ JONES (Medicare Provider Number: 2426621B)

-------



## Resource Content

```json
{
  "resourceType" : "Practitioner",
  "id" : "practitioner-2426621b",
  "meta" : {
    "profile" : ["http://hl7.org.au/fhir/core/StructureDefinition/au-core-practitioner"]
  },
  "identifier" : [{
    "type" : {
      "coding" : [{
        "system" : "http://terminology.hl7.org.au/CodeSystem/v2-0203",
        "code" : "UPIN"
      }],
      "text" : "Medicare Provider Number"
    },
    "system" : "http://ns.electronichealth.net.au/id/medicare-provider-number",
    "value" : "2426621B"
  }],
  "name" : [{
    "text" : "DR RAJ JONES",
    "family" : "JONES",
    "given" : ["RAJ"],
    "prefix" : ["DR"]
  }]
}

```
