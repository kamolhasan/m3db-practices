# m3db-practices

- Create etcd cluster (seed nodes) 
- Deploy m3db operator
- Deploy m3db cluster (storage nodes)
- Deploy m3aggregator 
- Deploy m3coordinator 
- Deploy m3query 
- Deploy prometheus exporter 
- Deploy prometheus

# Load testing
- setup gitea (add necessary flags to config)
- setup prometheus (using coreOS operator) 
- deploy etcd cluster
- deploy m3db operator
- deploy m3db cluster 
    - can't take more 3 namespaces at once
    - first give 3 namespaces configuration, once all db nodes are bootstrapped 
      update yaml for remaining namespaces
- Deploy m3aggregator
    - different statefulset with replication factor 1 is used sothat different nodeaffinity can be used. 
- Deploy m3coordinator 
- Deploy m3query 
- Update prometheus server with stack driver sidecar image 
- Deploy prometheus matrices exporter (https://github.com/searchlight/prometheus-metrics-exporter)
    - required (license)
- Deploy prometheus query handler (https://github.com/appscode-cloud/prom-query-handler/tree/master/artifacts/demo-querier)
    - required (username, password, license)