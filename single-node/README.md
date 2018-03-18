# Single Node
The files here are designed for single node use like *Minikube* on a local machine.

To achieve that, `replicas` value in *Deployments* are set to 1.

# Commands

    # Start minikube
    sudo start minikube
    
    # Start user store
    sudo kubectl create -f /home/vahdet/work/kubernetes/src/github.com/vahdet/k8s-go-auth/single-node/middleware/go-user-store-redis.yml

