# 06. Set up PIM Requests and Approval Process


## Objective

Enforce an approval workflow for all PIM role activations to enhance control and security.

---

## Steps

* Step 1: Eligible user signs in to Azure portal, navigates to PIM, and requests to activate a role or group membership.

* Step 2: User provides justification and selects desired duration (within allowed limit).

* Step 3: If approval required, designated approver receives email/portal notification.

* Step 4: Approver reviews request, can see justification and context, then approves or denies.

* Step 5: Upon approval:

  * User receives confirmation.

  * Role is activated for the specified time (enforced by PIM).

  * All activity is logged.

* Step 6: After duration expires, elevated access is revoked.

---

## **Approval Flow**

User requests activation ➔ Approver receives notification ➔ Approver approves ➔ User gains temporary privileged access ➔ Access expires after duration.

---

