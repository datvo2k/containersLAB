# Calico Lab

## Overview
This lab provides a hands-on environment for learning and experimenting with Calico networking in Kubernetes environments. Calico is an open-source networking and security solution for containers, virtual machines, and native host-based workloads.

## Prerequisites
- Kubernetes cluster (minikube, kind, or a cloud-managed cluster)
- `kubectl` CLI tool installed
- Basic understanding of Kubernetes networking concepts

## Lab Components
1. Calico installation and configuration
2. Network policy implementation
3. Securing pod-to-pod communication
4. Advanced network policies
5. Monitoring and troubleshooting

## Getting Started
1. Install Calico on your Kubernetes cluster:
   ```bash
   kubectl create -f https://docs.projectcalico.org/manifests/tigera-operator.yaml
   kubectl create -f https://docs.projectcalico.org/manifests/custom-resources.yaml
   ```

2. Verify Calico installation:
   ```bash
   kubectl get pods -n calico-system
   ```

## Exercises
- Create basic network policies to restrict pod communication
- Implement label-based network policies
- Configure egress policies
- Test isolation between namespaces

## Troubleshooting
- Use `calicoctl` to inspect Calico configuration
- Check Pod statuses and logs for connectivity issues
- Verify network policy implementation with test workloads

## Resources
- [Calico Documentation](https://docs.projectcalico.org/)
- [Kubernetes Network Policies](https://kubernetes.io/docs/concepts/services-networking/network-policies/)
- [Calico GitHub Repository](https://github.com/projectcalico/calico)