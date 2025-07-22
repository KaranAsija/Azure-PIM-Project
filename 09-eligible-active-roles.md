# 09. Explore Eligible and Active Roles


## Definitions

**Eligible Role:**
* An assignment status indicating a user can request temporary activation of a privileged role when needed, but does not have ongoing access.

* Supports the “just-in-time” security principle and is preferred for routine admin staff.

**Active Role:**

* A status where the user currently holds the permissions of a privileged role.

* Access is either permanent (rare, typically for break-glass accounts) or granted temporarily after activation.
---

## Steps

**1. Open Azure AD in the Portal**

* Go to https://portal.azure.com.

* Sign in as a Global Administrator.

**2. Assign a Role as Eligible**

* In the left menu, navigate to Azure Active Directory > Privileged Identity Management.

* Select Azure AD roles > Roles.

* Choose the desired privileged role (e.g., Global Administrator).

* Click Add assignments.

**In the assignment window:**

* Select the user(s) you wish to grant eligibility.

* Set Assignment type to Eligible (not Active).

* (Optional) Set start and end dates for the eligibility if necessary.

* Confirm and complete the assignment.

**3. Setting Up Activation Controls**

* For each eligible role assignment, configure:

   * Activation duration: E.g., 1 hour per activation.

   * MFA requirement: Enforce multi-factor authentication for role activation.

   * Justification requirement: Require a business reason before approval.

   * Approval workflow: Specify approvers if activation must be reviewed.

   * Notification: Set up alerts to security or admin staff when activations occur.

**4. User Requests (Activates) the Role**

* The eligible user:

   * Signs in to the Azure portal.

   * Navigates to Azure AD > Privileged Identity Management > My roles.

   * Locates the eligible role and clicks Activate.

   * Fills in any required justification, selects the desired duration, and completes MFA.

   * If approval is required, the request is sent to the designated approver.

   * Upon approval, the role status changes from Eligible to Active, and the user’s permissions are elevated for the approved period.

**5. Returning to Eligible State**

* After the activation duration ends, Azure PIM automatically reverts the user back to Eligible status.

* All actions and activations are logged for auditing.

---

**Example**

Activate Security Administrator role for 1 hour to reset user passwords, after which access expires automatically.
