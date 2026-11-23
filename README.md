## Testing

Check whether the ServiceAccount can read Pods:

```bash
kubectl auth can-i get pods -n rbac-lab --as=system:serviceaccount:rbac-lab:dev-user
```

Check whether it can create Pods:

```bash
kubectl auth can-i create pods -n rbac-lab --as=system:serviceaccount:rbac-lab:dev-user
```

Check whether it can delete Pods:

```bash
kubectl auth can-i delete pods -n rbac-lab --as=system:serviceaccount:rbac-lab:dev-user
```
