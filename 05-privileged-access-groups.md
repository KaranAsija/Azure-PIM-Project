# 05. Configure Privileged Access Groups


## Concept

**Privileged Access Groups** enable JIT access to Azure AD groups that grant broad permissions (e.g., “Server Admins” group) rather than direct role assignments.

---

## Steps

1. **Navigate:** Azure AD ➔ Groups ➔ New Group ➔ Security  
2. Name the group (e.g., PIM-SQL-Admins) and assign owners.
3. Under **Privileged Access (Preview)**:
   - Enable **Activate membership**.
   - Enable **Activate Azure AD roles** if applicable.
4. Save settings.
5. Assign members as **Eligible** or **Active**.
6. Configure group PIM settings for activation duration, approvals, and notifications.

---

**Best Practice**

Use for managing large admin groups to simplify workflows and reduce direct individual role assignments.
