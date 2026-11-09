# ForgeAI – Use Case Descriptions

**Project:** ForgeAI – Intelligent Student Team Formation and Academic Project Collaboration  
**Course:** SWE 401 – Software Engineering  
**Source:** Phase 2 Requirements Engineering and Functional Modeling Report

## 1. System Actors

| Actor | Description |
|---|---|
| Student | Provides academic and project-related information, maintains a profile, views team information and assigned tasks, and updates task status. |
| Teacher / Instructor | Creates projects, defines requirements, requests and reviews AI recommendations, approves or modifies groups, assigns tasks and monitors progress. |
| External AI API | Supporting external service that receives the relevant recommendation request data and returns candidate group recommendations and explanations. It does not approve groups or persist ForgeAI records. |

ForgeAI has two primary human user types: students and teachers. The external AI API is a supporting system, not a human user or account role.

## 2. UC-01 – Generate AI Team Recommendations

| Field | Description |
|---|---|
| Use Case ID | UC-01 |
| Primary actor | Teacher / Instructor |
| Supporting actor | External AI API |
| Goal | Generate candidate student groups using project requirements and relevant student information, with explanations for instructor review. |
| Preconditions | A project is available; required skills and team-size limits are defined; eligible student profiles exist; API configuration and credentials are available. |
| Trigger | Teacher selects **Generate Recommendations** for a project. |

### Main Success Scenario

1. Teacher selects a project.
2. ForgeAI retrieves the project requirements.
3. ForgeAI retrieves eligible student profiles.
4. ForgeAI validates and prepares the minimum necessary request data.
5. ForgeAI sends a request to the configured AI API.
6. The API returns candidate groups and explanations.
7. ForgeAI parses the response and validates student identifiers, eligibility, duplicate membership and team-size constraints.
8. ForgeAI calculates and displays skill coverage and missing required skills.
9. Candidate groups are shown to the teacher for review.

### Alternative and Exception Flows

- **A1 – Missing project data:** ForgeAI displays the fields that must be completed.
- **A2 – No eligible students:** ForgeAI informs the teacher and does not call the API.
- **A3 – Network or API failure:** ForgeAI displays an error and preserves stored data.
- **A4 – Malformed API response:** ForgeAI rejects the response and displays a processing error.
- **A5 – Constraint violation:** ForgeAI marks the candidate as invalid and prevents approval.

### Postconditions

Validated candidate recommendations are displayed for review. No group is finalized automatically.

---

## 3. UC-02 – Review and Approve or Modify a Team

| Field | Description |
|---|---|
| Use Case ID | UC-02 |
| Primary actor | Teacher / Instructor |
| Goal | Allow the teacher to inspect candidate group composition and explanations, then approve, modify or reject a recommendation. |
| Preconditions | At least one candidate recommendation has been generated and parsed. |
| Trigger | Teacher opens the recommendation review screen. |

### Main Success Scenario

1. ForgeAI displays candidate group members.
2. ForgeAI displays relevant skills, academic levels and recommendation explanations.
3. ForgeAI displays skill coverage and missing required skills.
4. Teacher reviews the candidate.
5. Teacher approves it or modifies membership.
6. ForgeAI validates team-size limits, student eligibility and duplicate membership.
7. If valid, ForgeAI saves the approved group and makes the assignment available to the relevant students.

### Alternative and Exception Flows

- **A1 – Candidate rejected:** The candidate remains unapproved.
- **A2 – Invalid team size:** ForgeAI displays a validation message and does not save the modification.
- **A3 – Ineligible or already assigned student:** ForgeAI prevents approval where project rules prohibit the assignment.
- **A4 – Database save failure:** ForgeAI displays an error and retains the previous saved state.

### Postconditions

A valid approved group is saved, or the candidate remains unapproved or rejected. The teacher remains the final decision-maker.

---

## 4. UC-03 – Manage Tasks and Monitor Progress

| Field | Description |
|---|---|
| Use Case ID | UC-03 |
| Primary actors | Teacher / Instructor and Student |
| Goal | Allow teachers to create tasks, assign responsibilities and deadlines, and allow students to update task status. |
| Preconditions | A project and an approved team exist. |
| Trigger | Teacher opens task management for an approved project team. |

### Main Success Scenario

1. Teacher selects a project team.
2. Teacher creates a task with a title and description.
3. Teacher assigns the task to a member of that team.
4. Teacher sets a deadline.
5. ForgeAI validates and saves the task.
6. Student opens their task list.
7. Student views task details and deadline.
8. Student updates the task status.
9. ForgeAI validates authorization and saves the update.
10. Teacher views task statuses and overall progress.

### Alternative and Exception Flows

- **A1 – Missing task description or invalid deadline:** ForgeAI requests correction.
- **A2 – Assigned student is not a member of the selected team:** ForgeAI rejects the assignment.
- **A3 – Student attempts to modify another student's task:** ForgeAI denies the operation.
- **A4 – Database error:** ForgeAI displays a message and preserves previously saved information.

### Postconditions

The task, assignee, deadline and current status are stored and available to authorized users.

---

## 5. Use Case Relationships and System Boundary

The UML use case diagram in the Phase 2 report identifies the student and teacher as human actors and the external AI API as a supporting actor for recommendation generation.

The diagram intentionally omits `include` and `extend` relationships where they are not necessary to express the approved behavior.

## 6. Source and Status

These use cases describe intended system behavior from the Phase 2 report. They are design and requirements artifacts, not evidence that the workflows have already been implemented.
