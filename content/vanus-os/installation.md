# Installation

The document will teach you how to install Vanus in a Kubernetes environment.

## Prerequisites
:::tip
If you want to run Vanus locally, we suggest that you use [minikube](https://minikube.sigs.k8s.io/docs/start).
We also provide an [interactive Kubernetes environment](https://play.linkall.com) to simply deploy and try Vanus in your browser.
:::

Before installing Vanus, you must meet the following prerequisites:

1. Have a [Kubernetes](https://kubernetes.io/docs/setup) cluster.
2. Have installed the [kubectl](https://kubernetes.io/docs/tasks/tools/).

## Install Vanus

Install Vanus by running the command:

```bash
kubectl apply -f https://dl.vanus.ai/all-in-one/v0.6.0.yml
```

After using kubectl apply, vanus namespace is created

```bash
kubectl get ns
```

```bash
NAME 			STATUS		AGE
default			Active		6m35s
kube-node-lease	         Active		6m36s
kube-public		Active		6m36s
kube-system		Active		6m36s
vanus			Active		46s

```
### Switch Default Namespace to Vanus
To switch default namespace to vanus use:

```bash
kubectl config set-context --current --namespace=vanus
```

Now, you can easily see the pods in the namespace

```shell
kubectl get pods
```

The output:

```text
NAME                             READY   STATUS    RESTARTS    AGE
vanus-controller-0               1/1     Running   0           8s
vanus-controller-1               1/1     Running   0           9s
vanus-controller-2               1/1     Running   0           10s
vanus-gateway-7889df65c9-hvm97   1/1     Running   0           3s
vanus-store-0                    1/1     Running   0           10s
vanus-store-1                    1/1     Running   0           11s
vanus-store-2                    1/1     Running   0           12s
vanus-timer-88bc6885-fst27       1/1     Running   0           10s
vanus-trigger-8668cd4659-l9lgp   1/1     Running   0           10s
```

You can also access the pods without changing the default namespace. To do this, use:

```shell
kubectl get pods -n vanus
```

This can be done after installing Vanus with:

```bash
kubectl apply -f https://dl.vanus.ai/all-in-one/v0.6.0.yml
```