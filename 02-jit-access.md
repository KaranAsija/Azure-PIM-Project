# 02. Just-In-Time (JIT) Privileged Access


## Concept

**Just-In-Time (JIT)** access grants users privileged access only when needed, for a limited duration, not continuously.
* JIT reduces the risk of permanent admin access.

* Users can activate their eligible role when a privileged action is necessary.

* After the time frame expires, the elevated permissions are revoked.

---

## Implementation Steps

1. Go to **Azure AD PIM ➔ Azure AD roles**
2. Select a role (e.g., Global Administrator)
3. Click **Role settings ➔ Edit**
4. Configure:
   - **Activation maximum duration** (e.g., 1 hour)
   - **Require approval to activate:** Enabled
   - **Specify approvers:** e.g., IAM team leads
   - **Require MFA:** Enabled
   - **Notification settings:** Notify relevant admins upon activation
5. Click **Save**

---

## Theoretical Example:
UserA has "eligible" access to the Global Administrator role. When they need admin privileges, they request activation through PIM, provide justification, and receive access for 1 hour.

## Why it’s Important?

JIT access minimizes the attack surface and limits potential lateral movement for attackers by removing unnecessary permanent privileges.
