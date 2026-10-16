# Appointment FIL2001 (after S14) - HL7 v2 SIU to FHIR Appointment - AU Core (Proof of Concept) v0.1.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Appointment FIL2001 (after S14)**

## Example Appointment: Appointment FIL2001 (after S14)

Profile: [SIU AU Appointment](StructureDefinition-siu-au-appointment.md)

**Source Message Date/Time**: 2026-10-07 09:20:00+1000

**Source Message Control ID**: MSG0003

**identifier**: Filler Identifier/FIL2001, Placer Identifier/PLC1001

**status**: Booked

**serviceType**: General consultation

**appointmentType**: Follow-up

**start**: 2026-10-15 11:00:00+1000

**end**: 2026-10-15 11:30:00+1000

**minutesDuration**: 30

**comment**: Interpreter required (Mandarin)

> **participant****actor**: [ALICE TESTPATIENT](Patient-patient-900001.md)**required**: Required**status**: Accepted

> **participant****type**: Attending**actor**: [DR RAJ JONES](Practitioner-practitioner-2426621b.md)**status**: Accepted

> **participant****actor**: [Outpatient Clinic 1](Location-location-simhosp-opd-clinic1.md)**status**: Accepted



## Resource Content

```json
{
  "resourceType" : "Appointment",
  "id" : "appointment-fil2001-after-s14",
  "meta" : {
    "profile" : ["http://example.org/fhir/siu2fhir-au/StructureDefinition/siu-au-appointment"]
  },
  "extension" : [{
    "url" : "http://example.org/fhir/siu2fhir-au/StructureDefinition/source-message-datetime",
    "valueDateTime" : "2026-10-07T09:20:00+10:00"
  },
  {
    "url" : "http://example.org/fhir/siu2fhir-au/StructureDefinition/source-message-control-id",
    "valueString" : "MSG0003"
  }],
  "identifier" : [{
    "type" : {
      "coding" : [{
        "system" : "http://terminology.hl7.org/CodeSystem/v2-0203",
        "code" : "FILL"
      }]
    },
    "system" : "http://example.org/fhir/sid/appointment/filler/SCHED",
    "value" : "FIL2001"
  },
  {
    "type" : {
      "coding" : [{
        "system" : "http://terminology.hl7.org/CodeSystem/v2-0203",
        "code" : "PLAC"
      }]
    },
    "system" : "http://example.org/fhir/sid/appointment/placer/PAS",
    "value" : "PLC1001"
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
  "appointmentType" : {
    "coding" : [{
      "system" : "http://terminology.hl7.org/CodeSystem/v2-0276",
      "code" : "FOLLOWUP",
      "display" : "Follow-up"
    }],
    "text" : "Follow-up"
  },
  "start" : "2026-10-15T11:00:00+10:00",
  "end" : "2026-10-15T11:30:00+10:00",
  "minutesDuration" : 30,
  "comment" : "Interpreter required (Mandarin)",
  "participant" : [{
    "actor" : {
      "reference" : "Patient/patient-900001",
      "display" : "ALICE TESTPATIENT"
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
      "reference" : "Practitioner/practitioner-2426621b",
      "display" : "DR RAJ JONES"
    },
    "status" : "accepted"
  },
  {
    "actor" : {
      "reference" : "Location/location-simhosp-opd-clinic1",
      "display" : "Outpatient Clinic 1"
    },
    "status" : "accepted"
  }]
}

```
