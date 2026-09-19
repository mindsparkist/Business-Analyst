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


Yes — your flow is broadly correct. A few points need tightening because **Jira/Scrum practices vary by organization**, especially release timing and who is allowed to transition a Story to Done.

# 1. Traceability Matrix — RTM

A **Requirements Traceability Matrix (RTM)** is a document that connects each requirement to the corresponding **User Story, Acceptance Criteria, test cases, and test results**.

Its purpose is to answer:

> **"Can we trace every requirement from the original business requirement through development and testing to the final result?"**

### Simple example

| Requirement ID | Requirement             | Story  | Acceptance Criteria       | Test Case | Result |
| -------------- | ----------------------- | ------ | ------------------------- | --------- | ------ |
| REQ-001        | User should login       | ST-101 | Valid user can login      | TC-001    | Pass   |
| REQ-001        | User should login       | ST-101 | Invalid password rejected | TC-002    | Pass   |
| REQ-002        | User can reset password | ST-102 | Reset email sent          | TC-003    | Pass   |
| REQ-002        | User can reset password | ST-102 | Expired link rejected     | TC-004    | Fail   |

### How to make one

Start with the requirements:

```text
Business Requirement
        ↓
Epic
        ↓
Story
        ↓
Acceptance Criteria
        ↓
Test Case
        ↓
Test Result
        ↓
Defect, if any
```

In Jira, teams can achieve this through issue relationships, linked issues, test-management integrations, or dedicated test-management tools.

### Why is RTM useful?

It helps QA/management answer:

* Has every requirement been implemented?
* Has every requirement been tested?
* Which test cases cover this requirement?
* Which requirements failed?
* Which requirements have open defects?
* Are we ready for release?

---

# 2. Regression Testing

**Regression testing** means retesting existing functionality after a change to make sure that the change **has not broken previously working functionality**.

### Example

Suppose your application already has:

```text
Login
Search
Shopping Cart
Payment
Order History
```

The developer changes the **Payment** module.

QA tests the payment functionality, but they may also retest:

* Login
* Search
* Shopping Cart
* Order History

because changes in one component can affect other components.

### Simple definition

> **Regression testing verifies that recent code changes have not adversely affected existing functionality.**

### Regression vs Retesting

This is an important interview question.

**Retesting:**

> A defect was fixed → test the specific defect again.

**Regression testing:**

> A change was made → test existing functionality to make sure nothing else broke.

---

# 3. What is a Test Plan?

A **Test Plan** is a document that describes **what will be tested, how it will be tested, who will test it, when it will be tested, and what resources are required**.

Think of it as the QA team's roadmap.

### Typical Test Plan contents

```text
1. Test Objective
2. Scope
3. Out of Scope
4. Testing Types
5. Test Environment
6. Test Data
7. Roles & Responsibilities
8. Test Schedule
9. Entry Criteria
10. Exit Criteria
11. Risks & Dependencies
12. Defect Management
13. Tools
14. Deliverables
15. Approval
```

---

## Example

### Project

> E-commerce Website — Payment Module

### Objective

> Verify that customers can successfully complete payments using supported payment methods.

### In Scope

* Credit/debit card payment
* Payment confirmation
* Failed payment handling
* Refund functionality
* Payment API

### Out of Scope

* Third-party bank infrastructure
* Production infrastructure performance testing

### Testing

* Functional Testing
* API Testing
* Integration Testing
* Regression Testing
* Security Testing
* Performance Testing

### Entry Criteria

Testing can begin when:

* Build is deployed to QA
* Requirements are available
* Test environment is available
* Test data is available

### Exit Criteria

Testing can finish when:

* Planned test cases are executed
* Critical defects are resolved
* Acceptance Criteria are satisfied
* Required regression testing is completed
* Product Owner/authorized stakeholder accepts the result

---

# 4. Test Pyramid

The **Test Pyramid** describes how automated tests are generally distributed across different levels.

```text
             /\
            /  \
           / UI \
          /Tests \
         /--------\
        /   API    \
       / Integration\
      /--------------\
     /      Unit      \
    /      Tests       \
   /--------------------\
```

The basic idea is:

### Bottom — Unit Tests

Large number of tests.

Test individual functions/components.

> Fast and relatively inexpensive.

### Middle — Integration/API Tests

Test interactions between components/services.

> More comprehensive than unit tests but generally slower.

### Top — UI/End-to-End Tests

Test the application through the user interface.

> Usually slower and more expensive to maintain.

So generally:

> **More unit tests → fewer integration/API tests → fewer UI tests.**

---

# 5. When should a Release happen?

There isn't one universal rule that says:

> "Always release at the end of every Sprint."

There are two concepts you should separate:

### Sprint

A Sprint is a time-box in which the team works toward a Sprint Goal.

### Release

A Release is when functionality is actually made available to users/customers.

A Story can be:

```text
Developed
   ↓
Tested
   ↓
Accepted
   ↓
Done
```

without necessarily being immediately released to production.

---

## Common release models

### Model A — Release after every Sprint

```text
Sprint 1 → Release
Sprint 2 → Release
Sprint 3 → Release
```

This is common when the organization practices frequent delivery.

### Model B — Multiple Sprints → One Release

```text
Sprint 1 ─┐
Sprint 2 ─┼──→ Release 1.0
Sprint 3 ─┘
```

### Model C — Continuous Delivery

A completed and approved change can potentially be deployed independently of Sprint boundaries.

Therefore:

> **Sprint completion and Production Release are not necessarily the same event.**

---

# 6. Best day/time to release?

There is **no universally best day or time**.

Organizations normally choose a release window based on:

* Customer usage patterns
* Business impact
* Support availability
* Development availability
* QA availability
* Monitoring availability
* Rollback capability
* Change-management requirements
* Time-zone considerations
* Vendor/dependency availability

For a critical production system, teams often prefer a period when **appropriate engineering and support personnel are available** and customer impact is manageable.

The important principle is:

> **Don't choose a release time merely because it is convenient for development; choose a controlled window with sufficient support and rollback coverage.**

---

# 7. Sprint Planning — your understanding

You said:

> One day before the Sprint we would have Sprint Planning.

This **can** happen in a particular organization, but Scrum does not require Sprint Planning to be exactly one day before the Sprint.

Sprint Planning happens **at the beginning of the Sprint** and establishes:

1. Why is this Sprint valuable?
2. What can be accomplished?
3. How will the selected work be done?

---

# 8. What happens during Sprint Planning?

Your points are good. Let's organize them.

### 1. Review Product Backlog

The Product Owner presents the highest-priority work.

### 2. Discuss Stories

Team discusses:

* Requirements
* Acceptance Criteria
* Dependencies
* Technical complexity
* Risks
* Questions

### 3. Estimate effort

The team considers:

> How much work is involved?

This might use:

* Story Points
* Capacity/person-days
* Team-specific estimation methods

### 4. Check team capacity

For example:

```text
Developer A → 8 days available
Developer B → 7 days available
QA → 8 days available
Support → 5 days available
```

The team considers holidays, leave, meetings, production support, etc.

### 5. Consider historical velocity

Suppose the team historically completes around:

> 30 Story Points/Sprint

The team can use that as **one input** when determining how much work it may reasonably plan.

Velocity is **not a quota or guarantee**.

### 6. Confirm the Sprint Goal

The team agrees on the Sprint Goal and selected work.

Then the Sprint begins.

---

# 9. What about stakeholders?

One correction here:

> **Sprint Planning does not necessarily require every stakeholder to approve the Sprint before it starts.**

The core participants are generally:

* Product Owner
* Scrum Master
* Developers

Other stakeholders may provide information when appropriate.

The Product Owner is accountable for the Product Backlog and communicates priorities, while the Developers determine what work they can realistically take on based on their understanding and capacity.

---

# 10. Daily Stand-up

After the Sprint starts, the team normally has a **Daily Scrum**.

It's commonly called:

> Daily Stand-up

The **Developers are responsible for the Daily Scrum**.

The Scrum Master **facilitates/coaches the Scrum process** but isn't necessarily the "owner" of the meeting.

The purpose is to inspect progress toward the **Sprint Goal** and adapt the plan if necessary.

A common format is:

* What did I accomplish?
* What am I working on?
* What is blocking me?

But the formal Scrum purpose is more important than mechanically answering those three questions.

---

# 11. Your Dev → QA → PO flow

Your example is very realistic.

Suppose we have:

### Story

> As a customer, I want to download my invoice.

And subtasks:

```text
STORY: Download Invoice

├── Development
│   └── Implement invoice API
│
├── QA
│   └── Test invoice download
│
└── Support/Documentation
    └── Update support documentation
```

The Story should not be considered complete merely because development finished.

---

# 12. Developer completes development

Developer moves:

```text
To Do
   ↓
In Progress
   ↓
Ready for QA
```

The exact statuses depend on the Jira workflow.

QA then tests against:

* User Story
* Acceptance Criteria
* Functional requirements
* Relevant regression scenarios

---

# 13. What happens if QA finds a defect?

Suppose the Acceptance Criterion says:

> Customer must receive a PDF invoice.

QA discovers:

> Download produces an empty PDF.

QA should record a defect/bug according to the team's workflow.

Possible flow:

```text
Story
 ↓
Development
 ↓
QA
 ↓
Defect Found
 ↓
Bug Created
 ↓
Developer Fix
 ↓
QA Retest
 ↓
Pass
```

If the fix affects other functionality, regression testing may also be performed.

---

# 14. What if Product Owner/BA rejects the Story?

This is important.

Suppose QA passes everything, but the Product Owner says:

> "This doesn't satisfy the business requirement."

Then the Story should **not be treated as Done**.

Depending on the issue:

### Case 1 — Acceptance Criterion wasn't met

Developer makes the required change.

```text
PO/BA rejects
      ↓
Requirement clarified
      ↓
Developer updates
      ↓
QA tests again
      ↓
PO/BA verifies
      ↓
Accepted
```

### Case 2 — Requirement was unclear

The team discusses what the requirement actually means.

The Story or Acceptance Criteria may need clarification/update.

### Case 3 — New requirement

If the PO requests functionality that wasn't part of the original agreed scope, it may need to become **additional backlog work** rather than being silently added to the existing Story.

That's a very important Agile practice.

---

# 15. Who moves the Story to Done?

This is **workflow-specific**.

Your proposed practice:

> Developer moves it from To Do → In Progress; QA or BA/PO marks it Done after approval.

That is perfectly possible if your organization's Jira workflow is configured that way.

But Scrum itself does **not** prescribe:

> "Only QA can click Done."

What matters is that the team's **Definition of Done (DoD)** is satisfied.

For example:

```text
Definition of Done

✓ Development completed
✓ Code reviewed
✓ Unit tests passed
✓ QA testing passed
✓ Acceptance Criteria satisfied
✓ Critical defects resolved
✓ Required documentation completed
✓ Product Owner acceptance where required
```

Once the team's Definition of Done is satisfied, the Story is Done.

---

# 16. Definition of Done vs Acceptance Criteria

These are often confused.

### Acceptance Criteria

Specific to **one Story**.

Example:

> Password reset link expires after 30 minutes.

### Definition of Done

Applies to **all relevant Stories** or a defined class of work.

Example:

> Code reviewed, tests passed, no unresolved critical defects, documentation completed, etc.

So:

```text
Story
│
├── Acceptance Criteria
│    ├── AC1
│    ├── AC2
│    └── AC3
│
└── Definition of Done
     ├── Code Review
     ├── Testing
     ├── Documentation
     └── No critical defects
```

---

# 17. Sprint Report — what should you look for?

At the end of the Sprint, Jira provides various reports depending on the project configuration.

Important things to look at include:

### 1. Sprint Goal

First ask:

> **Did we achieve the Sprint Goal?**

This is more meaningful than simply counting tickets.

### 2. Completed vs incomplete work

For example:

```text
Planned:       35 Story Points
Completed:     30 Story Points
Not completed:  5 Story Points
```

Don't automatically interpret this as "the team performed badly." Investigate **why**.

Possible reasons:

* Requirement changed
* Dependency blocked work
* Production incident
* Unexpected technical complexity
* Story was too large
* Team member was unavailable
* External API/vendor issue

---

### 3. Sprint Burndown

A **Sprint Burndown Chart** shows remaining work over the Sprint.

Typical idea:

```text
Remaining
Work
 │\
 │ \
 │  \
 │   \
 │    \____
 │
 └──────────────
       Days
```

You're looking for:

* Is work getting completed?
* Is the team likely to achieve the Sprint Goal?
* Did work remain until the end?
* Were Stories added/removed during the Sprint?

---

### 4. Velocity

Look at velocity across **multiple Sprints**, not just one.

Example:

| Sprint   | Completed |
| -------- | --------: |
| Sprint 1 |        28 |
| Sprint 2 |        31 |
| Sprint 3 |        29 |
| Sprint 4 |        30 |

This gives the team historical information for future planning.

Velocity should **not** become:

> "Management demands 35 points every Sprint."

That can encourage unhealthy estimation behavior.

---

### 5. Carry-over Stories

Look at:

> What wasn't completed?

Then ask:

**Why?**

That's more useful than simply saying:

> "5 points were missed."

---

### 6. Defects

Review:

* Bugs found
* Severity
* Production defects
* Reopened defects
* Regression defects
* Defect resolution time

---

### 7. Blockers

Look for recurring blockers:

* Environment problems
* Dependency on another team
* Access issues
* API availability
* Unclear requirements
* Deployment problems

---

### 8. Cycle Time

How long does work take from:

> **In Progress → Done**

A rising cycle time may indicate:

* Stories are too large
* Too much work in progress
* Dependencies
* Review/testing bottlenecks
* Technical debt

---

# 18. A realistic end-to-end Jira/Scrum flow

This is the flow I'd recommend you remember for interviews:

```text
PRODUCT REQUIREMENT
        ↓
       EPIC
        ↓
      STORY
        ↓
BACKLOG REFINEMENT
        │
        ├── Clarify Story
        ├── Discuss AC
        ├── Identify Dependencies
        ├── Estimate
        └── Identify Risks
        ↓
SPRINT PLANNING
        │
        ├── Sprint Goal
        ├── Team Capacity
        ├── Prioritized Stories
        └── Historical Velocity
        ↓
      SPRINT
        ↓
    DEVELOPMENT
        ↓
      QA TESTING
        │
        ├── Functional Testing
        ├── API Testing
        └── Regression Testing
        ↓
   PO/BA ACCEPTANCE
        │
     ┌──┴──┐
     │     │
    YES    NO
     │     │
     ↓     ↓
   DONE   Clarify/Fix
           │
           └──→ QA/PO verification
        ↓
SPRINT REVIEW
        ↓
SPRINT RETROSPECTIVE
        ↓
REPORT / INSPECTION
        ↓
NEXT SPRINT / RELEASE
```

### The key distinction to remember

**QA says:**

> "I tested it and it meets the test conditions."

**PO/BA says:**

> "It satisfies the business requirement/Acceptance Criteria."

**Definition of Done says:**

> "The team's agreed completion conditions have been satisfied."

And the **Sprint Review** is where the team and stakeholders inspect the increment and discuss what was accomplished, while the **Retrospective** focuses on how the team worked and what can be improved.

The easiest way to remember the difference is:

> **Product Owner = What should we build and why?**
> **Scrum Master = How can the team work effectively using Scrum?**

## Product Owner vs Scrum Master

| Area                    | Product Owner (PO)                                 | Scrum Master (SM)                                        |
| ----------------------- | -------------------------------------------------- | -------------------------------------------------------- |
| **Primary focus**       | Product value                                      | Scrum/team effectiveness                                 |
| **Main question**       | What should we build? Why?                         | How can we work effectively?                             |
| **Owns**                | Product Backlog                                    | Scrum process                                            |
| **Prioritizes**         | Product Backlog                                    | Does not prioritize the product backlog                  |
| **Requirements**        | Clarifies business requirements                    | Helps the team understand/use Scrum                      |
| **Acceptance Criteria** | Defines/clarifies business expectations            | Helps facilitate clarification when needed               |
| **Stakeholders**        | Works closely with customers/business stakeholders | Helps facilitate stakeholder/team interactions           |
| **Sprint Planning**     | Explains priorities and desired outcomes           | Facilitates the Scrum event                              |
| **Daily Scrum**         | May attend, but isn't required                     | May facilitate/coach, but Developers own the Daily Scrum |
| **Sprint Review**       | Helps inspect the increment and gather feedback    | Facilitates the event                                    |
| **Retrospective**       | Participates                                       | Facilitates/coaches the process                          |
| **Team management**     | Not the team's manager                             | Not the team's manager                                   |
| **Technical decisions** | Usually doesn't dictate implementation             | Usually doesn't dictate implementation                   |
| **Success focus**       | Maximizing product value                           | Improving team effectiveness and Scrum adoption          |

---

# 1. Product Owner

The **Product Owner** represents the product/business perspective.

Their main responsibility is to **maximize the value of the product resulting from the Scrum Team's work**.

### Example

Suppose you're building a banking application.

The business says:

> Customers need to be able to reset their password.

The Product Owner helps establish what is actually required:

> As a customer, I want to reset my password using my registered email address, so that I can regain access to my account.

They may clarify:

* What should happen when the email is invalid?
* How long should the reset link remain valid?
* What password rules apply?
* What should the confirmation message say?
* Is this required for the next release?

The PO is heavily involved in **product priorities and requirements**.

---

# 2. Scrum Master

The **Scrum Master** focuses on helping the Scrum Team understand and apply Scrum effectively.

The Scrum Master is **not simply a meeting organizer**.

They help:

* Facilitate Scrum events
* Remove or help resolve impediments
* Coach the team in Scrum
* Help the organization understand Scrum
* Improve collaboration
* Encourage transparency and effective inspection/adaptation
* Help protect the team's ability to work toward the Sprint Goal

### Example

Suppose developers cannot test the password-reset Story because the QA environment has been unavailable for two days.

The Scrum Master might help the team identify and escalate the impediment:

> "The QA environment is blocking testing. Let's identify the responsible team and work on getting the environment restored."

The Scrum Master doesn't necessarily fix the server personally.

Their role is to **help the team and organization address the impediment**.

---

# 3. A simple real-world example

Imagine you're running a restaurant.

### Product Owner

The PO is thinking:

> "What food should we offer customers?"

They consider:

* Customer needs
* Business objectives
* Market requirements
* Priorities
* Value

### Scrum Master

The SM is thinking:

> "How can the kitchen team work effectively to deliver these dishes?"

They focus on:

* Collaboration
* Process
* Removing blockers
* Continuous improvement
* Effective Scrum practices

The **PO determines product direction/priorities**; the **SM enables effective Scrum and team collaboration**.

---

# 4. Who decides what goes into the Sprint?

This is an important distinction.

The **Product Owner** brings the highest-priority Product Backlog items and explains their value/requirements.

The **Developers** determine how much work they can realistically take into the Sprint based on their understanding and capacity.

The **Scrum Master** facilitates the Sprint Planning process and helps ensure Scrum is understood and followed.

So it's not:

> PO says "Take these 10 Stories."

Instead, there is collaboration.

```text
Product Owner
     │
     │ Priority + requirements
     ↓
Product Backlog
     │
     ↓
Sprint Planning
     │
     ├── PO → explains value/priorities
     ├── Developers → determine feasible work
     └── Scrum Master → facilitates/coaches
     ↓
Sprint Goal + Sprint Backlog
```

---

# 5. Who can reject a Story?

This is where your previous question about **Acceptance Criteria** becomes important.

Suppose:

> Story: Customer can download an invoice.

The Developer completes it.

QA tests it and reports that the functionality doesn't satisfy the Acceptance Criteria.

The Story isn't Done.

The PO/BA can also clarify that the delivered functionality doesn't satisfy the business requirement.

The Scrum Master doesn't normally decide:

> "This feature is acceptable from a business perspective."

That's primarily the **Product Owner/product side's responsibility**, while the team's Definition of Done determines whether the increment meets the team's agreed completion standard.

---

# 6. Who owns what?

A useful interview shortcut:

### Product Owner

**Owns/manages the Product Backlog and product priorities.**

Think:

> **PRODUCT**

### Scrum Master

**Serves the Scrum Team and helps the organization use Scrum effectively.**

Think:

> **PROCESS + TEAM EFFECTIVENESS**

### Developers

**Create the usable Increment.**

Think:

> **BUILD**

So:

```text
        PRODUCT OWNER
        "What & Why?"
             │
             ↓
       PRODUCT BACKLOG
             │
             ↓
      SCRUM MASTER
     "How can Scrum
      work effectively?"
             │
             ↓
        DEVELOPERS
        "Build it"
             │
             ↓
        INCREMENT
```

---

## Interview answer

If an interviewer asks:

**"What is the difference between a Product Owner and Scrum Master?"**

A strong concise answer would be:

> **The Product Owner is responsible for maximizing product value and managing the Product Backlog, including communicating and ordering product priorities. The Scrum Master is responsible for helping the team and organization understand and apply Scrum effectively, facilitating Scrum events, coaching the team, and helping remove impediments. In simple terms, the Product Owner focuses primarily on the product and its value, while the Scrum Master focuses primarily on Scrum effectiveness and the team's ability to work effectively.**

One important correction to a common misconception: **the Scrum Master is not the project manager or boss of the Developers, and the Product Owner is not the boss of the Developers either.** Scrum defines these as different accountabilities within the Scrum Team.

Yes. These are the next important concepts to learn for a **Jira + Agile QA workflow**. I'll organize them the way you would actually encounter them in a project.

# 1. Raising a Bug in Jira

A **bug/defect** is an unexpected behavior where the actual result differs from the expected requirement, Acceptance Criteria, or agreed behavior.

### Example

Requirement:

> User should be able to reset their password.

QA tests it.

**Expected Result:**

> Password reset email should be sent.

**Actual Result:**

> No email is received.

QA can raise a Jira Bug.

---

## Bug workflow

A common workflow is:

```text
Test Case
    ↓
Execute Test
    ↓
Actual Result ≠ Expected Result
    ↓
Raise Bug
    ↓
Developer investigates
    ↓
Bug Fixed
    ↓
QA Retests
    ↓
PASS ─────→ Close/Resolve
    │
    └─ FAIL → Reopen / Return to Development
```

The exact Jira statuses depend on your organization's workflow.

---

# 2. What information should you provide when raising a Bug?

This is extremely important in real IT work.

A developer should ideally be able to understand:

> **What happened, where did it happen, how can I reproduce it, what should have happened, and how serious is it?**

## Jira Bug Template

You can use this structure:

# Bug Title / Summary

**[Module] – [Short description of the problem]**

Example:

> **Login – User receives "500 Internal Server Error" with valid credentials**

---

## 1. Description

Briefly explain what the issue is.

Example:

> When a registered user attempts to log in with valid credentials, the application returns a 500 Internal Server Error instead of logging the user into the application.

---

## 2. Environment

* Environment: QA / UAT / Production
* Application Version/Build:
* Browser:
* Browser Version:
* Operating System:
* Device:
* API Version, if applicable:

---

## 3. Preconditions

Conditions that must exist before reproducing the issue.

Example:

* User must have a registered account.
* User account must be active.
* User must have valid credentials.
* Application must be accessible.

---

## 4. Steps to Reproduce

1. Open the application.
2. Navigate to the Login page.
3. Enter a valid username.
4. Enter a valid password.
5. Click **Login**.
6. Observe the result.

---

## 5. Expected Result

> User should be successfully logged into the application and redirected to the dashboard.

---

## 6. Actual Result

> Application displays a 500 Internal Server Error and the user is not logged in.

---

## 7. Severity

Example:

> High

Explain the impact if necessary.

---

## 8. Priority

Example:

> High

Priority may depend on business impact and release requirements.

---

## 9. Reproducibility

Example:

> 5/5 attempts

---

## 10. Attachments / Evidence

Attach relevant evidence:

* Screenshot
* Screen recording
* Error message
* Application logs
* API response
* Console logs
* Network trace
* Relevant request/response

---

## 11. Related Jira Items

* Story:
* Epic:
* Test Case:
* Related Bug:
* Release/Fix Version:

---

## 12. Additional Information

Include anything that may help investigation.

Example:

> Issue occurs only in the QA environment and was reproduced using Chrome and Edge.

### The golden rule

A good bug report should allow the developer to reproduce the problem **without having to come back to QA repeatedly for basic information**.

---

# 3. Severity vs Priority

Don't confuse these.

### Severity

> **How seriously does the defect affect the system?**

Examples:

* Critical
* High
* Medium
* Low

### Priority

> **How urgently should the business/team fix it?**

Example:

A cosmetic typo on the homepage may have:

> Low Severity + High Priority

if the page is being demonstrated to an important customer tomorrow.

Conversely, a serious issue in a rarely used administrative feature might have different business priority.

---

# 4. Test Scenario vs Test Case

This is another common interview question.

## Test Scenario

A **Test Scenario** is a high-level situation or functionality that needs to be tested.

Example:

> **Verify Login functionality.**

That's the overall testing area.

---

## Test Case

A **Test Case** provides the detailed steps, data, expected result, and conditions required to test something.

Example:

> Verify that a registered user can log in with valid credentials.

### Comparison

| Test Scenario                | Test Case                  |
| ---------------------------- | -------------------------- |
| High-level                   | Detailed                   |
| Describes what to test       | Explains how to test       |
| Usually broader              | Specific                   |
| Can have multiple test cases | Tests a specific condition |

Example:

**Scenario:**

> Test Login functionality.

**Test Cases:**

```text
TC-001 → Login with valid credentials
TC-002 → Login with invalid password
TC-003 → Login with invalid username
TC-004 → Login with blank username
TC-005 → Login with blank password
TC-006 → Account locked after repeated failures
TC-007 → Password field masks characters
```

---

# 5. What is a Precondition?

A **Precondition** is something that must be true or already set up **before you execute the test**.

Example:

### Test Case

> Verify successful login.

### Preconditions

```text
1. Application is available.
2. User has a registered account.
3. User account is active.
4. Valid username and password are available.
```

Then you execute the test.

---

# 6. Negative Test Cases

A **negative test case** verifies how the system behaves when the user provides **invalid, unexpected, missing, or unacceptable input**.

### Positive test

```text
Valid username
+
Valid password
        ↓
Successful Login
```

### Negative tests

```text
Invalid username
        ↓
Error message
```

```text
Valid username
+
Invalid password
        ↓
Login rejected
```

```text
Blank username
        ↓
Validation message
```

```text
SQL/script/special input
        ↓
Application handles input safely
```

Negative testing is important because a good system should not only work when everything is correct—it should also handle incorrect conditions appropriately.

---

# 7. Test Closure / Test Closure Report

At the end of testing, QA performs **Test Closure**.

The objective is to formally conclude the testing activity and communicate the final testing status.

A Test Closure Report may contain:

```text
Test Closure
│
├── Scope tested
├── Test cases planned
├── Test cases executed
├── Passed
├── Failed
├── Blocked
├── Defects raised
├── Defects closed
├── Outstanding defects
├── Regression results
├── Risks
├── Environment information
└── Final QA assessment
```

### Example

| Metric             | Result |
| ------------------ | -----: |
| Test Cases Planned |    150 |
| Executed           |    150 |
| Passed             |    142 |
| Failed             |      8 |
| Blocked            |      0 |
| Critical Defects   |      0 |
| High Defects       |      0 |
| Medium Defects     |      2 |
| Low Defects        |      4 |
| Deferred           |      2 |

The numbers above are just an **illustrative example**, not a recommended release threshold.

---

# 8. Handing over to Support

Once a release is ready, the QA/Project team may provide information to the **Application/Production Support team**.

This is commonly called a:

> **Knowledge Transfer / Handover**

Support should know enough to operate and troubleshoot the application after release.

### Information to provide

**Application information**

* Application name
* Version/release
* Major changes
* New functionality

**Known Issues**

* Known defects
* Workarounds
* Limitations

**Operational information**

* Monitoring
* Logs
* Health checks
* Dependencies
* Scheduled jobs

**Troubleshooting**

* Common errors
* Error messages
* First-level troubleshooting steps
* Escalation procedure

**Support**

* L1 responsibilities
* L2 responsibilities
* L3/development escalation
* Contact/ownership information

**Documentation**

* Runbook
* Release notes
* Knowledge articles
* Architecture/reference documentation

---

# 9. Types of Testing — Big Picture

There are several different ways to classify testing.

This is where beginners often get confused because:

> **Functional/Non-functional**, **Black-box/White-box**, and **Smoke/Regression/Integration/etc.** are different classification dimensions.

Think of it like this:

```text
                    SOFTWARE TESTING
                          │
          ┌───────────────┴───────────────┐
          │                               │
     FUNCTIONAL                     NON-FUNCTIONAL
          │                               │
    Does it work?                  How well does it work?
```

And separately:

```text
              TESTING APPROACH
                    │
          ┌─────────┴─────────┐
          │                   │
      BLACK-BOX           WHITE-BOX
```

And separately:

```text
             TESTING LEVEL / PURPOSE
                    │
     ┌──────────────┼───────────────┐
     │              │               │
 Component      Integration      System
 Testing        Testing          Testing
                    │
              Regression
              Smoke/Sanity
```

These categories can overlap.

---

# 10. Component Testing

**Component Testing** tests an individual component/module in isolation or near isolation.

Example:

An application contains:

```text
Login
Payment
Search
Reporting
```

Testing the **Login component** independently is component testing.

It is sometimes called **Module Testing** or **Unit Testing** depending on the context, although terminology varies.

---

# 11. Integration Testing

Integration testing checks whether **two or more components work correctly together**.

Example:

```text
Login UI
    ↓
Login API
    ↓
Authentication Service
    ↓
Database
```

You may test whether these components correctly communicate.

Another example:

```text
Order System
     ↓
Payment Gateway
     ↓
Bank/Payment Provider
```

You're testing the **interaction between systems/components**.

---

# 12. Smoke Testing

**Smoke Testing** is a relatively broad, shallow check to determine whether a build is stable enough for more detailed testing.

Example after a new build arrives:

```text
✓ Application opens
✓ Login works
✓ Main dashboard loads
✓ Search works
✓ Basic transaction works
```

If these basic checks fail badly, QA may reject the build for deeper testing.

Think:

> **"Is this build testable?"**

---

# 13. Sanity Testing

**Sanity Testing** is usually a focused check after a specific change or fix to determine whether the relevant functionality is behaving correctly.

Example:

Developer fixes:

> Password reset bug.

QA performs targeted checks:

```text
✓ Password reset works
✓ Reset email is sent
✓ New password works
```

Think:

> **"Did this particular change/fix work as expected?"**

Terminology and exact distinction between smoke and sanity can vary across organizations, so use your project's definitions when discussing them.

---

# 14. Regression Testing

Regression testing asks:

> **Did this change break something that was already working?**

Example:

Payment code changed.

QA tests:

```text
Payment
+
Cart
+
Order creation
+
Order history
+
Refund
```

because the change could affect related functionality.

---

# 15. Functional Testing

Functional testing asks:

> **Does the system perform the required function correctly?**

Example requirement:

> User should be able to transfer money.

Functional tests check:

* Transfer succeeds with valid information
* Invalid account is rejected
* Insufficient balance is handled
* Appropriate confirmation is displayed

The focus is on **what the system does**.

---

# 16. Non-Functional Testing

Non-functional testing asks:

> **How well does the system perform?**

Examples:

### Performance

How quickly does it respond?

### Load

Can it handle expected workload?

### Stress

What happens beyond expected capacity?

### Security

Can unauthorized users access protected functionality?

### Usability

Is the application reasonably usable?

### Reliability

Does it remain stable over time?

---

# 17. Black-Box Testing

In **Black-box testing**, the tester focuses on the system's **inputs and outputs without needing to know the internal implementation/code**.

Example:

```text
Input
  ↓
[ Application ]
  ↓
Output
```

Tester doesn't need to know whether the developer implemented it using Java, Python, C#, etc.

Example:

```text
Username: shuv@example.com
Password: ValidPassword
        ↓
     Login API
        ↓
Expected: HTTP 200 + successful login
```

---

# 18. White-Box Testing

**White-box testing** involves knowledge of the internal code, logic, structure, paths, or implementation.

Developers commonly perform this type of testing.

Example:

```text
if passwordValid:
       login()
else:
       reject()
```

Tests can be designed around branches/conditions in that code.

Common areas include:

* Code paths
* Conditions
* Branches
* Loops
* Statement coverage

---

# 19. Quick comparison table

| Testing Type         | Main Question                                          |
| -------------------- | ------------------------------------------------------ |
| **Component**        | Does this individual component work?                   |
| **Integration**      | Do components work together?                           |
| **System**           | Does the complete system work?                         |
| **Smoke**            | Is this build stable enough for testing?               |
| **Sanity**           | Does the specific change/fix work correctly?           |
| **Regression**       | Did the change break existing functionality?           |
| **Functional**       | Does the system do what it should?                     |
| **Non-functional**   | How well does it work?                                 |
| **Black-box**        | Can I test behavior without knowing the internal code? |
| **White-box**        | Does the internal code/logic behave correctly?         |
| **Positive testing** | Does it work with valid input?                         |
| **Negative testing** | Does it handle invalid/unexpected input correctly?     |

---

# 20. One complete example

Imagine your team develops a **Login feature**.

### Requirement

> As a registered user, I want to log in so that I can access my account.

### Test Scenario

> Verify Login functionality.

### Test Cases

```text
TC01 → Valid username + valid password
TC02 → Invalid username + valid password
TC03 → Valid username + invalid password
TC04 → Blank username
TC05 → Blank password
TC06 → Locked account
TC07 → Multiple failed attempts
```

### Precondition

> Active user account exists.

### Test Execution

Suppose TC03 fails.

**Expected:**

> Error: Invalid username or password.

**Actual:**

> Application crashes with HTTP 500.

### Raise Jira Bug

```text
BUG-123

Summary:
Login - Application returns HTTP 500 for invalid password

Environment:
QA

Precondition:
Active user account exists

Steps:
1. Open login page
2. Enter valid username
3. Enter invalid password
4. Click Login

Expected:
User should receive an appropriate authentication error.

Actual:
Application returns HTTP 500 and displays a server error.

Severity:
High

Priority:
High

Reproducibility:
5/5

Evidence:
Screenshot + API response + logs

Related Story:
ST-101
```

Then:

```text
Developer fixes
      ↓
QA retests BUG-123
      ↓
PASS
      ↓
Regression testing
      ↓
Test Closure
      ↓
Release / Handover
      ↓
Support
```

That is a very realistic **Agile + Jira + QA lifecycle** to understand for an IT support/QA/project environment.
