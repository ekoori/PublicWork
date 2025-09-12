# 📓Doc Audit/Review



## Executive Summary

UGL TCS currently uses AS15288 based life-cycle. At the moment UGL Engineering Framework Procedure seems to be the parent document for the complete project/product delivery process.

Each project tailors a set of plans which which dictate the execution of a specific project - DEMP, SEMP.

This report recommends that it would be of great value for TCS team to apply Basic Integrity requirements based on EN50128 in its software development processes. Even if the decision is not to advertise it externally.

Both standards AS15288 and EN05128 are compatible. Clients and EN50128 standard have more stringent requirements in areas of software quality, safety and life-cycle, and have rail industry in mind:
- quality planning and targets
- configuration management ( Framework Procedure quotes AS ISO 10007-2003 Quality Management Systems – Guidelines as requirement)
- manage safety / safety assurance, product safety 
- manage stakeholder needs
- manage interfaces, 
- manage changes, 
- manage verification validation, software changes (and V&V of the changes)
- handing over the system to the client with clear SRACs
- traceability issues

Problems are stemming out from the fact that processes related to "Organisation Project-Enabling Processes" as required in AS15288 (and UGL Engineering Framework) have not been implemented. (Life-cycle management process, infrastructure management process, portfolio management process, quality management process, etc.) 

EN50128 outlines specific (detailed) standards for most of the aforementioned processes, making it a logical choice for adoption across various projects.

Currently, the requirements for these processes vary inconsistently from one project to another and are often customised based on the client and the individuals involved. This lack of uniformity leads to confusion, disarray, and overall inefficiency in work, resulting in frustration among engineers.
Certain parts of the processes seem to be established due to specific templates being defined and/or established team practice, but the requirements don't seem to be traceable to their source (other then project requirements, client procedures).
Clients are railway operators which formally cite 15288 as a head standard, but loosely implement CENELEC EN5012X. Oftentimes they are seem not to be aware of where their requests are coming from, e.g. have requests based on "safety assurance requirements" not being aware of their originator (EN50129).

It would make sense to standardise one way of working to avoid mentioned issues, and the set of CENELEC standards makes perfect sense to be implemented. Current processes and clients expectations converge in CENELEC standards. It would be beneficial for clients and the team to have a clear standard and set of requirements against which system and process can be evaluated. The aimed/standardised quality objectives to be achieved can then be advertised as part of the product/brand so expectations could be managed in easier way and there would be a buy in from project delivery team. This doesn't seem to be the case at the moment.

There are certain difficulties expected in the implementation of the EN50128 standard. Due to legacy nature of its core system - SigView basic integrity can be reached only SFAIRP.

Additionally, EN50128 defines specific requirements for categories that are applicable for TCS - generic software (COTS software) application data, tools, components.  I.e. this railway standard is actually relevant to TCS.

Basic Integrity (or SIL0) set of requirements define requirements that are almost entirely achievable. 

If UGL TCS advertises a certain standard (i.e. EN50128 SIL0) to the clients we would have a buy-in from the project delivery team too and would align quality processes with internal and client expectations.

This is beneficial whether TCS implements any safety-related function or not. From below statements you can see that both low demand safety-related functions and non-safety-related functions should aim for  SIL 0. 

- "*4.3 The required software safety integrity level shall be decided and assessed at system level, on the basis of the system safety integrity level and the level of risk associated with the use of the software in the system.*"
- *"4.4 At least the SIL 0 requirements of this European Standard shall be fulfilled for the software part of functions that have a safety impact below SIL 1. This is because uncertainty is present in the evaluation of the risk, and even in the identification of hazards. In the face of uncertainty it is prudent to aim for a low level of safety integrity, represented by SIL 0, rather than none."*
- "*3.1.2 Basic integrity (definition from 50129) - integrity attribute for safety-related functions with a Tolerable Function Failure Rate (TFFR) higher than (less demanding) \(10^{-5} h^{-1}\), or for non-safety-related functions. Note: In this document, Basic Integrity requirements relate only to safety-related functions. If a non-safety-related function has been given basic-integrity requirements on the basis of the process described in EN 50126-2:2017, no additional requirements are defined in this document.*"

Context is important (citation from 50128): "*It is within the scope of EN 50126-1 and EN 50129 to define the process of specifying the safety functions allocated to software.*"

Engineering Framework defines review milestones which are compatible with the railway industry. These are not specifically required in CENELEC, but can be used from standard's perspective.

## Introduction

### Context

In response to persistent issues with documentation and inconsistencies in project delivery—including the suspected loss of the CRN project due to inadequate SA-related software implementation—an internal audit was deemed necessary. This audit aims to evaluate the available documentation and adherence to established company-wide processes.

The necessity to drive the delivery of quality documentation by project demands has led to compromises in the consistency and overall quality of internal products. This is further exacerbated by the rapid expansion of the TCS team, which has been taking on multiple projects without a unified approach to documentation or product processes.

Notably, the Sydney team appears primarily project-focused without standardised product processes in place. Additionally, the transition of a lead engineer, who previously acted as the product owner, to another position within the company has created a gap in leadership and continuity.

To address these shortcomings, it is advisable to establish a dedicated standard or set of standards, and a dedicated role or team responsible for overseeing documentation standards and compliance across all projects. Implementing a centralised TCS documentation system could also improve consistency and traceability, preventing future losses and enhancing project delivery. 

Further, training sessions on selected set of standards and related requirements should be conducted to align all team members with the updated processes and quality expectations.


### Objectives

1. **Gap Identification:** Identify discrepancies between the UGL Engineering Framework and the documentation produced by the TCS team across various projects. This involves a thorough analysis of all documentation impacting TCS team workflows and life-cycle processes, including technical management and process enabling documentation. This objective also includes an examination of product documentation for additional insights.
2. **Root Cause Analysis:** Ascertain the primary reasons for the TCS team's non-compliance with the framework to address systemic issues effectively.
3. **Practice Comparison:** Evaluate the existing practices based on the AS15288 standard and assess the potential advantages of implementing the EN50128 SIL 0 requirements into the TCS life-cycle.
4. **Life-cycle Optimisation:** Recommend an ideal life-cycle model and identify suitable templates to support this life-cycle, and list actionable items to implement the same.

### Scope

This audit encompasses a thorough analysis of the following documents and processes:
- **Documents Analysed:**
  - Project-specific documentation from the Original RRL, UMA, and CRN projects, which are integral to the TCS workflow.
  - GGS documents, including procedures and templates derived from the AS15288 standard.
  - A selection of documents identified as "good examples" from various projects, which serve as benchmarks for high-quality documentation practices.

- **Processes Evaluated:**
  - The UGL Engineering framework, which is based on the AS15288 standard, forms the foundational process structure for this analysis.
  - Comparisons were made with the EN50128 SIL 0 requirements to identify gaps and potential enhancements.
  - Main software delivery procedures from MTM and V/Line projects were reviewed to assess alignment and compliance with the overarching engineering framework.

- Stakeholder Feedback:
	- TCS team members were interviewed for effectiveness, usability, and compliance of the processes and documentation in real-world applications.
	- Analysis of historical audit outcome (for CRN project) that provided a longitudinal perspective on improvements or persistent challenges within these areas.

## Methodology

The methodology applied in this audit systematically evaluates the adherence to and the effectiveness of documentation and processes within the TCS framework. This structured approach is aimed at identifying key areas for improvement and ensuring alignment with industry standards. Here's an overview of the methodology used for this audit:
- **Document Analysis:** Review and categorisation of available project documentation relevant to TCS workflows was conducted. The quality of information was assessed and classified into three levels based mainly on the subjective completeness and clarity of the information. It's noteworthy that identifying gaps against a "UGL standard" posed challenges due to the lack of detailed specifications for TCS activities in central documents. Therefore, the primary reference points were the System Engineering Management Plans (SEMP) and the Design Engineering Management Plans (DEMP) of each project.
- **Comparative Document Analysis:** We conducted a side-by-side comparison of document types across different projects to identify the most prevalent practices. Special attention was given to the adherence to the TCS V-model, which is promoted based on the Engineering Framework Procedure (AS15288). Our findings suggest a lack of complete adherence to this model across projects, with no clear evidence of compliance audits.
- **Template Utilisation:** The audit reviewed the availability and applicability of templates from the Group Governance System (GGS) for UGL engineering processes, noting where they could potentially align with TCS activities. This included examining specific templates like the 50128 verification report templates and software quality assurance plans.
- **Stakeholder Interviews:** Interviews were conducted with several team members, focusing on the gaps found in processes and the lack of available documents. This also included discussions about team concerns and suggestions for best practices, aiming to incorporate practical insights from team members into the audit findings.
- **Documentation of Findings:** All findings from document analyses, comparisons, and interviews were comprehensively documented in this report. Each identified issue or gap was detailed, providing a foundation for the recommended actions.
- **Standards Comparison:** A detailed comparison between the AS15288 and EN50128 standards was performed. This focused on highlighting the differences and how additional efforts required by EN50128 could benefit the UGL/TCS team in the long term.
- **Actionable Recommendations:** Based on the findings, SMART (Specific, Measurable, Achievable, Relevant, Time-bound) actions were proposed. These recommendations are designed to address the identified gaps and enhance overall compliance and efficiency within the TCS framework.




## Findings

### Overview of Issues
The primary challenge appears to stem from the TCS team's rapid growth and relative immaturity. Consequently, several organisational enabling processes, such as life-cycle models, knowledge management, and quality management, remain under-defined. This situation leads to difficulties in adhering to the systematic rules set forth by the ISO/IEC/IEEE 15288 standard. The lack of defined standards (ISO/IEC/IEEE 15288, 6.2.1.1), which requires the definition, maintenance, and assurance of life cycle models and policies, introduces ambiguities across processes. Additional complexities arise from a general lack of buy-in regarding internal processes and product quality by the project delivery teams.

According to ISO/IEC/IEEE 15288 (6.2.1.1), the primary purpose of the Life Cycle Model Management process is to define and maintain life cycle models and policies that are accessible and usable by the organisation. It also ensures that organisational policies and procedures for managing life cycle models are established, with clearly defined responsibilities and accountability (ISO/IEC/IEEE 15288, 6.2.1.2). This standard mandates that life cycle models used by an organisation must be regularly assessed and improved, based on prioritised needs (ISO/IEC/IEEE 15288, 6.2.1.3).

It is important to consider the scale of life cycle implementation within projects, which depends on work complexity, utilised methods, and the skills of the involved personnel (ISO/IEC/IEEE 15288, Note in 6.2.1.3). Each project should tailor these policies and models to fit its specific requirements while aligning with overarching regulations and organisational policies, as elaborated in Annex A of the standard.


Additionally, it would be worthwhile to go through the MTM/VLine standards because often (always) we have to comply with them:

- MTM Procedures:
	- L1-CHE-MAN-001 Engineering Management System (EMS) Methodology: requires IEC12207 for software development, and EN50128 when SIL3 or 4 may be applicable.
- V/Line standards: NIPR-2695 Design Management Procedure
	- *The requirement of V/Line is that the systems safety program must comply with the requirements of V/Line processes and standards and EN 50126:2017 and the supporting standards EN 50 128/9 as appropriate.*



### UGL Framework Adherence
- **Documentation and Process Quality:** High-quality SEMP and DEMP are normally produced for projects, although they often lack detailed coverage of software quality standards necessary for clear client communication. The Engineering Framework Procedure highlights review stages and refers to various standards, such as AS ISO 10007 for Configuration Management, emphasising the need for adaptability based on project complexity and risk. None of the above detail internal processes to a sufficient level to guide the team without ambiguities.

### Product Ownership
- **Lack of Formal Ownership:** System ownership parts are undocumented, leading to internal confusion. Formalising responsibilities through a clear product development procedure and a RACI (Responsible, Accountable, Consulted, Informed) matrix is essential to establish clear processes.
### Product Documentation
- **Documentation Deficits:** There is a noticeable lack of comprehensive documentation on internal software architecture and other product-related documentation. This gap is particularly evident in tools used to generate final executable codes and configurations.
- SigView software architecture documentation is not standardise, so projects and new components created for projects cannot build on top of it. This creates issues of lack of traceability and non defined (internal) interfaces.
### Centralised Documentation
- **Efforts and Challenges:** There is a low-priority ongoing effort to centralise templates related to projects and products based on "best practices" and lessons learned. However, there lacks a clear and enforceable standard, meaning projects can still override the internal process, which does not address the root cause or ensure long-term resolution.
### Project and Design Documentation
- **Centralisation Needs:** Smaller projects often lack a centralised TCS Design Document, making design history tracking challenging.
- Establishing a centralised document register for projects and internal product documentation and templates is recommended to further alleviate this issue.


### Quality Management
- **Need for Clear Goals:** Establishing clear, quantifiable quality objectives is crucial for maintaining and enhancing product and process integrity.

### Safety Assurance Process
- **Current Practices:** The Safety Assurance process and review gates generally align with client requirements and reflect practices loosely based on EN50129 and commonly on EN50126 as documented in RAMS. However, the explicit specifications of EN50129 are rarely noted, leading to potential oversight in safety oversight compliance.


### Systems Engineering
- **Visibility of Software Architecture:** System breakdown structures are commonly in place, though software architecture documentation is absent except in complex systems like those seen in the CRN project.

### Configuration Management
- **Inconsistencies and Tool Utilisation:** Configuration and change management practices vary significantly and are dependent on the engineering manager. Standardising tools such as Mantis for managing software deliverables could enhance consistency across projects.

### Requirements Management
- **Standardisation of Requirements Storage:** While project-specific requirements are tracked, there’s a lack of continuity for product-related requirements, necessitating redundancy in requirement definition for each new project. Implementing a unified, version-controlled system for storing requirements would improve efficiency and reusability.

### Change and Agile Project Management
- **Formalising Change Management:** Project-level definitions for change management exist, but the details, especially in software changes and Mantis/SVN workflows, are often too general and lead to inefficiencies. Formalising these processes in the "TCS SW Development Procedure" is crucial.
- **Agile Implementation:** Adopting agile methodologies for parts of software delivery dependent on user feedback could increase responsiveness and project success.





### Life-cycle and Process Verification
- **Verification Gaps:** Current practices only verify design document submissions and initial phase gates (A-F), assuming audits may occur post-issue identification. Establishing proactive verification processes could prevent issues before they arise, enhancing overall project delivery and compliance.

### Lack of training / Knowledge Management
- **Enhanced Training and Induction Programs:** Develop tailored training modules for new and existing staff to bridge knowledge gaps, particularly in understanding and applying standards like AS15288 and EN50128.

### Process Improvement
- **Periodic Review and Audit Schedules:** Introduce regular audit schedules to proactively measure compliance and effectiveness of the documentation and processes, ensuring continual improvement.
- **Feedback Mechanisms:** Implement structured feedback loops from end-users and stakeholders to continuously refine processes and documentation according to practical needs and challenges.



## Comparative Analysis

Both project-wide activities and internal (or product-wide) activities and outcomes have been assessed against the two standards. For each area (project/internal), the assessment includes three columns:
- **Current Practice**: Describes the highlights of our current practices, including findings from existing audits (as these reflect the outcomes of our current practices) and observations made during this audit.
- **Actions (Compliance / Recommended)**: Lists non-conformances and recommended improvements to close the gap with ISO/IEC/IEEE 15288.
- **Additional Actions for 50128 Compliance**: Specifies additional actions required to comply with EN 50128, categorised as RI (Recommended Improvement) or NCR (Non-Conformance Resolution, which must be implemented to be compliant).

#### Summary of Finding Classification:
- **Effective (E)**: An area which conforms to specified requirements and is effectively implemented. No action required.
- **Non-Conformance (NCR)**: Failure to fulfil a specified requirement. Requirements may be defined within a standard, specification, process, or procedure.
- **Recommended Improvement (RI)**: A documented statement identifying areas of improvement.
- **Observation (O)**: An item of note not requiring specific attention.





Identify Gaps: Determine where current practices fall short of the requirements and recommendations of ISO/IEC/IEEE 15288 and BS EN 50128.

Align Processes: Ensure that both project delivery and internal product development processes align with industry standards.

Enhance Documentation: Improve the consistency and comprehensiveness of documentation practices across all lifecycle stages.

Improve Quality and Compliance: Implement actions to meet the safety, quality, and performance requirements specified by both standards.

Standardize Practices: Establish clear, standardized procedures for lifecycle management, acquisition, supply, and use of tools and languages.

Support Continuous Improvement: Create a framework for ongoing monitoring, control, and improvement of processes.

Facilitate Certification: Prepare the organization for potential certification by complying with both ISO/IEC/IEEE 15288 and BS EN 50128.

Mitigate Risks: Identify and address potential risks associated with acquisition, supply, and lifecycle management processes.

Ensure Traceability: Maintain comprehensive documentation to ensure traceability and accountability throughout the project and product lifecycles.

Drive Efficiency: Enhance the efficiency and effectiveness of both project delivery and internal product development by adopting best practices.




All involved personnel should be trained against EN50128 (and 129 for context)
Independence of roles would be easily achievable for SIL0 based on current team structure. Modification of documentation and implementation in SQMP would be required to clearly distinguish those roles.

Two different sets of documents need to be distinguished: project and product process related.
Application and configuration data.......

Project - lifecycle of the work

Comparing 50128 and 15288 requirements:
- [[./AS15288 Summary|AS15288 Summary]]
- 15288 is aware of existence of "*Critical quality characteristics commonly include those related to health, safety, security assurance, reliability, availability and supportability*", but talks of them only on the high level in terms of managing the requirements and applying them on the lifecycle - it doesn't go into the specifics of any of the standard or specific industry


UGL Framework Procedure:
- is also high level
- compliance is claimed by projects adhering to  Project specific Plans.
- configuration management - asks for AS/ISO 10007 QMS compliance
- safety - legislative requirements
- V&V - satisfy necessary stakeholder and regulatory requirements






### Project Specific Documentation

#### Original RRL
- i went through Original RRL files [Original RRL files](<file:///z://AUNSW06/01. NSW-SA Ops/Engineering/Train Control & Signalling/Train Control Systems/Projects/VIC/RRL PKG SIGVIEW>) - mainly technical documents are available for that project - I wasn't able to find many related procedures. Seems like project was relying on old "EIMS-4-xxxx" procedures which don't appear to be completely transferred to the new GGS system.
	- i found some useful management plans in here, seems like there's more interesting documents: [HISTORICAL](<file://///Z:/AUVIC01/Groups/SS-Vic/Engineering Management/Handover/Useful info/RRL/Management Plans/HISTORICAL>)
		- info on Systems Engineering!

- In March 2013, TCS system was evaluated against EN50128 (SIL2 for an unknown reason) as part of the "Original RRL" project. "SigView TCS EN50128 Equivalence Statement was not provided to serve as a compliance statement.  "*The purpose of this report is to provide documentary evidence of how the processes used for developing the Sigview TCS for RRL (also known as RRL-TCS) align to the requirements and recommendations provided in EN50128:2011 ... This report can then be used to support arguments on the suitability of the Sigview TCS (RRL-TCS) in a safety critical envionrment.*"
- However, compliance evidence against each requirement served as a valuable starting point for this report. SEMP nor available requirements mention cenelec standards so it is assumed it was a consequence of SA client stakeholder or to provide reassurance although not in the original SOW.


#### UMA
- going through [UMA Docs (from Sherif)](<file:///C:/Users/igor.krbavcic/OneDrive - UGL Limited/Projects/UMA (from Sherif)/>)
- Questions:
	- how are requirements tracked? VCRM / RTM?
	- Mantis / SVN used? External doc management system?
	- HLDS not required? - check design report, seems like a lot is chucked in there
	- no product modifications required?
	- 

#### CRN

- there was an internal quality audit performed with interesting findings 
	- [UGLRL-001 Audit Report NCSM - Final signed w attachments.pdf](https://uglltd.sharepoint.com/:b:/s/RegionalLinxSystems/EQj0E7wbccpIqWxWVFvsvbIBv5WFp89DmYuzhLnwgCW1NQ?e=FSTyWT) (1100 WHSEQ / 1101 Quality) from 2022 - against the framework
	- there were another two that were not completed (0200 Project Controls and Reporting / 220 and 221)
- "Document Analysis" is a report readable to everyone. It aims to:
	- provide an overview of the documents available in reviewed projects AND GGS repository. Only documents relevant to the TCS team.
	- explains Purpose and Scope of the docs that are not 100% clear
	- suggests improvements based on the current life-cycle (15288) definition and SIL0 EN50128 requirements
- Reviewing Original RRL 50128 Equivalence Statement
	- misinterprets a lot of definitions
	- puts N/A for requirements, although applicable

- Internal Audit (No 2130 performed on 03/02/2022)  with the scope of "Project conformance to UGL Engineering processes" as the name says audited the project scope of the processes, and the Supporting processes were omitted. Three identified NCRs were related to:
	- Competency Management (significant competency assessment gaps at the late stages of the project)
		- RI-8 recommends documenting the validation scope responsibility split between the teams; RI-9 asks for tester roles to be included in TCARP, RI-11 suggests documenting level of independence required for test personnel
	- Management of Suppliers (not all technical suppliers have been reviewed using the supplier evaluation process)
	- Configuration (system design baseline not formalised prior to test commencement)
		- improvement recommendation RI-1 recommended further detailed audit of TCS requirements verification data quality, pointing to in-existence of systemic verification
		- RI-10 suggests a checklist to assist determination of regression testing requirements following code changes
	- All three NCRs are closely related to and/or stemming from "Organisational Project Enabling Processes" which have been omitted in the audit, but also does not seem to be not existent in the day to day TCS operation
	- 





## Recommendations and Action Summary

1. decide whether EN50128 SIL 0 requirements are beneficial for TCS software life-cycle
2. implement a standard SQMP as part of project SEMP, but also for internal product development
3. select / develop set of templates
4. define internal development procedure
	1. configuration management
5. fill the gap in product documentation
	1. "Software Product Specifications"
	2. requirement specs for standard products
6. Mantis standard configuration



| recomendation based on 15288 | recommendation based on SIL 0 |
| ---------------------------- | ----------------------------- |
|                              |                               |
|                              |                               |





Traceability. Document and requirements hierarchy should be standardised and modified per projects' needs afterwards.

Assessment must be carried out by an independent assessor. This is not a requirement for SIL0. However, if implementation is done correctly assessment can be internally performed by an external auditor or by client's or alliance's SA contractor. Depending on risk appetite.

Mantis should be used for managing software change control (approvals etc).

verifications of the process should be performed where applicable (product/project) GGS template exists.

Techniques and Measures need to be selected



- I could write a sample EN50128 compliance statement that would get chucked into Safety Assurance Report safety case or whatever






## References to Documentation Used

My output files:
- [SIL0 Requirements Folder](<file:///C:/Users/igor.krbavcic/OneDrive - UGL Limited/Projects/SIL0 Requirements>)
- Review of all the docs are aggregated as a table in this file:
	- [FSMP Rev0.1.xlsx](<file:///C:\Users\igor.krbavcic\OneDrive - UGL Limited\Projects\SIL0 Requirements\FSMP Rev0.1.xlsx>)


Appendices:
- subhajit's V-model


- MTM standards: [A9090 - Engineering Documents Listing 2023-07-11.xlsx](<file:///C:\Users\igor.krbavcic\OneDrive - UGL Limited\Admin\MTM Standards\A9090 - Engineering Documents Listing 2023-07-11.xlsx>)


[[./Subhajit's V-Model|Subhajit's V-Model]]
- Original RRL TCS project files [Original RRL files](<file:///z://AUNSW06/01. NSW-SA Ops/Engineering/Train Control & Signalling/Train Control Systems/Projects/VIC/RRL PKG SIGVIEW>)
- UMA
- collection of reference documents collected from various projects: [Z:\AUVIC01\Groups\SS-Vic\TCS\_REFERENCE](Z:\AUVIC01\Groups\SS-Vic\TCS\_REFERENCE)

Several sets of documents are taken as a reference for this exercise:

- CRN
- (GLU)
- UGL / CIMIC GGS (Group Governance System) quality system - analysed procedures and templates related to TCS project activities. 
	- 