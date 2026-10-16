# Patient: MR BOB TESTPATIENT - HL7 v2 SIU to FHIR Appointment - AU Core (Proof of Concept) v0.1.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Patient: MR BOB TESTPATIENT**

## Example Patient: Patient: MR BOB TESTPATIENT

Profile: [AU Core Patient](http://hl7.org.au/fhir/core/2.0.0/StructureDefinition-au-core-patient.html)

MR BOB TESTPATIENT(official) Male, DoB: 1975-12-31 ( Medical record number: 900002)

-------



## Resource Content

```json
{
  "resourceType" : "Patient",
  "id" : "patient-900002",
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
    "value" : "900002",
    "assigner" : {
      "display" : "Simulated Hospital"
    }
  }],
  "name" : [{
    "use" : "official",
    "text" : "MR BOB TESTPATIENT",
    "family" : "TESTPATIENT",
    "given" : ["BOB"],
    "prefix" : ["MR"]
  }],
  "gender" : "male",
  "birthDate" : "1975-12-31"
}

```
