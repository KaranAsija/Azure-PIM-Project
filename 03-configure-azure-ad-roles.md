# 03. Configure Azure roles in PIM


## Objective

Implementing PIM for Azure AD roles is critical for limiting the risk of excessive or misused privileged access. The process involves onboarding high-privilege roles to PIM, customizing activation and approval settings, and maintaining clear, auditable assignments.

---

## Steps

**1. Open Azure AD in the Azure Portal**

* Navigate to https://portal.azure.com.

* Sign in with an account that has Global Administrator or Privileged Role Administrator rights.

**2. Access Privileged Identity Management**

* In the left-hand menu, select Azure Active Directory.

* **Under Manage,** click Privileged Identity Management.

* Click Azure AD roles to **manage** directory roles with PIM.

**3. Onboard Roles into PIM**

* Within Azure AD roles, click Roles to see all eligible roles.

* Identify roles that are highly privileged or sensitive, such as:

  * Global Administrator

  * Security Administrator

  * User Administrator

  * Application Administrator

* For each role, click on it and ensure it is enabled for PIM management.

**4. Assign Users as Eligible or Active**

* In the chosen role (e.g., Global Administrator), click Add assignments.

* In the assignment dialog:

  * Select users: Choose the users to be assigned.

  * Assignment type: Set as Eligible (can request activation) or Active (immediate assignment, generally for break-glass accounts).

  * (Optional) Configure start and end dates for temporary eligibility.
    
  * Finalize by clicking Add or Assign.

**5. Configure Role Activation Settings**

* For each onboarded role, set up robust security requirements.

 * **Set Activation Duration:** Choose the maximum session time allowed per activation (e.g., 1 hour, 2 hours).

 * **Require Multi-Factor Authentication (MFA):** Toggle to require an extra authentication step at activation time.

 * **Mandate Justification:** Require the user to provide a business reason each time they activate the role.

 * **Approval Workflow:** Specify if activation requires review and approval.

 * Assign one or more approvers for the role (e.g., another admin, team lead).

 * **Notifications:** Enable email or portal alerts for each activation to inform security or monitoring personnel.

 How to Set These:

 * Within the role’s page in PIM, click Settings or Role settings.

 * Adjust the parameters detailed above and save changes.


---

**Best Practices**

* Default to Eligible status for all privileged roles; only use Active for break-glass/emergency accounts.

* Require approval and MFA for all sensitive roles.

* Keep activation durations as short as operationally possible.

* Document all assignment and policy decisions as part of compliance.
