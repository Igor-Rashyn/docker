kind: Pod - runs one or more closely related containers.
kind: Services - Sets up networking in a Kubernetes Cluster. provides several sub-types (NodePort, ClusterIP, LoadBalancer, Ingress)
  type: NodePort - exposes a container to outside world (only good for dev purposes!!!)
kind: Deployment - runs a set of identical pods. Monitors the state of each pod, updating as necessary.

  minikube ip - return ip address of running
  kubectl get services/pods -  return a list of created pods/services
  kubectl apply -f client-node-port.yaml  - create pods/services/etc
  kubectl describe <container type> <container name>  - get information about container
  kubectl delete -f <config file> - delete running container