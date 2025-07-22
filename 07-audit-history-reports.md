# 07. Analyze PIM Audit History and Reports


## Objective

Privileged Identity Management (PIM) provides built-in auditing and reporting to help organizations track privileged access, respond to suspicious activities, and support compliance requirements. Understanding and utilizing these capabilities is essential for maintaining a secure Azure AD environment.

---

## Key Features

**Compliance:** Meet regulatory mandates by proving who accessed what, when, for how long, and why.

**Security:** Detect and respond rapidly to unauthorized or suspicious elevation attempts.

**Accountability:** Ensure all privilege activations, approvals, and administrative changes are tracked.

**Operational Insight:** Review patterns, optimize access policies, and support incident investigations.

---

## Steps

**1. Open Azure Portal and Access PIM**

* Go to https://portal.azure.com

* Sign in with appropriate privileges (e.g., Global Admin, PIM admin).

* Navigate: Azure Active Directory > Privileged Identity Management.

**2. Select the Appropriate Audit Scope**

* Depending on what you want to audit, choose from:

    * Azure AD roles for directory role activations/changes.

    * Azure resources for subscription/resource activations/changes.

    * Groups for privileged access group membership changes.

**3. Access Audit History**

* Within your chosen scope, click Audit history or Audit log.

* You will see a structured list of events with columns such as:

    * Date/time

    * Event type (Activation, Assignment, Approval, Denial, etc.).

    * User (requestor, approver).

    * Role or group.

    * Status (Success, Failed).

    * Justification/reason.

**4. Filter and Search**

* Use filter controls to narrow by:

  * Specific user or group

  * Role

  * Event type (e.g., just activations or approvals)

  * Date range

**5. Drill Into Event Details**

* Click any entry for detailed context, including:

  * Who performed the action

  * Time and duration

  * Whether MFA or approval was required

  * Justification text

  * Linked ticket information (if configured)

* This enables forensic analysis of privilege usage.

**6. Export and Archive Audit Data**

* Click Download or Export to download audit data in CSV or JSON for external review, archiving, or integration with SIEM systems.

* Use this exported data for compliance reporting or deeper custom analytics.

---


