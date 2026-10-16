# Patient: CHARLIE - HL7 v2 SIU to FHIR Appointment - AU Core (Proof of Concept) v0.1.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Patient: CHARLIE**

## Example Patient: Patient: CHARLIE

Profile: [AU Core Patient](http://hl7.org.au/fhir/core/2.0.0/StructureDefinition-au-core-patient.html)

CHARLIE Unknown, DoB: ( Medical record number: 900003)

-------

| | |
| :--- | :--- |
| Alt. Name: |  |



## Resource Content

```json
{
  "resourceType" : "Patient",
  "id" : "patient-900003",
  "meta" : {
    "profile" : ["http://hl7.org.au/fhir/core/StructureDefinition/au-core-patient"]
  },
  "identifier" : [{
    "type" : {
      "coding" : [{
        "system" : "http://terminology.hl7.org/CodeSystem/v2-0203",
        "code" : "MR"
      }]
    },
    "system" : "http://example.org/fhir/sid/simhosp/mrn",
    "value" : "900003",
    "assigner" : {
      "display" : "Simulated Hospital"
    }
  }],
  "name" : [{
    "text" : "CHARLIE",
    "given" : ["CHARLIE"]
  },
  {
    "extension" : [{
      "url" : "http://hl7.org/fhir/StructureDefinition/data-absent-reason",
      "valueCode" : "unknown"
    }]
  }],
  "gender" : "unknown",
  "_birthDate" : {
    "extension" : [{
      "url" : "http://hl7.org/fhir/StructureDefinition/data-absent-reason",
      "valueCode" : "unknown"
    }]
  }
}

```
