# Organization: SATELLITE - HL7 v2 SIU to FHIR Appointment - AU Core (Proof of Concept) v0.1.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Organization: SATELLITE**

## Example Organization: Organization: SATELLITE

Profile: [AU Core Organization](http://hl7.org.au/fhir/core/2.0.0/StructureDefinition-au-core-organization.html)

Tag: [Placeholder created from an SIU message - needs curation (Details: SIU2FHIR Resource Tags code placeholder = 'Placeholder created from an SIU message - needs curation')](CodeSystem-siu2fhir-tag.md)

SATELLITE (http://example.org/fhir/sid/organization#SATELLITE)

-------

| | |
| :--- | :--- |
| Active: | true |



## Resource Content

```json
{
  "resourceType" : "Organization",
  "id" : "organization-satellite",
  "meta" : {
    "profile" : ["http://hl7.org.au/fhir/core/StructureDefinition/au-core-organization"],
    "tag" : [{
      "system" : "http://example.org/fhir/siu2fhir-au/CodeSystem/siu2fhir-tag",
      "code" : "placeholder",
      "display" : "Placeholder created from an SIU message - needs curation"
    }]
  },
  "identifier" : [{
    "system" : "http://example.org/fhir/sid/organization",
    "value" : "SATELLITE"
  }],
  "active" : true,
  "name" : "SATELLITE"
}

```
