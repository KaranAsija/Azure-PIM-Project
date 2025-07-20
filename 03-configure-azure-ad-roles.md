# 03. Configure Azure AD Roles in PIM


## Objective

Configure Azure AD roles in PIM to enforce Just-In-Time activation and approval workflows for least privilege management.

---

## Theoretical Steps

**Onboard Roles to PIM**

* Navigate to Azure Active Directory > Privileged Identity Management > Azure AD roles.

* Select “Manage” and choose “Roles".

* Choose the role (e.g., Global Administrator), then select “Assign” to onboard it into PIM.

**Settings**

* Activation Duration: Set time (e.g., 1 hour per activation).

* Approval: Require approval from specified users or roles before activation.

* Multi-factor Authentication (MFA): Enforce MFA at activation.

* Justification: Ask users to provide reasons for activation.

**Assign Eligible Users**
* Assign users as “Eligible” for specific roles:

* Eligible users can activate their role as needed.

* Assignments can be permanent or time-bound.

## Sample Assignment Table:
| User |	Role | Assignment | Type | Approval Required | Duration |
|------|-------|------------|------|---------------------|----------|
| UserA |	Global | Admin | Eligible|	Yes |	1 hour |
|UserB |	Security | Admin |	Permanent |	No |	N/A |


---

**Real-World Application**

Used by IAM and security teams to control administrative access for IT operations, deployments, and incident responses.
