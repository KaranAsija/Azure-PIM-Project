# 04. Configure Azure Resource Roles in PIM


## Objective

Extend PIM to manage Azure resource-level privileges (subscriptions, resource groups, resources) with JIT access controls.

---

## Theoretical Steps

1. Go to **Azure AD PIM ➔ Azure resources**  
2. Select the desired **subscription/resource group/resource**  
3. Click **Manage resource roles**  
4. Choose a role (e.g., Owner, Contributor)  
5. Click **Add assignment ➔ Select member ➔ Eligible**  
6. Configure:
   - Activation duration
   - Approval workflow
   - MFA enforcement
7. Save configurations

---

🔎 **Use Case**

Provides DevOps or platform teams with temporary elevated access for deployments or resource management while maintaining strong security controls.
