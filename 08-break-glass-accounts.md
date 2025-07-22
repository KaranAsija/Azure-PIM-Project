# 08. Create and Manage Break-Glass Accounts

## Concept

**Break-glass accounts** are emergency administrative accounts designed to provide uninterrupted access to critical environments when standard privileged access methods (like PIM-controlled accounts or MFA) are unavailable. These accounts are a vital component of business continuity and security planning.

---
## Purpose of Break-Glass Accounts

* Ensure at least one method of administrative access during outages, lockouts, or misconfiguration (e.g., MFA failures, disabled Conditional Access).

* Enable rapid recovery from identity-related incidents.

* Satisfy compliance standards that require a secure, always-available path for emergency intervention.

## Steps

**1. Open Azure AD in the Portal**
* Navigate to: https://portal.azure.com

* Sign in as a Global Administrator.

**2. Create Break Glass Accounts**

* Go to Azure Active Directory -> Users -> New user.

* Enter account details (e.g., username: BreakGlassAdmin1).

* Set up strong, random passwords; record for secure storage.

* Click Create.

* Repeat for a second backup account.

**3. Assign Global Administrator Role.**

* From Azure AD, go to Roles and administrators.

* Select Global Administrator.

* Click Add assignments.

* Add your new break glass accounts as Active.

* Confirm assignments.

**4. Exclude from Conditional Access & MFA.**

* Go to Azure AD -> Security -> Conditional Access -> Policies.

* Edit each policy and add break glass accounts to the Excluded users list.

* Under Security -> Multi-Factor Authentication, verify MFA is not enforced for these accounts.

**5. Secure Account Credentials**

* On first login, update the password using the temporary password issued at creation.

* Record who has access and storage location.

**6. Monitor and Alert on Usage**

* Go to Azure AD > Sign-ins.

* Set up alerts so any sign-in with a break glass account notifies security/incident response teams.

**7. Regular Reviews and Credential Rotation**

* Quarterly (or after any use), reset passwords and review account exclusions and assignments.

* Log these actions in your documentation.

---

**Security Warning**

Due to their high privilege and bypass nature, break-glass accounts require strict controls and frequent review.
