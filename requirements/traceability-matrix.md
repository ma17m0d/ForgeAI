# ForgeAI – Requirements Traceability Matrix

**Project:** ForgeAI – Intelligent Student Team Formation and Academic Project Collaboration  
**Course:** SWE 401 – Software Engineering  
**Source:** Phase 2 Requirements Engineering and Functional Modeling Report

## 1. Purpose

This matrix maps each functional requirement to its related use case or analysis artifact, proposed design module, proposed Java implementation reference and planned test case.

The Java class names are proposed references for Phase 3/4. They must be aligned with the final NetBeans package structure. Test case IDs identify planned tests; no test execution is claimed in the Phase 2 report.

## 2. Traceability Matrix

| Requirement ID | Use case / Analysis artifact | Design / Module | Proposed implementation reference | Planned test case |
|---|---|---|---|---|
| FR-01 | Student profile workflow / UC-03 (profile subflow) | Student Profile UI + Student entity | `StudentProfilePanel.java`; `StudentService.java` | TC-01 |
| FR-02 | Profile maintenance / student profile model | Profile update and validation module | `StudentProfile.java`; `StudentService.java` | TC-02 |
| FR-03 | View profile workflow | Student Profile UI | `StudentProfilePanel.java` | TC-03 |
| FR-04 | Project creation workflow / teacher actor | Project Management module | `ProjectPanel.java`; `ProjectService.java` | TC-04 |
| FR-05 | Project requirements model | Project Requirements module | `Project.java`; `ProjectService.java` | TC-05 |
| FR-06 | Project management workflow | Project Management UI/service | `ProjectPanel.java`; `ProjectService.java` | TC-06 |
| FR-07 | UC-01 Generate AI Recommendations | AI Integration / Recommendation module | `AIRecommendationService.java`; `RecommendationService.java` | TC-07 |
| FR-08 | UC-01; recommendation explanation analysis | Recommendation Review module | `Recommendation.java`; `RecommendationPanel.java` | TC-08 |
| FR-09 | UC-01/UC-02; skill coverage analysis | Skill Coverage module | `SkillCoverageService.java` | TC-09 |
| FR-10 | UC-02 Review Candidate Team | Recommendation Review UI | `RecommendationPanel.java` | TC-10 |
| FR-11 | UC-02 Approve or Modify Team | Team Approval and validation module | `TeamService.java`; `TeamValidator.java` | TC-11 |
| FR-12 | UC-03 Create Task | Task Management module | `TaskPanel.java`; `TaskService.java` | TC-12 |
| FR-13 | UC-03 Assign Task | Task Assignment module | `TaskService.java` | TC-13 |
| FR-14 | UC-03 Set Deadline | Task Deadline module | `Task.java`; `TaskService.java` | TC-14 |
| FR-15 | UC-03 Student View Tasks | Student Task UI | `StudentTaskPanel.java` | TC-15 |
| FR-16 | UC-03 Update Task Status | Task Status module | `TaskService.java` | TC-16 |
| FR-17 | UC-03 Monitor Progress | Progress Monitoring module | `ProgressService.java`; `ProgressPanel.java` | TC-17 |
| FR-18 | UC-03 Deadline/update reminder | Notification / Reminder module | `ReminderService.java`; `NotificationPanel.java` | TC-18 |

## 3. Planned Test Case Coverage

| Test case | Requirement | Planned verification |
|---|---|---|
| TC-01 | FR-01 | Verify that a student can create a profile. |
| TC-02 | FR-02 | Verify that profile information can be updated and validated. |
| TC-03 | FR-03 | Verify that a student can view their profile information. |
| TC-04 | FR-04 | Verify that a teacher can create an academic project. |
| TC-05 | FR-05 | Verify that project requirements and group-size limits can be defined. |
| TC-06 | FR-06 | Verify that a teacher can view and manage created projects. |
| TC-07 | FR-07 | Verify that ForgeAI can request and process candidate recommendations through the configured external AI API. |
| TC-08 | FR-08 | Verify that recommendation explanations are displayed. |
| TC-09 | FR-09 | Verify that group skills and missing required skills are displayed correctly. |
| TC-10 | FR-10 | Verify that a teacher can review candidate groups. |
| TC-11 | FR-11 | Verify that valid groups can be approved or modified and invalid groups are prevented from approval. |
| TC-12 | FR-12 | Verify that a teacher can create a task for a project group. |
| TC-13 | FR-13 | Verify that a task can be assigned to a member of the selected team. |
| TC-14 | FR-14 | Verify that a task deadline can be set and validated. |
| TC-15 | FR-15 | Verify that students can view their assigned tasks and deadlines. |
| TC-16 | FR-16 | Verify that a student can update the status of their assigned task. |
| TC-17 | FR-17 | Verify that a teacher can view task statuses and monitor group progress. |
| TC-18 | FR-18 | Verify the selected in-application reminder or notification behavior, if implemented. |

## 4. Traceability Notes

1. The implementation references are proposed Java class names, not confirmed existing source files.
2. The final package and class structure should be established during system design and updated in this matrix.
3. The test cases are planned verification activities. They must be implemented and executed during the testing stage.
4. FR-18 is a Could-priority requirement and may be simplified or deferred depending on prototype capacity.
5. FR-07 depends on selecting and configuring an external AI provider.
6. UC-03 is used as the related workflow for student profile creation and maintenance in the original Phase 2 traceability mapping; this relationship should be reviewed during detailed design if a separate profile use case is introduced.

## 5. Source and Status

This matrix preserves the mappings presented in the Phase 2 report. It provides a starting point for design and testing traceability and should be updated as the actual implementation and test results become available.
