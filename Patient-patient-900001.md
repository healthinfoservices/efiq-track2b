# Patient: MS ALICE TESTPATIENT - HL7 v2 SIU to FHIR Appointment - AU Core (Proof of Concept) v0.1.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Patient: MS ALICE TESTPATIENT**

## Example Patient: Patient: MS ALICE TESTPATIENT

Profile: [AU Core Patient](http://hl7.org.au/fhir/core/2.0.0/StructureDefinition-au-core-patient.html)

MS ALICE TESTPATIENT(official) Female, DoB: 1980-01-01 ( Medical record number: 900001)

-------

| | |
| :--- | :--- |
| Other Ids: | * IHI/8003609900001239
* Medicare Number/29999999991
 |
| Contact Detail | * ph: 00 00000000(Home)
* [alice@example.org](mailto:alice@example.org)
* 1 Example Street, BRISBANE, QLD 4000
 |
| Language: | English |
| [Australian Indigenous Status](http://hl7.org.au/fhir/6.0.0/StructureDefinition-indigenous-status.html) | australian-indigenous-status-1: 4 (4) |



## Resource Content

```json
{
  "resourceType" : "Patient",
  "id" : "patient-900001",
  "meta" : {
    "profile" : ["http://hl7.org.au/fhir/core/StructureDefinition/au-core-patient"]
  },
  "extension" : [{
    "url" : "http://hl7.org.au/fhir/StructureDefinition/indigenous-status",
    "valueCoding" : {
      "system" : "https://healthterminologies.gov.au/fhir/CodeSystem/australian-indigenous-status-1",
      "code" : "4"
    }
  }],
  "identifier" : [{
    "type" : {
      "coding" : [{
        "system" : "http://terminology.hl7.org/CodeSystem/v2-0203",
        "code" : "MR"
      }]
    },
    "system" : "http://example.org/fhir/sid/mrn/SIMHOSP",
    "value" : "900001"
  },
  {
    "type" : {
      "coding" : [{
        "system" : "http://terminology.hl7.org/CodeSystem/v2-0203",
        "code" : "NI"
      }],
      "text" : "IHI"
    },
    "system" : "http://ns.electronichealth.net.au/id/hi/ihi/1.0",
    "value" : "8003609900001239"
  },
  {
    "type" : {
      "coding" : [{
        "system" : "http://terminology.hl7.org/CodeSystem/v2-0203",
        "code" : "MC"
      }],
      "text" : "Medicare Number"
    },
    "system" : "http://ns.electronichealth.net.au/id/medicare-number",
    "value" : "29999999991"
  }],
  "name" : [{
    "use" : "official",
    "text" : "MS ALICE TESTPATIENT",
    "family" : "TESTPATIENT",
    "given" : ["ALICE"],
    "prefix" : ["MS"]
  }],
  "telecom" : [{
    "system" : "phone",
    "value" : "00 00000000",
    "use" : "home"
  },
  {
    "system" : "email",
    "value" : "alice@example.org",
    "use" : "home"
  }],
  "gender" : "female",
  "birthDate" : "1980-01-01",
  "address" : [{
    "text" : "1 Example Street, BRISBANE, QLD 4000",
    "line" : ["1 Example Street"],
    "city" : "BRISBANE",
    "state" : "QLD",
    "postalCode" : "4000",
    "country" : "AU"
  }],
  "communication" : [{
    "language" : {
      "coding" : [{
        "system" : "urn:ietf:bcp:47",
        "code" : "en"
      }],
      "text" : "English"
    }
  }]
}

```
