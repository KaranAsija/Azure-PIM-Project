# 04. Configure Azure Resource Roles in PIM


## Objective

Extend PIM to manage Azure resource-level privileges (subscriptions, resource groups, resources) with JIT access controls.

---

## Steps

**Onboard Azure Resources**

* Go to PIM > Azure Resources.

* Add Subscriptions/Resource Groups for PIM management.

**Assign Resource Roles**

* Define which roles (Owner, Contributor, Reader) need privileged access in each resource.

* E.g., assign UserC as Eligible Owner of “ResourceGroupDemo.”

**Configure Activation and Approval**

* Duration (default: 2 hours).

* Approval required: Yes (assign approvers: e.g., Resource Owner).

* MFA enforced at activation.

* Justification required for tracking.

| User | Resource |	Role | Assignment Type |Approval	| Max Duration |
|------|----------|-------|-----------------|---------|--------------|
|UserC |	ResourceGroupDemo|Owner|Eligible|Yes|	2 hours|

---

**Use Case**

Provides DevOps or platform teams with temporary elevated access for deployments or resource management while maintaining strong security controls.
