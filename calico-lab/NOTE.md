# calico-security-controls-for-k8s

## Network policies
Calico network policies extend k8s network policies with 
additional capabilities like global scope, policy ordering controls, 
rule actions (i.e. Allow, Deny, Log, Pass), DNS policies, policy tiers, policy preview and staging, 
and other fine-grained policy controls.   

Deploy the Kubernetes policy to allow `centos` access `nginx` within `dev` namespace.

```yaml
# deploy policy
kubectl apply -f calico-policy/k8s.centos-to-nginx.yaml
```
## 