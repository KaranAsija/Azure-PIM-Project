# 06. Set up PIM Requests and Approval Process


## Objective

Enforce an approval workflow for all PIM role activations to enhance control and security.

---

## Steps

**1. Open Azure Portal and Access PIM**

* Go to https://portal.azure.com

* Sign in with Global Administrator or Privileged Role Administrator rights.

* In the left menu, select Azure Active Directory.

* Under Manage, select Privileged Identity Management.

**2. Configure Role Assignment and Approval Policies**

**a. Identify the Role or Group**

* Under PIM, select the appropriate scope:

  * Azure AD roles for directory roles

  * Azure resources for Azure subscriptions/resource roles

  * Groups for privileged access groups

* Choose the desired role (e.g., Global Administrator).

**b. Set Up Assignment**

* Click Assignments or Add assignments.

* Add the user as Eligible (preferred for JIT), not Active, unless required (e.g., break-glass).

* Set assignment start and end dates if the assignment is temporary.

**3. Configure Activation and Approval Settings**

* With your role selected, go to Settings or Role settings.

* For Activation maximum duration, set the maximum time per session (e.g., 1 hour).

* Under Require approval to activate, set to Yes.

  * Add one or more approvers (e.g., Security Admin, IT Lead).

* Toggle Require multifactor authentication as needed.

* Enable Require justification so users must explain their need for elevation.

* Configure Notification settings so approvers and SecOps receive alerts on activation.

* All above settings ensure each privilege elevation is thoroughly reviewed and controlled.

**4. User Activation (Request) Process**

* For an Eligible User:
  * Sign in to the Azure portal.

  * Navigate to PIM > My roles (for roles) or My requests (for group/resource access).

  * Click Activate beside the required eligible role or group.

  * Complete the activation form:

     * Enter justification (describing the business reason).

     * Choose duration (within the allowed policy).

     * Fulfill MFA (if required).

  * Submit the activation request.

**5. Approval Workflow**

* Approver(s) are instantly notified via email or portal notification.

* Approver reviews the request, justification, ticket (if configured), and context.

* Approver selects Approve or Deny:

   * If approved, the user is granted active privileges for the set duration.

   * If denied, the user is notified and privileges are not granted.

**6. Automatic Expiry and Audit Logging**

* Once the approved period ends, PIM automatically revokes the elevation.

* Every request, approval, denial, activation, justification, and notification is logged in PIM > Audit history for later review.

---

## **Approval Flow**

User requests activation ➔ Approver receives notification ➔ Approver approves ➔ User gains temporary privileged access ➔ Access expires after duration.

---

