# SIU AU Appointment - HL7 v2 SIU to FHIR Appointment - AU Core (Proof of Concept) v0.1.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **SIU AU Appointment**

## Resource Profile: SIU AU Appointment 

| | |
| :--- | :--- |
| *Official URL*:http://example.org/fhir/siu2fhir-au/StructureDefinition/siu-au-appointment | *Version*:0.1.0 |
| Draft as of 2026-10-28 | *Computable Name*:SIUAUAppointment |

 
An Appointment created and maintained from HL7 v2 SIU S12, S13, S14 and S15 messages, whose participants are AU Core resources. The ingestion service rebuilds the whole resource from each message it applies. 

**Usages:**

* Examples for this Profile: [Appointment/appointment-fil2001-after-s12](Appointment-appointment-fil2001-after-s12.md), [Appointment/appointment-fil2001-after-s13](Appointment-appointment-fil2001-after-s13.md), [Appointment/appointment-fil2001-after-s14](Appointment-appointment-fil2001-after-s14.md), [Appointment/appointment-fil2001-after-s15](Appointment-appointment-fil2001-after-s15.md)... Show 2 more, [Appointment/appointment-fil2002](Appointment-appointment-fil2002.md) and [Appointment/appointment-fil2003](Appointment-appointment-fil2003.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/resource/example.fhir.siu2fhir.au|current/StructureDefinition/StructureDefinition-siu-au-appointment.json)

### Formal Views of Profile Content

 [Description of Profiles, Differentials, Snapshots and how the different presentations work](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](StructureDefinition-siu-au-appointment.csv), [Excel](StructureDefinition-siu-au-appointment.xlsx), [Schematron](StructureDefinition-siu-au-appointment.sch) 



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "siu-au-appointment",
  "url" : "http://example.org/fhir/siu2fhir-au/StructureDefinition/siu-au-appointment",
  "version" : "0.1.0",
  "name" : "SIUAUAppointment",
  "title" : "SIU AU Appointment",
  "status" : "draft",
  "date" : "2026-10-28T20:03:31+00:00",
  "publisher" : "SIU2FHIR PoC",
  "description" : "An Appointment created and maintained from HL7 v2 SIU S12, S13, S14 and S15 messages,\nwhose participants are AU Core resources. The ingestion service rebuilds the whole\nresource from each message it applies.",
  "jurisdiction" : [{
    "coding" : [{
      "system" : "urn:iso:std:iso:3166",
      "code" : "AU",
      "display" : "Australia"
    }]
  }],
  "fhirVersion" : "4.0.1",
  "mapping" : [{
    "identity" : "workflow",
    "uri" : "http://hl7.org/fhir/workflow",
    "name" : "Workflow Pattern"
  },
  {
    "identity" : "rim",
    "uri" : "http://hl7.org/v3",
    "name" : "RIM Mapping"
  },
  {
    "identity" : "ical",
    "uri" : "http://ietf.org/rfc/2445",
    "name" : "iCalendar"
  },
  {
    "identity" : "w5",
    "uri" : "http://hl7.org/fhir/fivews",
    "name" : "FiveWs Pattern Mapping"
  },
  {
    "identity" : "v2",
    "uri" : "http://hl7.org/v2",
    "name" : "HL7 v2 Mapping"
  }],
  "kind" : "resource",
  "abstract" : false,
  "type" : "Appointment",
  "baseDefinition" : "http://hl7.org/fhir/StructureDefinition/Appointment",
  "derivation" : "constraint",
  "differential" : {
    "element" : [{
      "id" : "Appointment",
      "path" : "Appointment",
      "constraint" : [{
        "key" : "siu-appt-1",
        "severity" : "error",
        "human" : "Exactly one participant references the Patient",
        "expression" : "participant.where(actor.reference.contains('Patient/')).count() = 1",
        "source" : "http://example.org/fhir/siu2fhir-au/StructureDefinition/siu-au-appointment"
      },
      {
        "key" : "siu-appt-2",
        "severity" : "error",
        "human" : "cancelationReason is only populated for cancelled appointments",
        "expression" : "cancelationReason.exists() implies status = 'cancelled'",
        "source" : "http://example.org/fhir/siu2fhir-au/StructureDefinition/siu-au-appointment"
      }]
    },
    {
      "id" : "Appointment.extension",
      "path" : "Appointment.extension",
      "slicing" : {
        "discriminator" : [{
          "type" : "value",
          "path" : "url"
        }],
        "ordered" : false,
        "rules" : "open"
      }
    },
    {
      "id" : "Appointment.extension:sourceMessageDateTime",
      "path" : "Appointment.extension",
      "sliceName" : "sourceMessageDateTime",
      "min" : 0,
      "max" : "1",
      "type" : [{
        "code" : "Extension",
        "profile" : ["http://example.org/fhir/siu2fhir-au/StructureDefinition/source-message-datetime"]
      }],
      "mustSupport" : true
    },
    {
      "id" : "Appointment.extension:sourceMessageControlId",
      "path" : "Appointment.extension",
      "sliceName" : "sourceMessageControlId",
      "min" : 0,
      "max" : "1",
      "type" : [{
        "code" : "Extension",
        "profile" : ["http://example.org/fhir/siu2fhir-au/StructureDefinition/source-message-control-id"]
      }],
      "mustSupport" : true
    },
    {
      "id" : "Appointment.identifier",
      "path" : "Appointment.identifier",
      "short" : "SCH-2 filler and/or SCH-1 placer appointment ID",
      "min" : 1,
      "mustSupport" : true
    },
    {
      "id" : "Appointment.identifier.type",
      "path" : "Appointment.identifier.type",
      "min" : 1,
      "mustSupport" : true,
      "binding" : {
        "strength" : "required",
        "valueSet" : "http://example.org/fhir/siu2fhir-au/ValueSet/appointment-identifier-type"
      }
    },
    {
      "id" : "Appointment.identifier.system",
      "path" : "Appointment.identifier.system",
      "min" : 1,
      "mustSupport" : true
    },
    {
      "id" : "Appointment.identifier.value",
      "path" : "Appointment.identifier.value",
      "min" : 1,
      "mustSupport" : true
    },
    {
      "id" : "Appointment.status",
      "path" : "Appointment.status",
      "short" : "From SCH-25 (table 0278) or the trigger event; S15 always gives cancelled",
      "mustSupport" : true
    },
    {
      "id" : "Appointment.cancelationReason",
      "path" : "Appointment.cancelationReason",
      "short" : "SCH-6 event reason, populated only when status is cancelled",
      "mustSupport" : true
    },
    {
      "id" : "Appointment.serviceType",
      "path" : "Appointment.serviceType",
      "short" : "AIS-3 universal service identifier",
      "mustSupport" : true
    },
    {
      "id" : "Appointment.appointmentType",
      "path" : "Appointment.appointmentType",
      "short" : "SCH-7 appointment reason (HL7 table 0276)",
      "mustSupport" : true
    },
    {
      "id" : "Appointment.start",
      "path" : "Appointment.start",
      "short" : "SCH-11.4, else the earliest AIS-4 / AIG-8 / AIL-6 / AIP-6",
      "mustSupport" : true
    },
    {
      "id" : "Appointment.end",
      "path" : "Appointment.end",
      "short" : "SCH-11.5, else start + SCH-9/10, else the latest resource-segment end",
      "mustSupport" : true
    },
    {
      "id" : "Appointment.minutesDuration",
      "path" : "Appointment.minutesDuration",
      "mustSupport" : true
    },
    {
      "id" : "Appointment.comment",
      "path" : "Appointment.comment",
      "short" : "NTE-3 comments, newline-separated",
      "mustSupport" : true
    },
    {
      "id" : "Appointment.participant",
      "path" : "Appointment.participant",
      "mustSupport" : true
    },
    {
      "id" : "Appointment.participant.type",
      "path" : "Appointment.participant.type",
      "mustSupport" : true
    },
    {
      "id" : "Appointment.participant.actor",
      "path" : "Appointment.participant.actor",
      "short" : "AU Core Patient (PID), Practitioner (AIP-3), Location (AIL-3); display-only for AIG and unidentified resources",
      "type" : [{
        "code" : "Reference",
        "targetProfile" : ["http://hl7.org.au/fhir/core/StructureDefinition/au-core-patient",
        "http://hl7.org.au/fhir/core/StructureDefinition/au-core-practitioner",
        "http://hl7.org.au/fhir/core/StructureDefinition/au-core-practitionerrole",
        "http://hl7.org.au/fhir/core/StructureDefinition/au-core-location"]
      }],
      "mustSupport" : true
    },
    {
      "id" : "Appointment.participant.status",
      "path" : "Appointment.participant.status",
      "mustSupport" : true
    }]
  }
}

```
