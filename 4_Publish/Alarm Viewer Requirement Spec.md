# Alarm Viewer Requirement Spec


[Alarm Viewer - SharePoint Link](https://uglltd.sharepoint.com/:f:/s/TCSLab/EjnUuzl4YwVCrdkB70k46RkB12K8kT45U2cVvv41OjyUeA?e=vtVmnl)


# OBSOLETE

### Purpose
We have original SOW which contains desired state. We have current state based on investigation performed, and gap analysis between the two. Current state has been running since July 21 

Due to scope changes during the implementation and changes in TCS team structure an initial system has not been delivered in its entirety as required by the original SOW [1].

Investigation and gap analysis [2] has been performed and significant input from UGL is required to fix the outstanding issues. This SWRS contains the requirements for the outstanding work.


### Scope

[2] contains recommendations and actions, and gaps in features and site deployment
based on those.



### Extract from  [1]


4.1	Recommendations and Actions

a.	Collect information for the desired state deployment environments based on their individual environments, dependencies, and system specifications:
i.	System Information
1.	Operating System
2.	Hardware
3.	Etc
ii.	PCVue Version
iii.	.NET Version
iv.	SigView Software Manager Versions

b.	Write updated System Requirements Specification based on what was built and remove any open to interpretation items. 
i.	Clarify Replay functionality.
ii.	Clarify View Only Profile
iii.	Clarify Maintenance Profile
iv.	Clarify Operator Profile
c.	Write System Requirements Specification
d.	Negotiate approval of updated system requirements with client.
e.	Write as-built Functional Specification to meet the system requirements.
f.	Write as-built Architecture and High-Level Design Document(s).
g.	Write Detailed Design Document(s).
h.	Setup FAT environment with as close to Production as possible for all Production Environments as per 3.2 Sites. 
i.	Replicate SITE defect with Operator account on FAT environment.
j.	Replicate Replay Functionality defect on FAT environment.
k.	Develop solutions for outstanding issues.
l.	Write Test Plan with test cases to match agreed requirements.
m.	Write Risk Assessment for the desired state deployment environments based on their individual environments, dependencies, and system specifications.


1.1                          Features


| Current State                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | Desired State                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Alarm Manager starts from desktop shortcut                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Alarm Manager starts on SigView Project start-up                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| The Alarm Manager doesn’t display any alarms during replay mode.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | Alarm Manager includes replay functionality                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| The alarm panel displays alarm text accordingly:<br><br>1.    Flashing Red for Active and Not Acknowledged Critical Alarms,<br><br>2.    Steady Red for Active and Acknowledged Critical Alarms,<br><br>3.    Flashing Yellow for Active and Not Acknowledged Non-Critical Alarms,<br><br>4.    Steady Yellow for Active and Acknowledged Non-Critical Alarms,<br><br>5.    Flashing Blue for Active and Not Acknowledged Maintenance Blocking,<br><br>6.    Steady Blue for Active and Acknowledged Maintenance Blocking,<br><br>7.    Flashing Green for Cleared and Not Acknowledged Alarms (Critical, Non-Critical, Maintenance Blocking),<br><br>8.    Invisible for Cleared and Acknowledged Alarms (Critical, Non-Critical, Maintenance Blocking) and<br><br>9.    When the alarm text is selected the background, colour should be inverted for clear readability. | The alarm panel displays alarm text accordingly:<br><br>1.    Flashing Red for Active and Not Acknowledged Critical Alarms,<br><br>2.    Steady Red for Active and Acknowledged Critical Alarms,<br><br>3.    Flashing Yellow for Active and Not Acknowledged Non-Critical Alarms,<br><br>4.    Steady Yellow for Active and Acknowledged Non-Critical Alarms,<br><br>5.    Flashing Blue for Active and Not Acknowledged Maintenance Blocking,<br><br>6.    Steady Blue for Active and Acknowledged Maintenance Blocking,<br><br>7.    Flashing Green for Cleared and Not Acknowledged Alarms (Critical, Non-Critical, Maintenance Blocking),<br><br>8.    Invisible for Cleared and Acknowledged Alarms (Critical, Non-Critical, Maintenance Blocking) and<br><br>9.    When the alarm text is selected the background, colour should be inverted for clear readability. |
| Operator Profile with filters for:<br><br>1.    Critical Alarms,<br><br>2.    Non-Critical Alarms,<br><br>3.    Maintenance Block Indication,                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | Operator Workstation Profile with<br><br>-          Unchangeable filter alarms under the multiple areas on control<br><br>-          optional filters for:<br><br>1.    Critical Alarms,<br><br>2.    Non-Critical Alarms and<br><br>3.    Maintenance Block Indication.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| View Only Profile with filters for:<br><br>1.    Critical Alarms,<br><br>2.    Non-Critical Alarms,<br><br>3.    Maintenance Block Indication,<br><br>4.    System Alarms<br><br>5.    Control Area.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | View Only Workstation Profile with filters for:<br><br>1.    Critical Alarms,<br><br>2.    Non-Critical Alarms,<br><br>3.    Maintenance Block Indication<br><br>4.    Control Area Drop down Selection.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Maintenance Profile with filters for:<br><br>1.    Critical Alarms,<br><br>2.    Non-Critical Alarms,<br><br>3.    Maintenance Block Indication,<br><br>4.    System Alarms<br><br>5.    Control Area.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Maintenance Profile with filters for:<br><br>1.    Critical Alarms,<br><br>2.    Non-Critical Alarms,<br><br>3.    Maintenance Block Indication,<br><br>4.    System Alarms<br><br>5.    Control Area.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Alarm Manager is usable by the following profiles:<br><br>1.    Admin                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Alarm Manager will be usable by the following windows accounts:<br><br>1.    Admin<br><br>2.    Operator<br><br>3.    Maintainer                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Alarm Manager has acknowledgement capability for the Operator Profile.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Alarm Manager has acknowledgement buttons for the following profiles:<br><br>1.    Operator                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |

1.2 Sites


| Current State                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | Desired State                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Centrol:<br><br>1.    Operator Workstation  <br>Not Deployed<br><br>2.    Operator Workstation  <br>Not Deployed<br><br>3.    Operator Workstation  <br>Not Deployed<br><br>4.    Operator Workstation  <br>Not Deployed<br><br>5.    Operator Workstation  <br>Not Deployed<br><br>6.    Operator Workstation  <br>Not Deployed<br><br>7.    Operator Workstation (Shepperton New one)  <br>Not Deployed<br><br>8.    Operator Workstation (Training Room)  <br>Not Deployed<br><br>9.    Maintenance Workstation  <br>**v1.2.8.5  <br>Working with admin account only  <br>Replay Untested**<br><br>10. View Only Workstation (Tech Services)<br><br>**v1.2.8.5**<br><br>**Working with admin account only  <br>Replay Untested**<br><br>**Startup not installed**<br><br>11. View Only (4 decommissioned, not in use)  <br>Decommissioned as far as we are aware | Centrol:<br><br>1.    Operator Workstation  <br>Deployed<br><br>2.    Operator Workstation  <br>Deployed<br><br>3.    Operator Workstation  <br>Deployed<br><br>4.    Operator Workstation  <br>Deployed<br><br>5.    Operator Workstation  <br>Deployed<br><br>6.    Operator Workstation  <br>Deployed<br><br>7.    Operator Workstation (Shepperton New one)  <br>Not Deployed<br><br>8.    Operator Workstation (Training Room)  <br>Not Deployed<br><br>9.    Maintenance Workstation  <br>Deployed<br><br>10. View Only Workstation (Tech Services)  <br>Deployed<br><br>11. View Only (4 decommissioned, not in use)  <br>Not Deployed |
| DRS:<br><br>1.    Operator Workstation  <br>**v1.2.8.3  <br>Untested  <br>Appears to have had issues when deployed  <br>Startup installed but overwritten.**<br><br>2.    Operator Workstation  <br>**Unconfirmed, likely deployed as above (1.)**<br><br>3.    Operator Workstation  <br>**Unconfirmed, likely deployed as above (1.)**<br><br>4.    Operator Workstation  <br>**Unconfirmed, likely deployed as above (1.)**<br><br>5.    Operator Workstation  <br>**Unconfirmed, likely deployed as above (1.)**<br><br>6.    Operator Workstation  <br>**Unconfirmed, likely deployed as above (1.)**<br><br>7.    Maintenance Workstation  <br>**Unconfirmed, likely deployed as above (1.)**                                                                                                                                                                 | DRS:<br><br>1.    Operator Workstation  <br>Deployed<br><br>2.    Operator Workstation  <br>Deployed<br><br>3.    Operator Workstation  <br>Deployed<br><br>4.    Operator Workstation  <br>Deployed<br><br>5.    Operator Workstation  <br>Deployed<br><br>6.    Operator Workstation  <br>Deployed<br><br>7.    Maintenance Workstation  <br>Deployed                                                                                                                                                                                                                                                                                       |
| Metrol:<br><br>Not Deployed                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | Metrol:<br><br>1.    View Only Workstation (NetOp from Centrol)  <br>Deployed<br><br>2.    View Only Workstation (NetOp DRS situation)  <br>Deployed                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Werribee:<br><br>Not Deployed                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | Werribee:<br><br>1.    View Only Workstation (NetOp from Centrol)  <br>Deployed                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Geelong:<br><br>Not Deployed                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | Geelong:<br><br>1.    View Only Workstation  <br>Deployed                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Ballarat:<br><br>Not Deployed                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | Ballarat:<br><br>1.    View Only Workstation  <br>Deployed                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Southern Cross Station Yard Master:<br><br>Not Deployed                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Southern Cross Station Yard Master:<br><br>1.    Operator Workstation  <br>Deployed<br><br>2.    Operator Workstation  <br>Deployed                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |




## Alarm Viewer Software Requirements Specification (SWRS)

## 1. Introduction

### 1.1 Purpose
The purpose of this SWRS is to detail the outstanding requirements for the Alarm Viewer project, aimed at implementing the full scope of work as specified in the original Statement of Work (SOW). The gap analysis between the current and desired states has highlighted the need for UGL's input to resolve outstanding issues.

### 1.2 Scope
This document outlines the requirements based on investigations, gap analysis, and recommendations for the Alarm Viewer project, which has been operational since July 21. The document will address the variances in features and site deployment requirements as identified.

## 2. System Requirements

### 2.1 General Requirements

#### 2.1.1 RS.0001
The system shall be based on the desired state deployment environments, including Operating System, Hardware specifications, PCVue Version, .NET Version, and SigView Software Manager Versions.

### 2.2 Functional Requirements

#### 2.2.1 RS.0002
The SIGMAP product shall start the Alarm Manager automatically upon the SigView Project's start-up.

#### 2.2.2 RS.0003
The Alarm Manager shall include replay functionality to display alarms during replay mode.

#### 2.2.3 RS.0004
The Alarm Manager's display panel shall:
- Flash red for active, not acknowledged critical alarms.
- Remain steady red for active, acknowledged critical alarms.
- Flash yellow for active, not acknowledged non-critical alarms.
- Remain steady yellow for active, acknowledged non-critical alarms.
- Flash blue for active, not acknowledged maintenance blocking.
- Remain steady blue for active, acknowledged maintenance blocking.
- Flash green for cleared, not acknowledged alarms (critical, non-critical, maintenance blocking).
- Become invisible for cleared and acknowledged alarms (critical, non-critical, maintenance blocking).
- Invert the background colour of the selected alarm text for clear readability.

#### 2.2.4 RS.0005
The system shall implement an Operator Workstation Profile with unchangeable filter alarms under multiple areas of control and optional filters for critical alarms, non-critical alarms, and maintenance block indication.

#### 2.2.5 RS.0006
The system shall implement a View Only Workstation Profile with filters for critical alarms, non-critical alarms, maintenance block indication, and a control area dropdown selection.

#### 2.2.6 RS.0007
The Maintenance Profile shall have filters for critical alarms, non-critical alarms, maintenance block indications, system alarms, and control areas as per design.

#### 2.2.7 RS.0008
The Alarm Manager shall be accessible and functional for the following Windows accounts: Admin, Operator, and Maintainer.

#### 2.2.8 RS.0009
The system shall include acknowledgement buttons for the Alarm Manager within the Operator profile.

### 2.3 Site Deployment Requirements

#### 2.3.1 RS.0010
The Centrol, DRS, Metrol, Werribee, Geelong, Ballarat, and Southern Cross Station Yard Master sites shall have the Alarm Manager deployed and configured according to the desired state specifications.

#### 2.3.2 RS.0011
All Operator Workstations at each site specified shall be deployed and in accordance to the system specifications as per the desired state.

#### 2.3.3 RS.0012
All View Only Workstations at each site specified shall be deployed with the intended configurations and functionalities.

#### 2.3.4 RS.0013
The Maintenance Workstation at each specified site shall be equipped and configured as detailed in the desired state specifications.

### 2.4 Support Requirements
*Note: Specific support requirements to be determined and added.*

## 3. Documentation Requirements
*Note: Documentation requirements including updated SRS, as-built Functional Specification, Architecture and High-Level Design Document(s), Detailed Design Document(s), Test Plan, and Risk Assessment to be detailed here in further revisions of this document.* 

---

*Note: The above SWRS is structured to provide clear and concise requirements, ensuring that they are verifiable and traceable as per best practices outlined in the Requirements Writing Guide. Each requirement has been given a specific identifier (RS.####) to ensure traceability. The complement syntax and guideline for simplicity and clarity have been applied throughout. Full details and justifications will be added to support each requirement in line with the Requirements Writing Guide and the information provided in the purpose, scope, and extract sections of the provided notes.*




Certainly! Here is the table in Markdown format:

| Site | Type | OS Version | HW Specs | PCVue Version | SigView SW Manager | .NET Version | Comment |
|------|------|------------|----------|---------------|--------------------|--------------|---------|
| Centrol | Operator | | | | | | |
| Centrol | Operator | | | | | | |
| Centrol | Operator | | | | | | |
| Centrol | Operator | | | | | | |
| Centrol | Operator | | | | | | |
| Centrol | Operator | | | | | | |
| Centrol | Operator (New Shepperton) | | | | | | Will need something new in future |
| Centrol | Training Room | | | | | | Not in scope of these works |
| Centrol | Maintenance | | | | | | |
| Centrol | View Only | | | | | | |
| Centrol | Not in-use View Only Configs | | | | | | No current workstations |
| Centrol | SAMS View Only | | | | | | Mentioned in Letter of Offer; already decommissioned |
| DRS | Operator | | | | | | |
| DRS | Operator | | | | | | |
| DRS | Operator | | | | | | |
| DRS | Operator | | | | | | |
| DRS | Operator | | | | | | |
| DRS | Operator | | | | | | |
| DRS | Maintenance | | | | | | |
| Metrol | View Only | | | | | | |
| Metrol | View Only | | | | | | |
| Werribee | View Only | | | | | | |
| Geelong | View Only | | | | | | |
| Ballarat | View Only | | | | | | |
| Southern Cross Station Yard Master | Operator | | | | | | Likely oversight, missed in the original scope of works |
| Southern Cross Station Yard Master | Operator | | | | | | Likely oversight, missed in the original scope of works |

Please note that placeholders (empty cells) have been used for the OS Version, HW Specs, PCVue Version, SigView SW Manager, and .NET Version, as these details were not provided. These will need to be filled in with specific information for each site and type of workstation.

