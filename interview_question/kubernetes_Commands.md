Pod Management
kubectl get pods --all-namespaces: List all pods across all namespaces.

kubectl describe pod <pod_name>: Get detailed information about a specific pod.

kubectl logs <pod_name> -c <container_name>: View logs of a specific container in a pod.

kubectl delete pod <pod_name> --grace-period=0 --force: Forcefully delete a pod.

kubectl exec -it <pod_name> -- /bin/sh: Open a shell inside a running container for debugging.

kubectl cp <pod_name>:/path/to/file /local/path: Copy files from a pod to your local machine.

kubectl get pods -o wide: List pods with additional details like node and IP.

kubectl get pods --field-selector=status.phase=Running: List only running pods.

Deployment and Rollout Management
kubectl rollout undo deployment <deployment_name>: Roll back a deployment to the previous version.

kubectl rollout status deployment <deployment_name>: Check the status of a deployment rollout.

kubectl rollout history deployment <deployment_name>: View the rollout history of a deployment.

kubectl scale deployment <deployment_name> --replicas=<number>: Scale a deployment up or down.

kubectl set image deployment/<deployment_name> <container_name>=<new_image>: Update the image of a container in a deployment.

Node Management
kubectl get nodes: List all nodes in the cluster.

kubectl describe node <node_name>: Get detailed information about a specific node.

kubectl drain <node_name> --ignore-daemonsets: Safely drain a node for maintenance.

kubectl cordon <node_name>: Mark a node as unschedulable.

kubectl uncordon <node_name>: Mark a node as schedulable again.

kubectl taint nodes <node_name> <key>=<value>:NoSchedule : Add a taint to a node to prevent scheduling.

kubectl top nodes: Monitor resource usage (CPU/memory) of nodes.

Service and Endpoint Management
kubectl get services: List all services in the current namespace.

kubectl get endpoints <service_name>: List endpoints for a specific service.

kubectl expose deployment <deployment_name> --type=LoadBalancer --port=<port>: Expose a deployment as a service.

kubectl get ingress: List all ingress resources.

Cluster and Component Health
kubectl get componentstatuses: Check the health of core cluster components (e.g., etcd, kube-apiserver).

kubectl get events --all-namespaces --sort-by=.metadata.creationTimestamp: View cluster events sorted by creation time.

kubectl cluster-info: Display cluster information and health.

kubectl get csr: List Certificate Signing Requests (useful for debugging node registration).

Resource Monitoring
kubectl top pods --all-namespaces: Monitor resource usage of pods across all namespaces.

kubectl top nodes: Monitor resource usage of nodes.

kubectl get hpa: List Horizontal Pod Autoscalers (HPA) and their status.

Configuration and Debugging
kubectl apply -f <file.yaml>: Apply a configuration from a YAML file.

kubectl delete -f <file.yaml>: Delete resources defined in a YAML file.

kubectl edit deployment <deployment_name>: Edit a deployment in place.

kubectl config view: View the current Kubernetes configuration.

kubectl config use-context <context_name>: Switch to a different Kubernetes context.

kubectl auth can-i <verb> <resource>: Check if you have permission to perform an action.

Namespace Management
kubectl get namespaces: List all namespaces.

kubectl create namespace <namespace_name>: Create a new namespace.

kubectl delete namespace <namespace_name>: Delete a namespace.

kubectl config set-context --current --namespace=<namespace_name>: Switch to a specific namespace.

ETCD and Backup Management
etcdctl --endpoints=https://<etcd-server>:2379 snapshot save backup.db: Take a snapshot of the etcd database.

etcdctl --endpoints=https://<etcd-server>:2379 snapshot restore backup.db: Restore etcd from a snapshot.

kubectl get secrets: List all secrets in the current namespace.

Miscellaneous
kubectl get pv: List Persistent Volumes (PV).

kubectl get pvc: List Persistent Volume Claims (PVC).

kubectl get storageclass: List storage classes.

kubectl get jobs: List all jobs.

kubectl get cronjobs: List all cron jobs.

kubectl get configmaps: List all ConfigMaps in the current namespace.