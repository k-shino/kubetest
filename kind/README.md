# kubetest

Various kubernetes version deployment tool on kind

## Requirements

- kind version v0.8.1
- yq version 3.2.1
- kustomize version v3.5.4

## How to build

```bash
kubetest <kubernetes-version>
```

example:

```bash
$ ./kubetest v1.18.2/
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

