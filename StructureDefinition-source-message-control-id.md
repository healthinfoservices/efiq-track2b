# Source Message Control ID - HL7 v2 SIU to FHIR Appointment - AU Core (Proof of Concept) v0.1.0

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Source Message Control ID**

## Extension: Source Message Control ID 

| | |
| :--- | :--- |
| *Official URL*:http://example.org/fhir/siu2fhir-au/StructureDefinition/source-message-control-id | *Version*:0.1.0 |
| Draft as of 2026-10-16 | *Computable Name*:SourceMessageControlId |

The MSH-10 (message control ID) of the most recent HL7 v2 SIU message applied to this Appointment. Provides traceability back to the interface engine's message log.

**Context of Use**

**Usage info**

**Usages:**

* Use this Extension: [SIU AU Appointment](StructureDefinition-siu-au-appointment.md)
* Examples for this Extension: [Appointment/appointment-fil2001-after-s12](Appointment-appointment-fil2001-after-s12.md), [Appointment/appointment-fil2001-after-s13](Appointment-appointment-fil2001-after-s13.md), [Appointment/appointment-fil2001-after-s14](Appointment-appointment-fil2001-after-s14.md), [Appointment/appointment-fil2001-after-s15](Appointment-appointment-fil2001-after-s15.md)... Show 2 more, [Appointment/appointment-fil2002](Appointment-appointment-fil2002.md) and [Appointment/appointment-fil2003](Appointment-appointment-fil2003.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/resource/example.fhir.siu2fhir.au|current/StructureDefinition/StructureDefinition-source-message-control-id.json)

### Formal Views of Extension Content

 [Description of Profiles, Differentials, Snapshots, and how the XML and JSON presentations work](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](StructureDefinition-source-message-control-id.csv), [Excel](StructureDefinition-source-message-control-id.xlsx), [Schematron](StructureDefinition-source-message-control-id.sch) 

#### Constraints



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "source-message-control-id",
  "url" : "http://example.org/fhir/siu2fhir-au/StructureDefinition/source-message-control-id",
  "version" : "0.1.0",
  "name" : "SourceMessageControlId",
  "title" : "Source Message Control ID",
  "status" : "draft",
  "date" : "2026-10-16T06:09:14+00:00",
  "publisher" : "SIU2FHIR PoC",
  "description" : "The MSH-10 (message control ID) of the most recent HL7 v2 SIU message applied to this\nAppointment. Provides traceability back to the interface engine's message log.",
  "jurisdiction" : [{
    "coding" : [{
      "system" : "urn:iso:std:iso:3166",
      "code" : "AU",
      "display" : "Australia"
    }]
  }],
  "fhirVersion" : "4.0.1",
  "mapping" : [{
    "identity" : "rim",
    "uri" : "http://hl7.org/v3",
    "name" : "RIM Mapping"
  }],
  "kind" : "complex-type",
  "abstract" : false,
  "context" : [{
    "type" : "element",
    "expression" : "Appointment"
  }],
  "type" : "Extension",
  "baseDefinition" : "http://hl7.org/fhir/StructureDefinition/Extension",
  "derivation" : "constraint",
  "differential" : {
    "element" : [{
      "id" : "Extension",
      "path" : "Extension",
      "short" : "Source Message Control ID",
      "definition" : "The MSH-10 (message control ID) of the most recent HL7 v2 SIU message applied to this\nAppointment. Provides traceability back to the interface engine's message log."
    },
    {
      "id" : "Extension.extension",
      "path" : "Extension.extension",
      "max" : "0"
    },
    {
      "id" : "Extension.url",
      "path" : "Extension.url",
      "fixedUri" : "http://example.org/fhir/siu2fhir-au/StructureDefinition/source-message-control-id"
    },
    {
      "id" : "Extension.value[x]",
      "path" : "Extension.value[x]",
      "min" : 1,
      "type" : [{
        "code" : "string"
      }]
    }]
  }
}

```
