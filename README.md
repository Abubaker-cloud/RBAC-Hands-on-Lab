# Kubernetes RBAC Hands-On Lab

## Overview
A hands-on Kubernetes lab exploring Role-Based Access Control (RBAC).

## Lab Objectives
- Create and manage a Kubernetes Role.
- Connect a Role to a ServiceAccount using RoleBinding.
- Control access to Pods.
- Test authorization using `kubectl auth can-i`.

## Resources
- `view-pods-role.yaml` – Defines permissions on Pods.
- `view-pods-rolebinding.yaml` – Connects the Role to a ServiceAccount.
- `pod.yaml` – Pod manifest used during the lab.

## RBAC Concepts

### Role
Defines permissions within a specific namespace.

### RoleBinding
Assigns permissions defined in a Role to a User, Group, or ServiceAccount.

### ServiceAccount
Provides an identity for processes running inside Kubernetes.

## Testing

```bash
kubectl auth can-i get pods -n rbac-lab --as=system:serviceaccount:rbac-lab:dev-user
kubectl auth can-i create pods -n rbac-lab --as=system:serviceaccount:rbac-lab:dev-user
kubectl auth can-i delete pods -n rbac-lab --as=system:serviceaccount:rbac-lab:dev-user
