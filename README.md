# kubetest

Deployment tool for various versions of kubernetes environment

## Requirements

- [kind version v0.8.1](https://github.com/kubernetes-sigs/kind/releases/tag/v0.8.1)
- [yq version 3.2.1](https://github.com/mikefarah/yq/releases/tag/3.2.1)
- [kustomize version v3.5.4](https://github.com/kubernetes-sigs/kustomize/releases/tag/kustomize%2Fv3.5.4)

## How to use

```bash
kubetest deploy <kubernetes-version>
```

supported kubernetes version: (which depends on kind v0.8.0 release)
- v1.18.2
- v1.17
- v1.16
- v1.15
- v1.14
- v1.13
- v1.12
- v1.11

example:

```bash
$ kubetest deploy v1.16
Creating cluster "kubetest" ...
 ✓ Ensuring node image (kindest/node:v1.16.9) 🖼 
 ✓ Preparing nodes 📦 📦 📦  
 ✓ Writing configuration 📜 
 ✓ Starting control-plane 🕹️ 
 ✓ Installing CNI 🔌 
 ✓ Installing StorageClass 💾 
 ✓ Joining worker nodes 🚜 
Set kubectl context to "kind-kubetest"
You can now use your cluster with:

kubectl cluster-info --context kind-kubetest

Not sure what to do next? 😅  Check out https://kind.sigs.k8s.io/docs/user/quick-start/
```

## configure current context in kubectl

```
$ kubetest configure
Kubernetes master is running at https://127.0.0.1:54104
KubeDNS is running at https://127.0.0.1:54104/api/v1/namespaces/kube-system/services/kube-dns:dns/proxy

To further debug and diagnose cluster problems, use 'kubectl cluster-info dump'.
$
$ kubectl get node
NAME                     STATUS   ROLES    AGE     VERSION
kubetest-control-plane   Ready    master   6m      v1.16.9
kubetest-worker          Ready    <none>   5m23s   v1.16.9
kubetest-worker2         Ready    <none>   5m23s   v1.16.9
```

## delete cluster

```bash
$ kubetest delete
Deleting cluster "kubetest" ...
```

