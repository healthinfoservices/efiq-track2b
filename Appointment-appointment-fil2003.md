# Appointment FIL2003 - HL7 v2 SIU to FHIR Appointment - AU Core (Proof of Concept) v0.1.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Appointment FIL2003**

## Example Appointment: Appointment FIL2003

Profile: [SIU AU Appointment](StructureDefinition-siu-au-appointment.md)

**Source Message Date/Time**: 2026-10-07 09:50:00+1000

**Source Message Control ID**: MSG0006

**identifier**: Filler Identifier/FIL2003, Placer Identifier/PLC1003

**status**: Booked

**serviceType**: General consultation

**start**: 2026-10-17 09:00:00+1000

**end**: 2026-10-17 09:15:00+1000

**minutesDuration**: 15

> **participant****actor**: [CHARLIE](Patient-patient-900003.md)**required**: Required**status**: Accepted

> **participant****type**: Attending**actor**: ANON**status**: Accepted



## Resource Content

```json
{
  "resourceType" : "Appointment",
  "id" : "appointment-fil2003",
  "meta" : {
    "profile" : ["http://example.org/fhir/siu2fhir-au/StructureDefinition/siu-au-appointment"]
  },
  "extension" : [{
    "url" : "http://example.org/fhir/siu2fhir-au/StructureDefinition/source-message-datetime",
    "valueDateTime" : "2026-10-07T09:50:00+10:00"
  },
  {
    "url" : "http://example.org/fhir/siu2fhir-au/StructureDefinition/source-message-control-id",
    "valueString" : "MSG0006"
  }],
  "identifier" : [{
    "type" : {
      "coding" : [{
        "system" : "http://terminology.hl7.org/CodeSystem/v2-0203",
        "code" : "FILL"
      }]
    },
    "system" : "http://example.org/fhir/sid/appointment/filler/SCHED",
    "value" : "FIL2003"
  },
  {
    "type" : {
      "coding" : [{
        "system" : "http://terminology.hl7.org/CodeSystem/v2-0203",
        "code" : "PLAC"
      }]
    },
    "system" : "http://example.org/fhir/sid/appointment/placer/PAS",
    "value" : "PLC1003"
  }],
  "status" : "booked",
  "serviceType" : [{
    "coding" : [{
      "system" : "http://example.org/fhir/CodeSystem/v2-local/LOCAL",
      "code" : "GPCONS",
      "display" : "General consultation"
    }],
    "text" : "General consultation"
  }],
  "start" : "2026-10-17T09:00:00+10:00",
  "end" : "2026-10-17T09:15:00+10:00",
  "minutesDuration" : 15,
  "participant" : [{
    "actor" : {
      "reference" : "Patient/patient-900003",
      "display" : "CHARLIE"
    },
    "required" : "required",
    "status" : "accepted"
  },
  {
    "type" : [{
      "coding" : [{
        "system" : "http://terminology.hl7.org/CodeSystem/v3-ParticipationType",
        "code" : "ATND"
      }],
      "text" : "Attending"
    }],
    "actor" : {
      "display" : "ANON"
    },
    "status" : "accepted"
  }]
}

```
