# Location: Outpatient Clinic 1 - HL7 v2 SIU to FHIR Appointment - AU Core (Proof of Concept) v0.1.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Location: Outpatient Clinic 1**

## Example Location: Location: Outpatient Clinic 1

Profile: [AU Core Location](http://hl7.org.au/fhir/core/2.0.0/StructureDefinition-au-core-location.html)

Outpatient Clinic 1 (Clinic) (http://example.org/fhir/sid/location#SIMHOSP/OPD/CLINIC1)

-------

| | | | |
| :--- | :--- | :--- | :--- |
| Status: | Active | Form: | Room |
| Type: | Clinic | | |
| Address: | 1 Simulated Way, Brisbane, QLD 4000(work) | | |
| Managed By: | [Simulated Hospital](Organization-organization-simhosp.md) | | |



## Resource Content

```json
{
  "resourceType" : "Location",
  "id" : "location-simhosp-opd-clinic1",
  "meta" : {
    "profile" : ["http://hl7.org.au/fhir/core/StructureDefinition/au-core-location"]
  },
  "identifier" : [{
    "system" : "http://example.org/fhir/sid/location",
    "value" : "SIMHOSP/OPD/CLINIC1"
  }],
  "status" : "active",
  "name" : "Outpatient Clinic 1",
  "type" : [{
    "coding" : [{
      "system" : "http://example.org/fhir/CodeSystem/v2-local/LOCAL",
      "code" : "CLIN",
      "display" : "Clinic"
    }],
    "text" : "Clinic"
  }],
  "address" : {
    "use" : "work",
    "type" : "physical",
    "text" : "1 Simulated Way, Brisbane, QLD 4000",
    "line" : ["1 Simulated Way"],
    "city" : "Brisbane",
    "state" : "QLD",
    "postalCode" : "4000",
    "country" : "AU"
  },
  "physicalType" : {
    "coding" : [{
      "system" : "http://terminology.hl7.org/CodeSystem/location-physical-type",
      "code" : "ro",
      "display" : "Room"
    }]
  },
  "managingOrganization" : {
    "reference" : "Organization/organization-simhosp",
    "display" : "Simulated Hospital"
  }
}

```
