## 1. What is an Epic in Agile?

An **Epic** is a **large body of work** that is too big to be completed as a single User Story.

An Epic is usually broken down into multiple smaller **Stories** that can be developed, tested, and delivered incrementally.

### Example

Suppose you're building an e-commerce application.

**Epic:**

> User Account Management

This could contain several Stories:

* Create user registration
* User login
* Forgot password
* Change password
* Update profile
* Enable two-factor authentication

So:

**Epic → Stories → Tasks/Sub-tasks**

Think of an Epic as a **big business objective or feature area**.

---

# 2. What is a Story?

A **User Story** describes a small piece of functionality from the **user's/business user's perspective**.

It explains:

* **Who** wants something?
* **What** do they want?
* **Why** do they want it?

### Standard User Story format

> **As a [user/persona], I want [functionality], so that [benefit/reason].**

### Example

> As a registered user, I want to reset my password using my email address, so that I can regain access to my account if I forget my password.

This is small enough for a development team to work on during a Sprint.

---

# 3. How are Epics and Stories related?

The relationship is straightforward:

```text
EPIC
│
├── Story 1
├── Story 2
├── Story 3
├── Story 4
└── Story 5
```

### Example: Food Delivery Application

**Epic:** Online Food Ordering

**Stories:**

1. As a customer, I want to search for restaurants.
2. As a customer, I want to view a restaurant's menu.
3. As a customer, I want to add food items to my cart.
4. As a customer, I want to place an order.
5. As a customer, I want to pay for my order.
6. As a customer, I want to track my delivery.

The **Epic represents the larger capability**, while each Story represents a smaller deliverable.

---

# 4. Creating an Epic in Jira

The exact Jira UI can vary depending on your Jira project type/version, but the general process is:

### Step 1

Open your Jira project.

### Step 2

Go to **Backlog** or the relevant issue/project view.

### Step 3

Create an issue and select:

**Issue Type → Epic**

### Step 4

Enter the Epic details.

Example:

**Epic Name:**

> User Authentication

**Summary:**

> Implement user authentication functionality

**Description:**

> Implement registration, login, password recovery, and related authentication functionality for application users.

### Step 5

Click **Create**.

The Epic can then be associated with the Stories that belong to it.

---

# 5. Creating a Story in Jira

Again, the exact location varies by Jira configuration.

### Step 1

Open your Jira project.

### Step 2

Click **Create**.

### Step 3

Select:

**Issue Type → Story**

### Step 4

Enter the Story details.

For example:

**Summary:**

> Implement password reset functionality

**Description:**

> As a registered user, I want to reset my password using my registered email address, so that I can regain access to my account if I forget my password.

**Epic:**

> User Authentication

**Acceptance Criteria:**

* User can request a password reset.
* User receives a password-reset email.
* Reset link expires after the configured period.
* User can create a new password.
* User can log in using the new password.

Then click **Create**.

---

# 6. Where does the Story appear in Jira?

A newly created Story can appear in the **Backlog**, depending on your Jira project's configuration and workflow.

The important distinction is:

### Backlog

The **Backlog** contains work that the team has not yet committed to a Sprint.

For example:

```text
Backlog

Epic: User Authentication
    ├── Story: User Registration
    ├── Story: User Login
    └── Story: Password Reset

Epic: Product Management
    ├── Story: Add Product
    ├── Story: Edit Product
    └── Story: Delete Product
```

The team can later move Stories from the Backlog into a **Sprint**.

---

# 7. What is the Release tab?

The **Release** area is different from the Backlog.

A **Release/Version** represents a planned delivery of functionality, such as:

> Version 1.0
> Version 1.1
> Version 2.0

Stories can be associated with a particular **Fix Version/Release**.

For example:

```text
Release: Version 1.0
│
├── Login Story
├── Registration Story
├── Password Reset Story
└── User Profile Story
```

Once the Stories are completed and the release criteria are met, they can be included in that release.

### Important clarification

A Story is **not automatically created in both the Backlog and Release tab** simply because you create it.

Typically:

**Create Story → Story enters the project's work/backlog view → assign it to a Sprint and/or Fix Version (Release) as appropriate.**

---

# 8. What is the format for writing a Story?

The most common format is:

> **As a [type of user], I want [some goal], so that [some reason/benefit].**

### Example

> **As a customer, I want to receive an email confirmation after placing an order, so that I know my order has been successfully submitted.**

Breakdown:

| Part                                        | Meaning              |
| ------------------------------------------- | -------------------- |
| **As a customer**                           | Who needs it?        |
| **I want to receive an email confirmation** | What do they want?   |
| **So that I know my order was submitted**   | Why do they need it? |

---

# 9. What are Acceptance Criteria?

**Acceptance Criteria (AC)** are the **conditions that a Story must satisfy to be accepted as complete by the Product Owner/business**.

In simple words:

> **Acceptance Criteria define what must be true for the User Story to be considered successfully implemented.**

They remove ambiguity between the **business, developer, and tester**.

### Example Story

> **As a customer, I want to reset my password using my registered email address, so that I can regain access to my account if I forget my password.**

### Acceptance Criteria

**AC1:**
User can enter their registered email address and request a password reset.

**AC2:**
The system sends a password-reset email to the registered email address.

**AC3:**
The reset link expires after a defined period.

**AC4:**
User can enter and confirm a new password.

**AC5:**
The user can log in using the newly created password.

**AC6:**
The system displays an appropriate error when an unregistered email address is entered.

---

# 10. Acceptance Criteria using Given / When / Then

Acceptance Criteria can also be written using **Gherkin-style** syntax.

### Example

**Scenario: Successful password reset**

**Given** the user has a registered account
**When** the user requests a password reset
**Then** the system should send a password-reset email

Another scenario:

**Given** the user has received a valid reset link
**When** the user enters a valid new password
**Then** the system should update the password successfully

This format is particularly useful for **QA/testing and Behaviour-Driven Development (BDD)**.

---

# 11. Epic vs Story vs Task vs Sub-task

A useful Jira hierarchy to remember is:

```text
EPIC
 │
 ├── STORY
 │    ├── Task/Sub-task
 │    └── Task/Sub-task
 │
 ├── STORY
 │    ├── Task/Sub-task
 │    └── Task/Sub-task
 │
 └── STORY
```

### Simple analogy

Think about building a house:

**Epic:**
🏠 Build a House

**Stories:**

* Build foundation
* Build electrical system
* Build plumbing
* Build rooms
* Install doors/windows

**Tasks/Sub-tasks:**

* Order cement
* Dig foundation
* Install wiring
* Install pipes

The Epic is the **large goal**, Stories are the **valuable pieces of functionality/work**, and Tasks/Sub-tasks represent the **implementation work**.

---

## 12. Complete Jira Story example

### Epic

> **User Authentication**

### Story

> **As a registered user, I want to reset my password using my email address, so that I can regain access to my account if I forget my password.**

### Acceptance Criteria

```text
1. User can enter their registered email address.
2. System sends a password-reset email.
3. Reset link is valid only for the configured expiration period.
4. User can enter and confirm a new password.
5. New password must satisfy the password policy.
6. User can log in using the new password.
7. An appropriate error is displayed for an unregistered email.
```

### Jira fields you might commonly encounter

| Field               | Example                    |
| ------------------- | -------------------------- |
| Issue Type          | Story                      |
| Summary             | Implement password reset   |
| Description         | User Story                 |
| Epic                | User Authentication        |
| Priority            | High                       |
| Assignee            | Developer                  |
| Reporter            | Product Owner              |
| Sprint              | Sprint 12                  |
| Fix Version         | Release 1.0                |
| Acceptance Criteria | Conditions for acceptance  |
| Story Points        | 5                          |
| Status              | To Do → In Progress → Done |

### The overall flow

```text
Business Requirement
        ↓
      EPIC
        ↓
   Break into Stories
        ↓
Write User Story
        ↓
Define Acceptance Criteria
        ↓
Create Story in Jira
        ↓
Backlog
        ↓
Sprint Planning
        ↓
Sprint
        ↓
Development + Testing
        ↓
Acceptance
        ↓
Done
        ↓
Release / Version
```

**Key interview sentence to remember:**

> **An Epic is a large body of work that can be broken down into multiple User Stories. A User Story describes a specific piece of functionality from the user's perspective, while Acceptance Criteria define the conditions that must be satisfied for that Story to be accepted as complete.**

Yes. These are all connected to **Agile backlog refinement/grooming, Story preparation, estimation, Sprint planning, and testing**. Here’s a practical version you can use as notes.

# 1. What is Backlog Grooming?

**Backlog Grooming**, now more commonly called **Backlog Refinement**, is a meeting/activity where the Agile team reviews upcoming backlog items and makes sure they are ready for future Sprints.

The team typically:

* Reviews Epics and User Stories
* Clarifies requirements
* Discusses the User Story
* Defines/discusses Acceptance Criteria
* Identifies dependencies
* Identifies technical questions
* Breaks large Stories into smaller Stories if necessary
* Identifies subtasks
* Estimates complexity/effort
* Prioritizes or reorders items when needed
* Removes outdated or duplicate items

### Simple definition

> **Backlog Refinement is the process of reviewing and preparing backlog items so that they are sufficiently clear, sized, and understood before Sprint Planning.**

---

# 2. What happens in a Backlog Grooming meeting?

Imagine the Product Owner brings this requirement:

> **"As a client, I should be able to reset my password."**

The team discusses it.

### Requirement

> As a client, I should be able to reset my password.

A more standard User Story format would be:

> **As a client, I want to reset my password using my registered email address, so that I can regain access to my account if I forget my password.**

Then the team asks questions.

### Questions the team may ask

**Developer:**

> Do we already have an email service/API for sending the reset link?

**QA:**

> What should happen if the email address isn't registered?

**Developer:**

> How long should the reset link remain valid?

**Product Owner:**

> The link should expire after 30 minutes.

**QA:**

> Should the user be allowed to reuse an old reset link?

**Product Owner:**

> No.

These discussions help turn a vague requirement into something that can actually be developed and tested.

---

# 3. Discussing Acceptance Criteria

The team then discusses:

> **What conditions must be satisfied for this Story to be accepted?**

For the password reset Story:

### Acceptance Criteria

```text
1. Client can enter their registered email address.

2. System sends a password-reset email.

3. Reset link expires after 30 minutes.

4. Client can create a new password.

5. Password must comply with the defined password policy.

6. Client can log in using the new password.

7. System displays an appropriate message when an
   unregistered email address is entered.
```

This gives the **Developer** something to implement and the **QA** something to test.

---

# 4. "As a client, I should be able to..."

This is commonly used as a starting point for requirements, but the more standard User Story format is:

> **As a [user], I want [goal], so that [benefit].**

For example:

❌ Less complete:

> As a client, I should be able to download my invoice.

✅ Better User Story:

> **As a client, I want to download my invoice as a PDF, so that I can keep a copy for my records.**

Then Acceptance Criteria define exactly what "download my invoice" means.

---

# 5. Complexity vs Effort

These are related but not exactly the same.

### Complexity

Complexity asks:

> **How complicated is this work?**

Factors include:

* Technical difficulty
* Number of components involved
* Dependencies
* Unknowns
* Integration requirements
* Potential risks

### Effort

Effort asks:

> **How much work is required?**

For example:

| Story                     | Complexity |   Effort |
| ------------------------- | ---------- | -------: |
| Change button text        | Low        |    1 day |
| Create login API          | Medium     | 2–3 days |
| Build payment integration | High       |  5+ days |

---

# 6. "One person, one day = 1 effort"

You may hear this in some teams, but be careful with the terminology.

If your team's agreed estimation convention is:

> **1 person working for 1 day = 1 effort unit**

then:

**1 person × 1 day = 1 effort**

For example:

```text
1 person × 1 day = 1 effort
2 people × 3 days = 6 person-days
```

But this is **team-specific**.

Modern Scrum teams often use **Story Points** rather than person-days.

For example:

```text
1 → Very small
2 → Small
3 → Moderate
5 → Larger
8 → Complex
13 → Very large / should probably be split
```

Story Points generally represent a combination of **effort, complexity, uncertainty, and risk**, rather than literally meaning "5 days."

---

# 7. Story Points vs Effort

This is important for interviews.

### Effort

Can be expressed as:

> 3 person-days

### Story Points

Can be:

> 5 Story Points

You shouldn't automatically say:

> 5 Story Points = 5 days.

That's not necessarily true.

For example, a team might historically complete:

> 20 Story Points per Sprint.

That is the team's **velocity**.

---

# 8. What is a Sub-task?

A **Sub-task** is a smaller piece of work created under a Story or other parent issue where supported.

Example:

### Story

> As a client, I want to reset my password.

### Sub-tasks

```text
Story: Password Reset

├── Design password reset UI
├── Develop password reset API
├── Implement email notification
├── Implement password validation
└── Write automation/manual test cases
```

The Story represents the **user/business requirement**.

The Sub-tasks represent **work required to implement it**.

---

# 9. Does a Sub-task belong to a Sprint?

**Yes, typically a Sub-task is worked on as part of the Sprint containing its parent Story.**

Example:

```text
Sprint 15
│
└── Story: Password Reset
     │
     ├── Sub-task: Frontend
     ├── Sub-task: Backend API
     ├── Sub-task: Email service
     └── Sub-task: Testing
```

The exact Jira behavior can vary according to project configuration, but conceptually:

> **The Story is the Sprint-level unit of planned value; its Sub-tasks represent the work needed to complete that Story.**

---

# 10. What is API Testing?

**API Testing** tests the communication between software components through an API rather than testing only the user interface.

Suppose your application has:

```text
Frontend
    ↓
POST /api/login
    ↓
Backend
    ↓
Database
```

QA can test the API directly.

### Example request

```http
POST /api/login
```

```json
{
  "username": "user@example.com",
  "password": "Password123"
}
```

Expected response:

```json
{
  "status": "success",
  "token": "..."
}
```

The tester checks things such as:

* HTTP status code
* Response body
* Response headers
* Authentication
* Authorization
* Error handling
* Response time
* Input validation
* Database/data correctness

Common tools include **Postman**, **SoapUI**, and automated API-testing frameworks.

---

# 11. Non-Functional Testing

Functional testing asks:

> **Does the system do what it is supposed to do?**

Non-functional testing asks:

> **How well does the system perform that function?**

### Functional example

Requirement:

> User should be able to log in.

QA checks:

```text
Correct username + password
        ↓
Successful login
```

### Non-functional examples

QA may check:

* Performance
* Scalability
* Security
* Reliability
* Usability
* Availability
* Compatibility

For example:

> Can 10,000 users log in simultaneously without unacceptable performance degradation?

That's not simply checking whether login works; it's checking **how the system behaves under a particular condition**.

---

# 12. Stress Testing

**Stress Testing** is a type of performance testing where the system is pushed **beyond its expected/normal operating capacity** to understand how it behaves under extreme load.

### Example

Suppose an application normally expects:

> 10,000 concurrent users.

During stress testing, the team might progressively increase the load:

```text
5,000 users
      ↓
10,000 users
      ↓
20,000 users
      ↓
30,000 users
      ↓
40,000 users
```

The team observes:

* Response time
* Error rate
* CPU/memory utilization
* Throughput
* System failures
* Recovery behavior

The objective isn't simply:

> "Does it work?"

It's more like:

> **"What happens when we push the system beyond its expected capacity?"**

---

# 13. Load Testing vs Stress Testing

This distinction is frequently asked in interviews.

| Testing                    | Purpose                                             |
| -------------------------- | --------------------------------------------------- |
| **Load Testing**           | Test the system under expected/anticipated workload |
| **Stress Testing**         | Push the system beyond normal/expected capacity     |
| **Performance Testing**    | Broadly evaluate performance characteristics        |
| **Spike Testing**          | Test sudden increases/decreases in load             |
| **Endurance/Soak Testing** | Test sustained load over an extended period         |

### Simple example

If your application normally expects **10,000 users**:

**Load Test:**

> Can the application handle 10,000 users?

**Stress Test:**

> What happens at 20,000, 30,000, or more users?

**Spike Test:**

> What happens if the application suddenly jumps from 1,000 → 20,000 users?

**Soak Test:**

> Can the application handle 10,000 users continuously for 24 hours?

---

# 14. Putting everything together

Here's how these concepts connect in a real Agile project:

```text
BUSINESS REQUIREMENT
        ↓
      EPIC
        ↓
   USER STORY
        ↓
Backlog Refinement/Grooming
        ↓
 ┌───────────────────────┐
 │ Clarify requirement   │
 │ Discuss AC            │
 │ Identify dependencies │
 │ Estimate complexity   │
 │ Estimate effort       │
 │ Identify subtasks     │
 │ Identify testing      │
 └───────────────────────┘
        ↓
   Sprint Planning
        ↓
      SPRINT
        ↓
 ┌───────────────┐
 │ Development   │
 │ API Testing   │
 │ Functional QA │
 │ Non-functional│
 │ Testing       │
 └───────────────┘
        ↓
Acceptance Criteria met
        ↓
       DONE
        ↓
      RELEASE
```

### Interview-ready answer

> **Backlog Refinement is a collaborative Agile activity where the Product Owner, Developers, QA, and other relevant team members review upcoming backlog items. They clarify requirements, discuss acceptance criteria, identify dependencies and technical risks, break down work where necessary, and estimate complexity or effort. The objective is to make Stories sufficiently clear and ready for Sprint Planning.**

And remember this distinction:

**Epic = large body of work**
**Story = user/business requirement**
**Acceptance Criteria = conditions for accepting the Story**
**Sub-task = implementation work under a Story**
**Backlog Refinement = prepare and clarify upcoming work**
**Sprint = time-box in which the team works on selected backlog items**
**API Testing = test APIs directly**
**Non-functional Testing = test qualities such as performance/security/reliability**
**Stress Testing = test behavior beyond expected capacity**


