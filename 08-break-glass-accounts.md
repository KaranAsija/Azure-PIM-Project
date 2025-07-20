# 08. Create and Manage Break-Glass Accounts

## Concept

**Break-glass accounts** are emergency Global Administrator accounts used when PIM, MFA, or Conditional Access policies lock out admins.

---


## Steps

1. **Create Account:** Cloud-only account (e.g., breakglass-admin@domain.onmicrosoft.com)  
2. Assign **Global Administrator** permanently  
3. **Exclude from Conditional Access policies** enforcing MFA temporarily  
4. **Secure credentials:**
   - Store in password vaults (e.g., Azure Key Vault, CyberArk)
5. **Monitor:**
   - Setup alerts for all sign-ins
   - Review quarterly for compliance

---

**Security Warning**

Due to their high privilege and bypass nature, break-glass accounts require strict controls and frequent review.
