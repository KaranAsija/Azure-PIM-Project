# 05. Configure Privileged Access Groups


## Concept

**Privileged Access Groups (PAGs)** in Azure Active Directory (Azure AD) enhance Just-in-Time (JIT) access controls by extending them to group membership. With PAGs, group-based access can be tightly governed for administrative and highly privileged activities, ensuring least-privilege, time-bound, and auditable access across Azure and integrated applications.

---

## Steps

**1. Sign In to Azure Portal**

* Navigate to https://portal.azure.com.

* Log in with a Global Administrator or Privileged Role Administrator account.

**2. Create and Prepare the Security Group**

* Go to Azure Active Directory -> Groups -> New Group.

* Select Security as the group type.

* Enable the following options:

   * Azure AD roles can be assigned to the group.

   * Assign a name, e.g., NetworkAdmins or ServerAdmins.

* Optionally, assign roles (e.g., Exchange Admin, Intune Admin) directly to the group.

**3. Enable the Group for Privileged Access in PIM**

* Go to Azure Active Directory > Privileged Identity Management > Groups.

* Click Discover groups.

* Select the previously created group and click Enable PIM (or “Manage group” for PIM).

**4. Assign Eligible and Active Memberships**

* Under the group in PIM, choose Assignments.

* Click + Add assignments.

* In the assignment dialog:

   * Assignment type: Select Eligible for users who should request temporary access or Active for break-glass scenarios.

   * Users/Groups: Select who can be assigned.

   * Start/End date: (Optional) to make assignment temporary.

* Confirm and create the assignments.

**5. Configure Group Activation Settings**

* Within the group in PIM, go to Settings or Group settings.

* Set:

   * Activation maximum duration: e.g., 1 hour.

   * Require approval: Set to Yes if activation needs review and select approvers.

   * Require MFA: Enforce multifactor at activation.

   * Justification requirement: Prompt the user for business reason.

   * Notification: Configure alerts for group activations.

   * Other options: Ticketing (for change control), eligible/active limits.

* Save your configuration.

**6. User Activation Workflow**

* Eligible users do not belong to the group by default.

* The user logs into Azure and goes to PIM -> Groups -> My groups.

* They find the eligible group and click Activate.

* The user is prompted for:

   * Duration (cannot exceed policy maximum)

   * Justification and, if configured, ticket number

   * MFA challenge (if required)

* If approval is enabled, the request is sent to assigned approvers.

* Once approved, the user becomes an active group member for the specified time.

* After the activation expires, membership is automatically revoked.

---

**Best Practice**

Use for managing large admin groups to simplify workflows and reduce direct individual role assignments.
