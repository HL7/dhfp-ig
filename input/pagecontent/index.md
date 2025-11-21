### Note to Readers: Introduction 

1. The Dental Health Functional Profile Package R2 includes the following parts: 

    * Overview chapter (this and following pages)

    * Dental Health Functional Profile (DHFP) – a profile of on ISO/HL7 10781 – Electronic Health Record System Functional Model (EHR-S FM), Release 2.1 as the informative document. Functions and criteria are ordered according to EHR-S FM sections and subsections.

2. The DHFP Project Team spent 16 months in analysis of the EHR-S FM Release 2.0.1 to determine which functions and criteria in the EHR-S FM pertain to dental health. After publication of the DHFP R1 in 2020, the Project Team worked until now to publish this R1.01 Errata Version. After the release for EHR-S FM Release 2.1, the project lead reviewed the document for DHFP to create this version to be in-line with the [EHR-S FM R2.1](https://build.fhir.org/ig/HL7/ehrsfm-ig/)

3. The HL7 DHFP is organized as per the Sections, Sub-Sections and Functions in the EHR-S FM, i.e.: 
    * Overview (OV) 
    * Care Provision (CP) 
    * Care Provision Support (CPS) 
    * Administrative Support (AS) 
    * Population Heath Support (POP) 
    * Record Infrastructure (RI) 
    * Trust Infrastructure (TI)

### Acknowledgements 

This project was sponsored by the Health Level Seven International, Incorporated (HL7), and the American Dental Association (ADA). A project team that focused on this Dental Health Functional Profile was formed under the HL7 Electronic Health Record Work Group (EHR WG) in cooperation with the ADA Standards program. Many thanks to all who participated in project team meetings and contributed to the analysis and development effort for the DHFP.

### Background 

#### Project Scope Statement 

The scope of this project is to develop an EHR System Dental Health Functional Profile, referred hereinafter as DHFP, by identifying functions and conformance criteria from HL7/ISO 10781, Electronic Health Record System Functional Model Release 2.1, then modifying and adding to those functions and conformance criteria where appropriate. 

The Project uses the Common HL7 tool set - FHIR implementation guide publisher based HL7 EHR Functional Model/Profile Tooling Product to develop, ballot, and publish the DHFP. 

#### Profile for US Realm 

The DHFP is targeted to the US Realm. The profile can be adopted globally as the content has no geographical limitations. 

#### Sponsors 

**HL7 International and HL7 EHR Work Group**

Founded in 1987, Health Level Seven International (HL7, www.HL7.org) is a not-for-profit healthcare standards development organization (SDO) accredited by the American National Standards Institute (ANSI). While traditionally involved in the development of messaging standards used by healthcare systems to exchange data, HL7 began to develop structured document standards related to healthcare information systems. In 2002, a newly formed HL7 EHR Special Interest Group started development of a functional model for EHR systems. Shortly thereafter, several organizations approached HL7 to develop a consensus standard to define the necessary functions for an EHR system. The EHR Special Interest Group was promoted to a full EHR Technical Committee (EHR-TC) and subsequently renamed the EHR Work Group (EHR WG). In 2004 the EHR WG published the EHR-S Functional Model (EHR-S FM) as a Draft Standard for Trial Use (DSTU). The Functional Model underwent membership level ballot in September 2006 and in January 2007, and then was approved as a full Standard in February 2007. In 2009, EHR System Functional Model Release 1.1 was jointly balloted and published by ISO TC215 and CEN TC251, being designated ISO 10781. 

In April 2014, EHR-S FM Release 2 completed HL7 balloting and was approved for publication. ISO also completed balloting and published the Standard in 2015. 

Release 2.01 is an unballoted errata release, published by HL7 in 2017. 

In April 2014, EHR-S FM Release 2.1 completed HL7 balloting and was approved for publication. ISO also completed balloting and published the Standard in 2015. 

The HL7 EHR Work Group intends that unique functional profiles be developed by subject matter experts in various care settings to inform developers, purchasers, and other stakeholders of the functional requirements of systems developed for specific domains.

**American Dental Association**

The American Dental Association (ADA, www.ada.org) is a non-profit professional association that is also accredited as a voluntary consensus standards development organization by the American National Standards Institute (ANSI). The Dental Health Functional profile was developed by subject matter expertise from ADA Standards program.

### EHR WG Co-Chairs and Facilitators

| Role  | Name | Organization | Contact |
| --- | --- | --- | --- |
| **Project Facilitator** | Dr. Aarthi Shanmugavel | American Dental Association | shanmugavela@ada.org |
| **Co-Chair** | Gary Dickinson | EHR Standards Consulting | gary.dickinson@ehr-standards.com |
| **Co-Chair** | Mark Janczewski MD, MPH | Medical Networks, LLC | mark.janczewski@gmail.com |
| **Co-Chair** | John Ritter FHL7, MSc |  | johnritter1@verizon.net |
| **Co-Chair** | Lincoln Weed |  | ldweed424@gmail.com |
| **Co-Chair, Publishing Facilitator** | Michael van der Zel BSc | UMCG | m.van.der.zel@umcg.nl |
