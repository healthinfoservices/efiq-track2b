# Artifacts Summary - HL7 v2 SIU to FHIR Appointment - AU Core (Proof of Concept) v0.1.0

* [**Table of Contents**](toc.md)
* **Artifacts Summary**

## Artifacts Summary

This page provides a list of the FHIR artifacts defined as part of this implementation guide.

### Structures: Resource Profiles 

These define constraints on FHIR resources for systems conforming to this implementation guide.

| | |
| :--- | :--- |
| [SIU AU Appointment](StructureDefinition-siu-au-appointment.md) | An Appointment created and maintained from HL7 v2 SIU S12, S13, S14 and S15 messages, whose participants are AU Core resources. The ingestion service rebuilds the whole resource from each message it applies. |

### Structures: Extension Definitions 

These define constraints on FHIR data types for systems conforming to this implementation guide.

| | |
| :--- | :--- |
| [Source Message Control ID](StructureDefinition-source-message-control-id.md) | The MSH-10 (message control ID) of the most recent HL7 v2 SIU message applied to this Appointment. Provides traceability back to the interface engine's message log. |
| [Source Message Date/Time](StructureDefinition-source-message-datetime.md) | The MSH-7 (date/time of message) of the most recent HL7 v2 SIU message applied to this Appointment. The ingestion service compares an incoming message's MSH-7 with this value and ignores messages that are older, so a delayed message cannot undo a later change. |

### Terminology: Value Sets 

These define sets of codes used by systems conforming to this implementation guide.

| | |
| :--- | :--- |
| [Appointment Identifier Type](ValueSet-appointment-identifier-type.md) | Identifier types used on SIU Appointments: filler (SCH-2) and placer (SCH-1) appointment IDs. |

### Terminology: Concept Maps 

These define transformations to convert between codes by systems conforming with this implementation guide.

| | |
| :--- | :--- |
| [HL7 v2 Administrative Sex (0001) to FHIR AdministrativeGender](ConceptMap-HL70001ToAdministrativeGender.md) | The mapping the ingestion service applies to PID-8. The A and N mappings are judgement calls. |
| [HL7 v2 Filler Status (0278) to FHIR AppointmentStatus](ConceptMap-HL70278ToAppointmentStatus.md) | The mapping the ingestion service applies to SCH-25. Blocked, Overbook and Started have no exact FHIR equivalent. |

### Example: Example Instances 

These are example instances that show what data produced and consumed by systems conforming with this implementation guide might look like.

| | |
| :--- | :--- |
| [Appointment FIL2001 (after S12)](Appointment-appointment-fil2001-after-s12.md) | Appointment FIL2001 as stored after the S12 new booking. |
| [Appointment FIL2001 (after S13)](Appointment-appointment-fil2001-after-s13.md) | Appointment FIL2001 as stored after the S13 reschedule. |
| [Appointment FIL2001 (after S14)](Appointment-appointment-fil2001-after-s14.md) | Appointment FIL2001 as stored after the S14 modification (practitioner change, note added). |
| [Appointment FIL2001 (after S15)](Appointment-appointment-fil2001-after-s15.md) | Appointment FIL2001 as stored after the S15 cancellation. |
| [Appointment FIL2002](Appointment-appointment-fil2002.md) | Appointment FIL2002 as stored booked by an S12 whose timing is only in the AIS segment. |
| [Appointment FIL2003](Appointment-appointment-fil2003.md) | Appointment FIL2003 as stored booked by an S12 with missing patient data (data-absent-reason). |
| [Location: Outpatient Clinic 1](Location-location-simhosp-opd-clinic1.md) | Simulated location created from the sample SIU messages. |
| [Location: Physio Room 1](Location-location-simhosp-opd-physio1.md) | Simulated location created from the sample SIU messages. |
| [Organization: Simulated Hospital](Organization-organization-simhosp.md) | Simulated organization created from the sample SIU messages. |
| [Patient: CHARLIE](Patient-patient-900003.md) | Simulated patient created from the sample SIU messages. |
| [Patient: MR BOB TESTPATIENT](Patient-patient-900002.md) | Simulated patient created from the sample SIU messages. |
| [Patient: MS ALICE TESTPATIENT](Patient-patient-900001.md) | Simulated patient created from the sample SIU messages. |
| [Practitioner: DR JANE SMITH](Practitioner-practitioner-8003619900004562.md) | Simulated practitioner created from the sample SIU messages. |
| [Practitioner: DR RAJ JONES](Practitioner-practitioner-2426621b.md) | Simulated practitioner created from the sample SIU messages. |

