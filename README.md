# Kubernetes configurations for `go-user-store` and `redis`

### go-user-store on DockerHub
The container image can be found on:
* https://hub.docker.com/r/vahdet/go-user-store/

### on Kubernetes
The logic for a container environment (including linking containers) can be built on [Kubernetes](https://kubernetes.io/). 

#### Pulling images from Docker Hub
In documentation it says:

>You create your Docker image and push it to a registry before referring to it in a Kubernetes pod.
>
>The image property of a container supports the same syntax as the docker command does, including private registries and tags.

For further reading:
* [Kubernetes Images Doc](https://kubernetes.io/docs/concepts/containers/images/)

## See also
* [Expose Pod Information to Containers Through Environment Variables](https://kubernetes.io/docs/tasks/inject-data-application/environment-variable-expose-pod-information/)
* [Creating a Pod that runs two Containers](https://kubernetes.io/docs/tasks/access-application-cluster/communicate-containers-same-pod-shared-volume/#creating-a-pod-that-runs-two-containers)
* [Configuring Redis using a ConfigMap](https://kubernetes.io/docs/tutorials/configuration/configure-redis-using-configmap/)
* [Diego Pacheco's Beautiful 'Go and Redis running on Kubernetes with Minukube'](http://diego-pacheco.blogspot.com.tr/2017/08/go-and-redis-running-on-kubernetes-with.html)
