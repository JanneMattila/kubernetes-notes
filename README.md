# Kubernetes notes

Collection of my different Kubernetes notes mostly in context of 
[Azure Kubernetes Service (AKS)](https://docs.microsoft.com/en-us/azure/aks/) or
[Azure Arc-enabled Kubernetes](https://docs.microsoft.com/en-us/azure/azure-arc/kubernetes/overview)
but also some that are also relevant for vanilla [Kubernetes](https://kubernetes.io/docs/home/).

## Super important topics to understand

- Understand the Kubernetes [relase cycle](https://github.com/kubernetes/community/blob/master/contributors/devel/sig-release/release.md#the-release-cycle)
  - ~3 releases per year
  - 3 minor versions supported at a time
  - [Support window is one year](https://kubernetes.io/blog/2020/08/31/kubernetes-1-19-feature-one-year-support/)
- Understand [AKS Kubernetes Release Calendar](https://docs.microsoft.com/en-us/azure/aks/supported-kubernetes-versions?tabs=azure-cli#aks-kubernetes-release-calendar)

All of the above just means that:

> There is no such thing as Kubernetes Long-term support (LTS)

and

> You need to plan your cluster upgrades due to frequent releases

and be careful because many things might break because of [Kubernetes API deprecations](https://kubernetes.io/docs/reference/using-api/deprecation-guide/).

## Playgrounds

Different playgrounds have been created for testing very specific scenario.
They also contain simple deployment script either written in
`bash` or `PowerShell` which you can run [line by line](https://github.com/JanneMattila/some-questions-and-some-answers/blob/master/q%26a/vs_code.md#automation-tip-shift-enter)
and replicate that environment for your own testing purposes.

### Storage

[Playground AKS Storage](https://github.com/JanneMattila/playground-aks-storage)

### Monitoring

[Playground AKS monitoring](https://github.com/JanneMattila/playground-aks-monitoring)

### Identity

[Playground AKS Identity](https://github.com/JanneMattila/playground-aks-identity)

[Cluster with Azure AD Auth](https://github.com/JanneMattila/k8s-cluster)

### Maintenance

[Playground AKS Maintenance](https://github.com/JanneMattila/playground-aks-maintenance)

[Playground AKS Scaling](https://github.com/JanneMattila/playground-aks-scaling)

### Windows

[Playground AKS Windows](https://github.com/JanneMattila/playground-aks-windows)

### Networking

[Playground AKS Networking](https://github.com/JanneMattila/playground-aks-networking)

[Playground Private AKS](https://github.com/JanneMattila/playground-private-aks)

[Playground for AKS and AGIC (Application Gateway Ingress Controller)](https://github.com/JanneMattila/playground-aks-agic)

### Development

[Kubernetes Probe Demo](https://github.com/JanneMattila/KubernetesProbeDemo)

[Playground AKS GitOps](https://github.com/JanneMattila/playground-aks-gitops)

### Multi-tenancy

[Playground-k8s-multi-tenancy](https://github.com/JanneMattila/playground-k8s-multi-tenancy)

Repository contains discussion topics around multi-tenancy options.

### Azure Arc

[Azure Arc-enabled Kubernetes](https://github.com/JanneMattila/azure-arc-demos/tree/main/k8s)

[Azure Application Services](https://github.com/JanneMattila/azure-application-services-demo)

### Misc

[kubernetes webhook controller in C#](https://github.com/JanneMattila/k8s-webhook-controller)
