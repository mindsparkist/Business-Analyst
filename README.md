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
