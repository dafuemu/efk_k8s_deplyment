Create the resources on k8s
```
kubectl create -f .
```

Create a headless Kubernetes service called èlasticsearch` that will define a DNS domain for the 3 Pods. A headless service does not perform load balancing or have a static IP; to learn more about headless services, consult the official Kubernetes documentation.
We set clusterIP: None, which renders the service headless. Finally, we define ports 9200 and 9300 which are used to interact with the REST API, and for inter-node communication, respectively.


A Kubernetes StatefulSet allows you to assign a stable identity to Pods and grant them stable, persistent storage. Elasticsearch requires stable storage to persist data across Pod rescheduling and restarts. To learn more about the StatefulSet workload, consult the Statefulsets page from the Kubernetes docs.
