# 02. Just-In-Time (JIT) Privileged Access


## Concept

**Just-In-Time (JIT)** access is a principle and operational feature in Azure PIM that allows users to activate privileged roles only when needed, for a strictly limited period. This minimizes the exposure of sensitive rights in your environment and supports a strong “zero standing privilege” security stance.

---

## Key Benefits

* Reduces Risk: Avoids having permanent admin accounts that can be compromised.

* Enhanced Auditability: Every privilege elevation is logged and fully reviewable.

* Supports Compliance: Meets strict regulatory standards for access control and privilege management.

* Enforces Least-Privilege: Users only possess high-level privileges for the minimum time required.

## Steps

**1. Set Up Eligible Role Assignment**

* Open Azure Portal: Go to https://portal.azure.com.

* Navigate to PIM:

   * Select Azure Active Directory -> Privileged Identity Management.

* Assign User as Eligible:

   * Click Azure **AD** roles -> Roles.

   * Pick the privileged role (e.g., Global Administrator).

   * Click Add assignments.

   * Choose the user and set as Eligible.

   * (Optional) Specify start and end dates for their eligibility.

**2. Configure JIT Activation Policies**

For each eligible assignment, set the following controls:

* Activation Duration: Specify the maximum time (e.g., 1 hour) per session.

* Approval Workflow:

   * Define if **manager/peer** approval is required before activation.

* Multi-Factor Authentication (MFA): Enforce MFA before the role is activated.

* Justification: Require the user to enter a business reason for each request.

* Notifications: Set up emails/alerts to admins or SOC for activation events.

**3. User Initiates JIT Role Activation**

* Sign In: The eligible user logs into the Azure portal.

* Go to My Roles in PIM:

   * Azure AD -> Privileged Identity Management -> My roles.

* Request Activation:

   * Find the desired eligible role and click Activate.

   * Fill out any required justification, select desired (within policy) duration.

   * Complete MFA if prompted.

* Approval Process (if configured):

   * The request is sent to the designated approvers.

   * Approvers are notified and grant/deny access after reviewing justification.

**4. Active Session and Rights Usage**

* Upon approval, the role changes to Active for the user.

* The user performs required administrative activities.

* All activities are tracked and logged for audit.

**5. Automatic Expiry and Reversion**

* When the activation duration ends, PIM automatically reverts the assignment from Active back to Eligible.

* Any attempts to retain privileges longer require submitting a new request.

* Security operations and audit teams can review every activation, justification, approval, and activity through the PIM audit logs.

---

## Example:
UserA has "eligible" access to the Global Administrator role. When they need admin privileges, they request activation through PIM, provide justification, and receive access for 1 hour.


