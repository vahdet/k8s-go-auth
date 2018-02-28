# Kubernetes configurations for `go-user-store`, `go-refresh-token-store`, `go-auth-service` and `redis`

### DockerHub Images
The container images can be found on:
* https://hub.docker.com/r/vahdet/go-user-store/
* https://hub.docker.com/r/vahdet/go-refresh-token-store/
* https://hub.docker.com/r/vahdet/go-auth-service/

### on Kubernetes
The logic for a container environment (including linking containers) can be built on [Kubernetes](https://kubernetes.io/). 

#### Pulling images from Docker Hub
In documentation it says:

>You create your Docker image and push it to a registry before referring to it in a Kubernetes pod.
>
>The image property of a container supports the same syntax as the docker command does, including private registries and tags.

For further reading:
* [Kubernetes Images Doc](https://kubernetes.io/docs/concepts/containers/images/)

## Minikube
Minikube is a single-node version of Kubernetes especially handy for local development.

On a **Linux Machine** Minikube can be run with [no VMs](https://github.com/kubernetes/minikube#quickstart). To do that minikubes should be started with the `vm-driver` option set to `false`

```bash
sudo minikube start --vm-driver=none
```

### Multiple containers in the same `pod`
Having multiple containers in the same pod:
* makes it possible to communicate the containers of the same port only through their `port`s.
### Using `kubectl` command with the .yml configs

```bash
kubectl create -f path/to/yml
```

## Kubernetes Setup on AWS
[Kops](https://github.com/kubernetes/kops) is used for setup Kubernetes on AWS.

## See also
* [Expose Pod Information to Containers Through Environment Variables](https://kubernetes.io/docs/tasks/inject-data-application/environment-variable-expose-pod-information/)
* [Creating a Pod that runs two Containers](https://kubernetes.io/docs/tasks/access-application-cluster/communicate-containers-same-pod-shared-volume/#creating-a-pod-that-runs-two-containers)
* [Configuring Redis using a ConfigMap](https://kubernetes.io/docs/tutorials/configuration/configure-redis-using-configmap/)
* [Diego Pacheco's Beautiful 'Go and Redis running on Kubernetes with Minukube'](http://diego-pacheco.blogspot.com.tr/2017/08/go-and-redis-running-on-kubernetes-with.html)
* [In-Pod and Inter-Pods Communication](https://www.mirantis.com/blog/multi-container-pods-and-container-communication-in-kubernetes/)
* [Kubernetes Guestbook Example](https://github.com/kubernetes/kubernetes/tree/master/examples/guestbook)
