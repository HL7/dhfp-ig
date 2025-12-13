### What is a Functional Profile?

The EHR-S FM is a list of all functions that COULD be present in EHR systems and criteria for achieving that function. Any given EHR-S will perform one or more functions (i.e., a subset) from the FM list (i.e., the superset), depending on the purpose of the system. The select subset of functions and the criteria for conforming to these functions characterize the EHR-S capabilities and are referred to as a “functional profile.” The functions and conformance criteria will vary across functional profiles, depending on the operational needs of the system, i.e., what the system is in place to accomplish. 

This Electronic Health Records DHFP R2 is based on the HL7® Electronic Health Record System Functional Model and Standard (EHR-S FM) Release 2.1.1, 2025. The DHFP is intended to inform software developers, users, purchasers, and other interested parties, such as payers and data aggregators, regarding the desired performance of a dental electronic health record software system, whether operating stand-alone or integrated with a medical electronic health record system. 

This document is an informative technical report and is designed to detail the “what and why” for the functions and conformance criteria for a dental electronic health record software system. The “how” regarding the manner that such functions are implemented in any particular dental electronic health record software system is left to software developers and vendors. “How” various software vendors implement the functions and conformance criteria in this DHFP will allow differentiation in the marketplace. Some specific dental comments are included as discussion in the DHFP to suggest how various EHR-S FM functions and conformance criteria might apply for the dental domain.

In 2024, the ADA published an ANSI accredited implementation guide for the DHFP R1.01 - ANSI/ADA 1108-2024 Dentistry - Implementation Guidance for the ADA/HL7® Dental Health Functional Profile. The scope of this standard is to identify the minimum performance functionality required of an electronic dental record system and to encourage the implementation of the ADA/HL7® DHFP effectively in an interoperable and coordinated care environment. 

Because the DHFP R2 adheres to the defined rules of the EHR-S FM, a dental EHR software system may claim conformance to the DHFP R2 if it meets the requirements outlined in the DHFP R2. In addition, because this DHFP R2 is based on the functions and conformance criteria of the EHR-S FM, this DHFP R2 will serve as a foundation for interoperability among dental electronic record software systems as well as between dental electronic record software systems and medical electronic record software systems.

### EHR-S Definitions and Standards

ISO/HL7® 10781 EHR-S FM references the International Organization for Standardization (ISO) 
ISO/TR-20514 Health Informatics – Electronic health record – Definition, scope and context1
and states: 

> “The primary purpose of the EHR is to provide a documented record of care that supports present and future care by the same or other clinicians…. Any other purpose for which the health record is used may be considered secondary.” 

> “The Core EHR contains principally clinical information; it is therefore chiefly focused on the primary purpose. The Core EHR is a subset of the Extended EHR. The Extended EHR includes the whole health information landscape; its focus therefore is not only on the primary purpose, but also on all of the secondary purposes as well. The Extended EHR is a superset of the Core EHR.” 

In this respect, the DHFP R2 may be regarded as a set of Extended (i.e., not Core) EHR functions.

### Systems, Components, and Applications

An EHR system consists of a collection of systems, applications, modules, or components, developed on different architectures. For example, a provider might pair one vendor's clinical documentation system with another's tracking, discharge, or prescribing system. An EHR system may be provided by a single vendor, multiple vendors, or by one or more development teams.

#### Organization of the HL7® EHR-S Functional Model

The EHR-S Functional Model is composed of a list of functions, known as the Function List, which is divided into seven sections: Overarching, Care Provision, Care Provision Support, Population Health Support, Administrative Support, Record Infrastructure, and Trust Infrastructure. 
Within the seven Sections of the Functional List the functions are grouped under header functions which each have one or more sub-functions in a hierarchical structure.

#### Sections of the Functional Model

The seven sections of the function list, shown in Figure A, reflect content of the EHR Interoperability Model, now integrated in the Functional Model, along with input from several functional profiles of the earlier versions of the Functional Model. Below is a summary description of each of the seven sections: 

1. Overarching: The Overarching Section contains functions and conformance criteria that apply to complete EHR Systems and which are typically included in all EHR-S FM compliant profiles. 
2. Care Provision: The Care Provision Section contains those functions and conformance criteria that enable direct care to a specific patient and facilitate hands-on delivery of healthcare. The functions are general and are not limited to a specific care setting and may be applied as part of an Electronic Health Record supporting healthcare clinics, hospitals, services, specialties, acute, post-acute and long-term care settings.
3. Care Provision Support: The Care Provision Support Section focuses on functions and conformance criteria supporting the provision of care. This section is organized generally in alignment with Care Provision Section. For example, CP.4 (Manage Orders) is supported directly by CPS.4 (Support Orders). 
4. Population Health Support: The Population Health Support Section focuses on functions and conformance criteria supporting the prevention and control of disease among a group of people (as opposed to the direct care of a single patient). This section includes functions to support input to systems that perform medical research, promote public health, and improve the quality of care to a population. 
5. Administrative Support: The Administrative Support Section focuses on functions and conformance criteria enabling the management of clinical practice and facilitating administrative and financial operations. This includes management of resources, workflow and communication with patients and providers as well as the management of non-clinical administrative information on patients and providers. 
6. Record Infrastructure: The Record Infrastructure Section consists of functions and conformance criteria describing how an EHR system manages an EHR record, particularly those functions vital to managing the lifecycle of EHR record entries (such as origination/retention, attestation, amendment/update, access/use, translation/transformation, transmittal/disclosure, receipt, de- identification, archive …) and record entry lifespan (persistence, indelibility, continuity, audit, encryption). RI functions are core and foundational to all other functions of the EHR-S FM (CP, CPS, POP, AS). 
7. Trust Infrastructure: The Trust Infrastructure Section consists of functions and conformance criteria common to an EHR System infrastructure, particularly those functions foundational to system operations, security, efficiency and data integrity assurance, safeguards for privacy and confidentiality, and interoperability with other systems. TI functions are core and foundational to all other functions of the EHR-S FM (CP, CPS, POP, AS, and RI). 

Each function in the HL7® EHR-S Functional Model is identified and described using a set of elements or components as detailed in the example in Table 1 below.

**Table 1: Examples of Functional Model Elements**

| ID | Type | Name | Statement | Description | Conformance Criteria |
| -- | -- | -- | -- | -- | -- |
| CP.1 | H | Manage Clinical History | Manage the patient's clinical history lists used to present summary or detailed information on patient health history. | Patient Clinical History lists are used to present succinct “snapshots” of critical health information including patient history; allergy intolerance and adverse reactions; medications; problems; strengths; immunizations; medical equipment/devices; and patient and family preferences.
| CP.1.4 | F | Manage Problem List | Create and maintain patient-specific problem lists. | A problem list may include, but is not limited to chronic conditions, diagnoses, or symptoms, injury/poisoning (both intentional and unintentional), adverse effects of medical care (e.g., drugs, surgical), functional limitations, visit or stay-specific conditions, diagnoses, or symptoms...
| CP.1.4 | C | | | | 1. The system SHALL provide the ability to manage, as discrete data, all active problems associated with a patient.
| CP.1.4 | C | | | | 2. The system SHALL capture and render a history of all problems associated with a patient.
| CP.1.4 | C | | | | 3. The system SHALL provide the ability to manage relevant dates including the onset date and resolution date of problem.
{: .grid .table-striped}

**Function ID**

This is the unique identifier of a function in the Function List (e.g., CP.1.1) and should be used to identify uniquely the function when referencing functions. The Function ID also serves to identify the section within which the function exists (CP = Care Provision Section) and the hierarchy or relationship between functions (CP.1.1 is at the same level as CP.1.2, CP.1.1 is also a parent of CP.1.1.1 and child of CP.1. In many cases the parent is fully expressed by the children. 

**Function Type**

This is an indication of the line item as being a Header (H), Function (F) or Conformance Criteria (C). The Tag (T) is used to identify a new section in the spreadsheet and its related functions in the spreadsheet. A Tag has no directly associated Functions or Criteria. 

**Function Name**

This is the name of the Function and while expected to be unique within the Function List; it is not recommended to be used to identify the Function without being accompanied by the Function ID. 
Example: CP.1.3, Manage Medication List 

**Function Statement**

This is a brief statement of the purpose of this function. While not restricted to the use of structured language that is used in the Conformance Criteria (see below), the Statement should clearly identify the purpose and scope of the function. 
Example: Create and maintain patient-specific medication lists 

**Description**

This is a more detailed description of the function, including examples if needed. 
Example: Medication lists are managed over time, whether over the course of a visit or stay, or the lifetime of a patient. All pertinent dates, including medication start, modification, and end dates are stored. The entire medication history for any medication, including alternative supplements and herbal medications, is viewable. Medication lists are not limited to medication orders recorded by providers, but may include, for example, pharmacy dispense/supply records, patient-reported medications and additional information such as age specific dosage. 

### Conformance Criteria

*Each function in the Function List includes one or more Conformance Criteria. A Conformance Criteria, which exists as normative language in this standard, defines the requirements for conforming to the function. The language used to express a conformance criterion is highly structured with standardized components with set meanings. 
Example: 1. The system SHALL provide the ability to manage, as discrete data, all active problems associated with a patient.*

#### Conformance Clause

These profiles are based on the HL7® EHR-S Functional Model Release 2.1.1, 2025. 
Key to the Functional Model and derived profiles is the concept of conformance, which is defined (by the EHR-S FM) as “verification that an implementation meets the requirements of a standard or specification”. In the Functional Model and in derived profiles, the general concept of conformance may be expressed in a number of forms. For instance, a profile can be said to conform to the Functional Model if it adheres to the defined rules specified by the Functional Model specification. Similarly, an EHR system may claim conformance to one of these profiles if it meets all the requirements outlined in the profile. 

### Conformance Criteria

Each function defined in the Functional Model or profiles is associated with specific conformance criteria, which are statements used to determine if a particular function is met (i.e., “the system SHALL capture, display and report all hearing tests associated with a patient”). Conformance criteria have been developed in accordance with the standards set forth by the EHR Work Group. In order to ensure consistent, unambiguous understanding and application of the Functional Profile, a consistent set of keywords (normative verbs) has been employed to describe conformance requirements.

The key words SHALL, SHALL NOT, SHOULD, and MAY in this document are to be interpreted as described in HL7® EHR-S Functional Model Release 2.1.1, 2025, Conformance Clause as detailed in Table 2 below.

**Table 2: Optionality key words**

| | |
| -- | -- |
| SHALL | Indicates a mandatory requirement to be followed (implemented) in order to conform. Synonymous with ‘is required to’ and ‘must’. |
| SHOULD | Indicates an optional recommended action, one that is particularly suitable, without mentioning or excluding others. Synonymous with ‘is permitted and recommended’. |
| MAY | Indicates an optional, permissible action. Synonymous with ‘is permitted’. |
{: .grid .table-striped}

### Functional Profiles

A “Functional Profile" is a selected set of functions that are applicable for a particular purpose, user, care setting, domain, etc. Functional Profiles help to manage the master list of functions. It is not anticipated that the full Functional Model will apply to any single EHR-S implementation. As such, an EHR system does not conform directly to the Functional Model; rather, it conforms to one or more Functional Profiles. See the EHR-S FM Conformance Clause for additional detail regarding how a system may claim conformance to Functional Profiles. 

Functional profiles are the expression of usable subsets of, or modifications or additions to, functions and criteria of the EHR-S Functional Model. 

The act of creating a Functional Profile is to support a business case for EHR-S use by selecting an applicable subset of functions from the EHR-S Functional Model list of functions, in effect constraining the model to meet specific requirements. For example, a Functional Profile may be created by a purchaser, to indicate requirements; by a vendor, to indicate the capability of specific products; or by any person/entity wishing to stipulate a desired subset of functions for a particular purpose, including a care setting within a specific realm.

### Normative Language

Additional clarification is necessary to understand the standardized nomenclature used to describe the actions performed by a system. The excerpt in Table 3, which is from the EHR-S FM R2 Glossary, illustrates the hierarchical nature of the nomenclature. For example, the term “Capture” is used to describe a function that includes both direct data entry (“Enter”) and indirect data entry (e.g., “Import” from another system). Similarly, “Maintain” is used to describe a function that entails storing, updating, and/or removing data.

**Table 3: "Manage Data" Action-Verbs**

<table class="grid">
<colgroup>
<col style="width: 9%" />
<col style="width: 8%" />
<col style="width: 10%" />
<col style="width: 8%" />
<col style="width: 7%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 11%" />
<col style="width: 8%" />
<col style="width: 7%" />
<col style="width: 9%" />
</colgroup>
<thead>
<tr class="header">
<th colspan="11">Manage (Data)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Capture</td>
<td colspan="3">Maintain</td>
<td colspan="3">Render</td>
<td>Exchange</td>
<td colspan="2">Determine</td>
<td>Manage Data Visibility</td>
</tr>
<tr class="even">
<td rowspan="2">Auto-populate<br/>
Enter<br/>
Import<br/>
Receive<br/></td>
<td>Store</td>
<td>Update</td>
<td>Remove</td>
<td rowspan="2">Extract</td>
<td rowspan="2">Present</td>
<td rowspan="2">Transmit</td>
<td rowspan="2">Export<br/>
Import<br/>
Receive<br/>
Transmit<br/></td>
<td rowspan="2">Analyze</td>
<td rowspan="2">Decide</td>
<td rowspan="2">De-Identify/<br/>
Re-Identify<br/>
Hide/<br/>
Unhide<br/>
Mask/<br/>
Unmask<br/></td>
</tr>
<tr class="odd">
<td>Archive<br/>
Backup<br/>
Decrypt<br/>
Encrypt<br/>
Recover<br/>
Restore<br/>
Save<br/></td>
<td>Annotate<br/>
Attest<br/>
Edit<br/>
Harmonize<br/>
Integrate<br/>
Link/Unlink<br/>
Tag/Untag<br/></td>
<td>Delete<br/>
Purge<br/></td>
</tr>
</tbody>
</table>