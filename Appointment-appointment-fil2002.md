# Appointment FIL2002 - HL7 v2 SIU to FHIR Appointment - AU Core (Proof of Concept) v0.1.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Appointment FIL2002**

## Example Appointment: Appointment FIL2002

Profile: [SIU AU Appointment](StructureDefinition-siu-au-appointment.md)

**Source Message Date/Time**: 2026-10-07 09:40:00+1000

**Source Message Control ID**: MSG0005

**identifier**: Filler Identifier/FIL2002, Placer Identifier/PLC1002

**status**: Booked

**serviceType**: Physiotherapy

**appointmentType**: Routine

**start**: 2026-10-16 14:00:00+1000

**end**: 2026-10-16 14:45:00+1000

**minutesDuration**: 45

> **participant****actor**: [BOB TESTPATIENT](Patient-patient-900002.md)**required**: Required**status**: Accepted

> **participant****actor**: [Physio Room 1](Location-location-simhosp-opd-physio1.md)**status**: Accepted



## Resource Content

```json
{
  "resourceType" : "Appointment",
  "id" : "appointment-fil2002",
  "meta" : {
    "profile" : ["http://example.org/fhir/siu2fhir-au/StructureDefinition/siu-au-appointment"]
  },
  "extension" : [{
    "url" : "http://example.org/fhir/siu2fhir-au/StructureDefinition/source-message-datetime",
    "valueDateTime" : "2026-10-07T09:40:00+10:00"
  },
  {
    "url" : "http://example.org/fhir/siu2fhir-au/StructureDefinition/source-message-control-id",
    "valueString" : "MSG0005"
  }],
  "identifier" : [{
    "type" : {
      "coding" : [{
        "system" : "http://terminology.hl7.org/CodeSystem/v2-0203",
        "code" : "FILL"
      }]
    },
    "system" : "http://example.org/fhir/sid/appointment/filler/SCHED",
    "value" : "FIL2002"
  },
  {
    "type" : {
      "coding" : [{
        "system" : "http://terminology.hl7.org/CodeSystem/v2-0203",
        "code" : "PLAC"
      }]
    },
    "system" : "http://example.org/fhir/sid/appointment/placer/PAS",
    "value" : "PLC1002"
  }],
  "status" : "booked",
  "serviceType" : [{
    "coding" : [{
      "system" : "http://example.org/fhir/CodeSystem/v2-local/LOCAL",
      "code" : "PHYSIO",
      "display" : "Physiotherapy"
    }],
    "text" : "Physiotherapy"
  }],
  "appointmentType" : {
    "coding" : [{
      "system" : "http://terminology.hl7.org/CodeSystem/v2-0276",
      "code" : "ROUTINE",
      "display" : "Routine"
    }],
    "text" : "Routine"
  },
  "start" : "2026-10-16T14:00:00+10:00",
  "end" : "2026-10-16T14:45:00+10:00",
  "minutesDuration" : 45,
  "participant" : [{
    "actor" : {
      "reference" : "Patient/patient-900002",
      "display" : "BOB TESTPATIENT"
    },
    "required" : "required",
    "status" : "accepted"
  },
  {
    "actor" : {
      "reference" : "Location/location-simhosp-opd-physio1",
      "display" : "Physio Room 1"
    },
    "status" : "accepted"
  }]
}

```
