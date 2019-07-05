kind: Pod - runs one or more closely related containers.
kind: Services - Sets up networking in a Kubernetes Cluster. provides several sub-types (NodePort, ClusterIP, LoadBalancer, Ingress)
  type: NodePort - exposes a container to outside world (only good for dev purposes!!!)
kind: Deployment - runs a set of identical pods. Monitors the state of each pod, updating as necessary.

  minikube ip - return ip address of running
  kubectl get services/pods -  return a list of created pods/services
  kubectl apply -f client-node-port.yaml  - create pods/services/etc
  kubectl describe <container type> <container name>  - get information about container
  kubectl delete -f <config file> - delete running container

  kubectl set image <object_type>/<object_name> <Container_name>=<new image to use> - перезапустит контейнер з переопределенным свойством (свойство: image) и указываем что мы хотим
  kubectl set image deployment/client-deployment client=nishik/multi-client:v2
  kubectl delete deployment <deployment_name> - удалить
  kubectl create secret generic <secret_name> --from--literal key=value - создать секрет для хранения паролей, ssh и тд

  eval $(minikube docker-env)  --   команда перенастроит shell смотреть на VM на которой стоит кубернет