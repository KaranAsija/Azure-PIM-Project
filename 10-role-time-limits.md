# 10. Set Time Limit of Roles



## Objective
 
Implementing time-bound access for privileged roles in Azure PIM is fundamental for reducing security risks associated with prolonged or permanent administrative rights. The "time limit" restricts how long a user can hold an active privileged role per activation, ensuring just-in-time, least-privilege access.

A time limit (activation duration) is the maximum period for which a user can be “active” in a privileged role after requesting activation through PIM. When this duration expires, access is automatically revoked, and the user returns to “eligible” status.

---

## Steps

**1. Sign In and Open Azure Portal**

* Go to https://portal.azure.com

* Sign in with a Global Administrator or a role with PIM management permissions.

**2. Access Azure Active Directory PIM**

* In the left menu, select Azure Active Directory.

* Under Manage, click Privileged Identity Management.

**3. Choose the Scope**

* You can set time limits on:

  * Azure AD roles (e.g., Global Administrator)

  * Azure Resource roles (e.g., Owner, Contributor of subscriptions/resource groups)
  
  * Privileged Access Groups

* For Azure AD roles:

  * Select Azure AD roles.

  * Click Roles or Settings.

**4. Select a Role and Open Settings**

* Find and select the role to update (e.g., Global Administrator).

* Select Settings or Role settings.

**5. Configure Maximum Activation Duration**

* In the settings panel, locate the Activation maximum duration field.

* Set the desired length (typically in hours, e.g., 1 hour, 2 hours).

  * This is the longest period a user can be “active” per activation request.

* Optionally, set a default duration (how long requests default to if the user does not specify).

**6. Save and Apply**

* Review other settings (e.g., MFA, justification, approval) as needed.

* Click Save to confirm changes.



---

**Best Practice**

Limit activations to the minimum time necessary to complete administrative tasks.
