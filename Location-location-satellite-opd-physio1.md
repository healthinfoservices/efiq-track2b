# Location: Physio Room 1 - HL7 v2 SIU to FHIR Appointment - AU Core (Proof of Concept) v0.1.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Location: Physio Room 1**

## Example Location: Location: Physio Room 1

Profile: [AU Core Location](http://hl7.org.au/fhir/core/2.0.0/StructureDefinition-au-core-location.html)

Physio Room 1 (http://example.org/fhir/sid/location#SATELLITE/OPD/PHYSIO1)

-------

| | | | |
| :--- | :--- | :--- | :--- |
| Status: | Active | Form: | Room |
| Managed By: | [SATELLITE](Organization-organization-satellite.md) | | |



## Resource Content

```json
{
  "resourceType" : "Location",
  "id" : "location-satellite-opd-physio1",
  "meta" : {
    "profile" : ["http://hl7.org.au/fhir/core/StructureDefinition/au-core-location"]
  },
  "identifier" : [{
    "system" : "http://example.org/fhir/sid/location",
    "value" : "SATELLITE/OPD/PHYSIO1"
  }],
  "status" : "active",
  "name" : "Physio Room 1",
  "physicalType" : {
    "coding" : [{
      "system" : "http://terminology.hl7.org/CodeSystem/location-physical-type",
      "code" : "ro",
      "display" : "Room"
    }]
  },
  "managingOrganization" : {
    "reference" : "Organization/organization-satellite",
    "display" : "SATELLITE"
  }
}

```
