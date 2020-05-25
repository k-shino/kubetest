# kubetest

Deployment tool for various kubernetes version environment

## Requirements

- [kind version v0.8.1](https://github.com/kubernetes-sigs/kind/releases/tag/v0.8.1)
- [yq version 3.2.1](https://github.com/mikefarah/yq/releases/tag/3.2.1)
- [kustomize version v3.5.4](https://github.com/kubernetes-sigs/kustomize/releases/tag/kustomize%2Fv3.5.4)

## How to use

```bash
kubetest <kubernetes-version>
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
$ ./kubetest v1.18.2
Creating cluster "kind" ...
 ✓ Ensuring node image (kindest/node:v1.18.2) 🖼
 ✓ Preparing nodes 📦 📦 📦
 ✓ Writing configuration 📜
 ✓ Starting control-plane 🕹️
 ✓ Installing CNI 🔌
 ✓ Installing StorageClass 💾
 ✓ Joining worker nodes 🚜
Set kubectl context to "kind-kind"
You can now use your cluster with:

kubectl cluster-info --context kind-kind

Thanks for using kind! 😊
```

## get clusters

```bash
$ kind get clusters
test
```

## delete cluster

```bash
$ kind delete cluster
Deleting cluster "kind" ...
```

