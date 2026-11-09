# ForgeAI – Functional Requirements

**Project:** ForgeAI – Intelligent Student Team Formation and Academic Project Collaboration  
**Course:** SWE 401 – Software Engineering  
**Source:** Phase 2 Requirements Engineering and Functional Modeling Report

## 1. Purpose

This document defines the functional requirements for ForgeAI. It describes the services the system is expected to provide to students and teachers.

ForgeAI supports student profile management, academic project management, AI-assisted team recommendations, instructor review and approval, and project task coordination.

The system uses a configured external AI API to generate candidate team recommendations. The AI provider has not yet been selected. The teacher remains responsible for reviewing and making the final decision about team formation.

## 2. Requirement Priorities

- **Must:** Essential to the core prototype.
- **Should:** Important supporting functionality.
- **Could:** Optional or may be simplified depending on implementation capacity.

## 3. Functional Requirements

| ID | Functional requirement | Priority |
|---|---|---|
| FR-01 | The system shall allow students to create their profiles. | Must |
| FR-02 | The system shall allow students to update profile information, including academic level, skills, interests and availability. | Must |
| FR-03 | The system shall allow students to view their profile information. | Must |
| FR-04 | The system shall allow teachers to create new academic projects. | Must |
| FR-05 | The system shall allow teachers to define project requirements, including required skills and group-size limits. | Must |
| FR-06 | The system shall allow teachers to view and manage the projects they create. | Must |
| FR-07 | The system shall generate candidate student-group recommendations using a configured external AI API, based on project requirements and relevant student information, including skills, interests, academic levels and availability. | Must |
| FR-08 | The system shall display the reasons behind each group recommendation using the explanation returned by the AI service and/or the system's validated recommendation data. | Must |
| FR-09 | The system shall display the skills available within each recommended group and identify missing required skills. | Must |
| FR-10 | The system shall allow teachers to review recommended groups before finalizing them. | Must |
| FR-11 | The system shall allow teachers to approve or modify recommended groups, subject to validation of mandatory project constraints. | Must |
| FR-12 | The system shall allow teachers to create tasks for project groups. | Should |
| FR-13 | The system shall allow teachers to assign tasks to individual students within a project group. | Should |
| FR-14 | The system shall allow teachers to set deadlines for tasks. | Should |
| FR-15 | The system shall allow students to view their assigned tasks and deadlines. | Should |
| FR-16 | The system shall allow students to update the status of their assigned tasks. | Should |
| FR-17 | The system shall allow teachers to view task statuses and monitor group progress. | Should |
| FR-18 | The system shall provide in-application notifications or reminders about task deadlines and updates, subject to the prototype's implementation capacity. | Could |

## 4. Requirement Notes

1. FR-07 depends on selecting and configuring an external AI API. The provider, API contract, pricing, data-retention policy and availability remain to be confirmed.
2. The AI service generates candidate recommendations. It does not approve teams or directly persist ForgeAI records.
3. FR-10 and FR-11 preserve teacher control over team approval and modification.
4. FR-11 requires validation of mandatory project constraints before an approved group is saved.
5. FR-18 may be simplified to dashboard reminders rather than email, push or real-time notifications.

## 5. Main Functional Areas

- **Student Profile Management:** FR-01 to FR-03
- **Project Management:** FR-04 to FR-06
- **AI Team Recommendations:** FR-07 to FR-09
- **Instructor Review and Approval:** FR-10 to FR-11
- **Task and Progress Management:** FR-12 to FR-17
- **Notifications and Reminders:** FR-18

## 6. Source and Status

These requirements are taken from the ForgeAI Phase 2 report. They describe the intended system behavior and are not evidence that the functionality has already been implemented.
