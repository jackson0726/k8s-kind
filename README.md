# k8s-kind

## [Installation](https://kind.sigs.k8s.io/docs/user/quick-start/)

```
curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.16.0/kind-linux-amd64
chmod +x ./kind
sudo mv ./kind /usr/local/bin/kind
```

## Creating a Cluster

```
kind create cluster

or

kind create cluster --image=...
```

## Deleting a Cluster

```
kind delete cluster --name=...
```

## Configuring Your kind Cluster

```
kind create cluster --config kind-example-config.yaml
```

## Multi-node clusters

```
# three node (two workers) cluster config
kind: Cluster
apiVersion: kind.x-k8s.io/v1alpha4
nodes:
- role: control-plane
- role: worker
- role: worker
```













