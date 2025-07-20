# 01. Overview and Setup Prerequisites for Roles and Licenses


## Overview

***Privileged Identity Management (PIM)*** is an Azure AD feature that enables organizations to manage, monitor, and control access to critical resources by granting just-in-time privileged access. PIM helps minimize risks associated with excessive, unnecessary, or misused access permissions.

### Key Benefits

- Just-In-Time (JIT) role activation
- Approval workflows for role elevation
- Time-bound privileged access
- Audit logs for compliance

---

##    Prerequisites

**Licenses Required:**  
* Azure AD Premium P2 is required for full PIM functionality. 
* Ensure all users needing PIM capability (admins, approvers, auditors) have this license.  

**Permissions:** 
* At least one Global Administrator to configure and onboard PIM.
* Identify key roles requiring oversight:
  * Global Administrator (full privileges)
  * Security Administrator (security controls)
  * Application Administrator, User Administrator, etc.
  
**Roles:** 
* Users must be assigned as eligible to utilize PIM features

### Setup Steps

1. **Navigate:** Azure Portal ➔ Azure Active Directory ➔ Privileged Identity Management  
2. **Onboard PIM:** Click **Consent to PIM** if using for the first time  
3. **Verify License:** Azure AD ➔ Licenses ➔ All products ➔ Ensure Azure AD Premium P2 is available  
4. **Assign Permissions:** Confirm your account has necessary administrative roles

---

**Note:** In this theoretical project, configurations are documented without practical implementation due to licensing constraints.
