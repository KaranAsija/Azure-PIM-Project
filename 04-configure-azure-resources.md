# 03. Configure Azure resources in PIM


## Objective

Azure Privileged Identity Management (PIM) extends just-in-time access controls not only to directory roles, but also to resources such as Azure subscriptions, management groups, resource groups, and individual resources (like VMs). Configuring PIM for these resources ensures that critical cloud assets are protected and governed under the same access discipline as Azure AD roles.

---

## Key Features

**Limits Standing Privileges:** Assigns eligible, rather than permanent, rights to key resources.

**Reduces Risk Window:** Temporary access prevents long-term misuse or external attack.

**Enforces Approval and Audit:** Every privilege elevation is tracked, reviewable, and (optionally) requires sign-off.

**Supports Compliance:** Meets standards requiring access controls and full logging on sensitive resources.

--- 

## Steps

**1. Sign In and Open the Azure Portal**

* Go to https://portal.azure.com

* Sign in with a user account assigned as Global Administrator, Privileged Role Administrator, or Resource Owner.

**2. Open Privileged Identity Management for Azure Resources**

* In the left navigation pane, select Azure Active Directory.

* Under Manage, click Privileged Identity Management.

* In PIM, select Azure resources.

**3. Onboard (Register) the Resource for PIM**

* Click Discover resources.

* In the list, select the subscription, management group, or resource group you want to manage.

* Click Manage resource to register it with PIM if it’s not already managed.

* Only registered resources will be controlled via PIM.

**4. Assign Roles via PIM**

* For each onboarded resource, follow these steps:

  * Select the resource (e.g., Subscription1).

  * Click Manage -> Roles.

  * Choose a role (e.g., Owner, Contributor, Reader).

  * Click Add assignments.

Assignment options:

  * Assignment type: Choose between Eligible (can activate when needed) and Active (immediately assigned; use only for emergencies).

  * Select members: Choose users or groups.

  * Start date/End date: Optionally set a limited period for eligibility.

* Confirm and finalize the assignments.

**5. Configure Settings & Activation Policies**

* For each role (per resource), you can enforce additional controls:

  * Activation maximum duration: Set how long a user can be active per activation (e.g., 1 or 2 hours).

  * Multi-Factor Authentication: Require MFA on elevation.

  * Justification requirement: Force users to enter a reason each time they request activation.

  * Approval workflow: Designate one or more required approvers for each activation.

  * Notification: Enable alerting when activations occur.

  * Require ticket information: For integration with ITSM or helpdesk ticketing systems.

  To access these options:

  * Select the resource in PIM.

  * Navigate to Settings > Role settings.

  * Configure each parameter and save changes.

**6. User Activation Flow**

* For Eligible Users:

  * The eligible user goes to the Azure portal > PIM > Azure resources > My roles.

  * Selects the appropriate resource and role, then clicks Activate.

  * Fills in required justification, ticket number (if needed), and desired duration.

   Completes MFA if required.

  * If approval is needed, request is routed to approvers.

  * Upon approval, user’s permissions are elevated for the allowed period.



---

**Real-World Application**

Used by IAM and security teams to control administrative access for IT operations, deployments, and incident responses.
