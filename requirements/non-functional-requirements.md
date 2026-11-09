# ForgeAI – Non-Functional Requirements

**Project:** ForgeAI – Intelligent Student Team Formation and Academic Project Collaboration  
**Course:** SWE 401 – Software Engineering  
**Source:** Phase 2 Requirements Engineering and Functional Modeling Report

## 1. Purpose

This document defines the quality attributes and constraints that ForgeAI should satisfy. Each requirement includes a measurable acceptance criterion to guide future implementation and testing.

The criteria below are proposed targets. They must be evaluated during implementation and testing; they are not claims of achieved performance.

## 2. Non-Functional Requirements

| ID | Quality attribute | Requirement | Measurable acceptance criterion |
|---|---|---|---|
| NFR-01 | Usability | The system shall provide a simple and clear user interface that students and teachers can understand and use easily. | In a small usability session, at least 4 of 5 representative users should complete the defined profile, recommendation-review or task-view workflow without developer intervention. Proposed target; recruit users if permitted. |
| NFR-02 | Usability / Error messaging | The system shall display clear error messages when users enter invalid or incomplete information. | All invalid-input cases in the approved test set must show a corrective message and must not crash or save invalid data. |
| NFR-03 | Performance | The system shall generate group recommendations within 5 seconds when processing a project with up to 100 student profiles. | Proposed target: API request-to-display time ≤5 seconds in at least 90% of 10 repeated trials on the agreed test network. Record provider/network latency separately; revise with instructor if infeasible. |
| NFR-04 | Performance | The system shall respond to normal user actions, such as opening profiles and viewing tasks, within 3 seconds under normal operating conditions. | At least 95% of 20 measured local profile/task operations should complete within 3 seconds on the demonstration computer. |
| NFR-05 | Security / Access control | The system shall restrict access to features according to user roles, so students and teachers can only access permitted functions. | All defined role-access test cases must pass: a student cannot invoke teacher-only project/team approval/task creation functions. |
| NFR-06 | Input validation | The system shall validate user input to prevent invalid or incomplete data from being stored. | All defined boundary, required-field, invalid-format and invalid-reference tests must reject invalid data; verify the database remains unchanged. |
| NFR-07 | Privacy | The system shall protect student information and only display it to authorized users. | Access tests must show unauthorized users cannot view another student's restricted profile/task data. Only minimum necessary fields are sent to the external AI API. |
| NFR-08 | Reliability | The system shall handle invalid user input without crashing. | Run the invalid-input test suite; the application remains operational and displays validation feedback in every test. |
| NFR-09 | Data integrity | The system shall maintain the accuracy of stored student profiles, project information, group recommendations and task records. | Create/read/update tests must return the saved values; invalid foreign-key references and duplicate membership in a confirmed team must be rejected. |
| NFR-10 | Compatibility | The system shall run as a Java desktop application on computers with a compatible Java Runtime Environment installed. | Application launches and passes core smoke tests on the agreed JDK/JRE version and NetBeans build environment. |

## 3. Testing Considerations

The acceptance criteria should be converted into test cases during implementation and testing.

- Usability should be assessed with representative users, subject to course approval.
- Performance tests should record the computer, network and AI provider conditions.
- Access-control tests should verify both interface restrictions and underlying service-level authorization.
- Input-validation tests should include missing fields, invalid formats, boundary values and invalid references.
- Privacy tests should verify what profile information is visible to each role and what information is transmitted to the external AI API.
- Data-integrity tests should verify database relationships and prevent invalid team membership.
- Compatibility tests should use the agreed Java runtime and NetBeans environment.

## 4. Important Constraints

The external AI provider has not yet been selected. Therefore, recommendation performance and external-service availability cannot yet be guaranteed. The proposed response-time target should be reviewed after the provider and test environment are selected.

## 5. Source and Status

These requirements and acceptance criteria are based on the Phase 2 report. Their measurable criteria are proposed targets that require verification; no test execution or achievement is claimed at this stage.
