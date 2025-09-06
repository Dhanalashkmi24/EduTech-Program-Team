# EduTech-Program-Team

# ServiceNow Project Documentation

## Project Title

ServiceNow Educational Organization Management

## Team Id:

\[Enter Your Team ID]

## Team Members:

* **Team Leader:** \[Name]
* **Team Member 1:** \[Name]
* **Team Member 2:** \[Name]
* **Team Member 3:** \[Name]

---

## Problem Statement

Managing users, groups, roles, tables, and workflows manually in an educational organization is time-consuming and prone to errors. ServiceNow provides an efficient way to automate these tasks by creating structured processes for user management, access control, and workflow automation.

---

## Objective

* To create and manage **users, groups, and roles** in ServiceNow.
* To design **custom tables** for project and task tracking.
* To assign **users to groups and roles** for controlled access.
* To implement **application access, ACLs, and flows** for streamlined automation.

---

## Skills

* ServiceNow Platform Navigation
* User, Group, and Role Management
* Table and Application Module Creation
* Access Control Lists (ACLs)
* Flow Designer Automation

---

# Task Initiation

## Milestone 1: Users

### Activity 1: Create Users

1. Open ServiceNow.
2. Click on **All → search for Users**.
3. Select **Users** under *System Security*.
4. Click on **New**.
5. Fill the required details to create a new user.
6. Click on **Submit**.

**Create another user:**
7\. Repeat the process with different user details.
8\. Click on **Submit**.

---

## Milestone 2: Groups

### Activity 1: Create Groups

1. Open ServiceNow.
2. Click on **All → search for Groups**.
3. Select **Groups** under *System Security*.
4. Click on **New**.
5. Fill the details to create a new group.
6. Click on **Submit**.

---

## Milestone 3: Roles

### Activity 1: Create Roles

1. Open ServiceNow.
2. Click on **All → search for Roles**.
3. Select **Roles** under *System Security*.
4. Click on **New**.
5. Fill the details to create a new role.
6. Click on **Submit**.

**Create another role:**
7\. Repeat the process to create a second role.
8\. Click on **Submit**.

---

## Milestone 4: Tables

### Activity 1: Create Tables

1. Open ServiceNow.
2. Click on **All → search for Tables**.
3. Select **Tables** under *System Definition*.
4. Click on **New**.
5. Fill the following details:

   * **Label:** Project Table
   * Check **Create Module** & **Create Mobile Module**
6. Enter **New Menu Name:** Project Table.
7. Add required table columns.
8. Click on **Submit**.

**Create another table:**
9\. Create another table named **Task Table 2** and add required columns.
10\. Click on **Submit**.

---

## Milestone 5: Assign Users to Groups

### Activity 1: Assign Users to Project Team Group

1. Open ServiceNow.
2. Click on **All → search for Groups**.
3. Select the **Project Team Group**.
4. Under **Group Members**, click **Edit**.
5. Select **Alice P** and **Bob P** and save.

---

## Milestone 6: Assign Roles to Users

### Activity 1: Assign Roles to Alice User

1. Open ServiceNow → **All → search for Users**.
2. Select the **Project Manager User**.
3. Under the user profile, click **Edit**.
4. Assign **Project Member** role.
5. Add roles: `u_project_table` and `u_task_table`.
6. Save and update the form.

### Activity 2: Assign Roles to Bob User

1. Open ServiceNow → **All → search for Users**.
2. Select **Bob P User**.
3. Under the user profile, click **Edit**.
4. Assign **Team Member** role and table role.
5. Save changes.
6. Click **Profile Icon → Impersonate User → Bob**.
7. Verify that **Task Table 2** is visible.

---

## Milestone 7: Application Access

### Activity 1: Assign Table Access to Application

1. When creating a table, an application & module is auto-created.
2. Go to **Application Navigator → search for Project Table Application**.
3. Click on **Edit Module** and assign **Project Member** role.
4. Search for **Task Table 2 → Edit Application**.
5. Assign **Project Member** and **Team Member** roles.

---

## Milestone 8: Access Control List (ACL)

### Activity 1: Create ACL

1. Open ServiceNow.
2. Click on **All → search for ACL**.
3. Select **Access Control (ACL)** under *System Security*.
4. Click on **Elevate Role** if required.
5. Click on **New**.
6. Fill details to create a new ACL.
7. Under **Requires Role**, add **Task Table** and **Team Member Role**.
8. Click on **Submit**.

**Repeat to create 4 ACLs for different fields as required.**

9. Go to **Profile → Impersonate User → Bob**.
10. Navigate to **Task Table 2**.
11. Verify that **Comment** and **Status** fields have edit access.

---

## Milestone 9: Flow

### Activity 1: Create a Flow to Assign Operations Ticket to Group

1. Open ServiceNow.
2. Navigate to **All → Flow Designer → New → Flow**.
3. Enter **Flow Name:** Task Table.
4. Application: **Global**.
5. Build the flow.

**Add a Trigger**

* Trigger: **Create Record**
* Table: **Task Table**
* Conditions:

  * Status = In Progress
  * Comments = Feedback
  * Assigned to = Bob

**Add Action – Update Records**

* Record: Task Table
* Field: Status → Value: Completed

**Add Action – Ask for Approval**

* Record: Task Table
* Approver: **Alice P**
* Approval Field: Status

6. Save and activate the flow.
7. Verify:

   * Status updates to *Completed*.
   * Approval request sent to Alice P.
   * Alice approves via **My Approvals → Approve**.

---

## Conclusion

This project demonstrates how **ServiceNow can be used to manage an educational organization’s IT resources** by efficiently handling users, groups, roles, tables, ACLs, and workflows. The implementation improves security, reduces manual effort, and ensures streamlined operations through automation.

---

### Notes & Next Steps

* Replace placeholder names and IDs with your team’s actual details.
* Add screenshots taken from your demo video under each milestone to increase clarity (place images in an `images/` folder and reference them using `![alt text](images/screenshot1.png)`).
* Optionally, include your demo video link under a **Demo Video** section by adding the Drive or YouTube link.

---

*End of documentation - Prepared for GitHub README.md*
