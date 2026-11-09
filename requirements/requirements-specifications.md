# ForgeAI – Requirements Specifications

**Project:** ForgeAI – Intelligent Student Team Formation and Academic Project Collaboration  
**Course:** SWE 401 – Software Engineering  
**Source:** Phase 2 Requirements Engineering and Functional Modeling Report

## 1. Purpose

This document provides structured natural-language specifications for three core ForgeAI requirements. These specifications refine the expected system behavior and are intended to guide the design, implementation and testing stages.

They do not claim that the functions have already been implemented.

## 2. SPEC-01 – AI Recommendation Request and Validation

**Related requirements:** FR-07, FR-08  
**Related use case:** UC-01 – Generate AI Team Recommendations

### Specification

When a teacher requests recommendations for a project with valid requirements and eligible student profiles, ForgeAI shall prepare the relevant data and send a structured request to the configured external AI API.

ForgeAI shall parse the response, validate the returned student identifiers and mandatory team constraints, and display valid candidate groups with available explanations.

If the API fails or returns an invalid response, ForgeAI shall display an understandable error and shall not finalize any group.

### Expected behavior

- Retrieve the selected project's requirements.
- Retrieve eligible student profiles.
- Validate and prepare the minimum necessary request data.
- Send a structured request to the configured external AI API.
- Parse the returned candidate recommendations.
- Validate student identifiers and mandatory team constraints.
- Display valid candidate groups and available explanations.
- Handle API failures and malformed responses without finalizing a group.

### Related validation considerations

- Missing project information should prevent an invalid request.
- No eligible students should result in an informative message.
- Network or provider errors should be handled without corrupting stored data.
- Invalid API responses should not be accepted as valid recommendations.

## 3. SPEC-02 – Skill Coverage and Missing Skill Analysis

**Related requirement:** FR-09  
**Related use cases:** UC-01 and UC-02

### Specification

When candidate group membership and project skill requirements are available, ForgeAI shall compare the skills recorded for each team member with the required project skills.

The system shall display skills represented by the group and identify each required skill for which no qualifying team member is recorded.

The analysis shall be presented to the teacher before team approval.

### Expected behavior

- Retrieve the project's required skills.
- Retrieve the recorded skills of each candidate group member.
- Compare the available member skills with the required project skills.
- Display the skills represented within the group.
- Identify required skills for which no qualifying team member is recorded.
- Present the results during recommendation review, before approval.

## 4. SPEC-03 – Teacher Review and Team Approval

**Related requirements:** FR-10, FR-11  
**Related use case:** UC-02 – Review and Approve or Modify a Team

### Specification

When a teacher reviews a candidate group, ForgeAI shall display its members, relevant profile information, recommendation explanation and skill-coverage result.

The teacher shall be able to approve, modify or reject the candidate.

Before saving an approved group, ForgeAI shall validate team-size constraints and student eligibility. A failed validation shall prevent approval and display a corrective message.

### Expected behavior

- Display candidate group members.
- Display relevant profile information.
- Display the recommendation explanation.
- Display skill-coverage results and missing required skills.
- Allow the teacher to approve, modify or reject the candidate.
- Validate team-size constraints before saving.
- Validate student eligibility before saving.
- Prevent approval when validation fails.
- Display a corrective message when the candidate violates a mandatory constraint.

## 5. External AI Integration Constraint

The AI provider is not specified in the Phase 2 report. Provider selection, API contract, pricing, data-retention policy and availability remain to be confirmed during design.

The external AI API is responsible for returning candidate recommendations and explanations. ForgeAI remains responsible for validating the returned information and enforcing its own team constraints. The AI service does not approve teams or directly persist ForgeAI records.

## 6. Source and Status

These specifications are derived from the Phase 2 report. They define intended behavior for subsequent design and implementation and should be used as a basis for future test cases.
