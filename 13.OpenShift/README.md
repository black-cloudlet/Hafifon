# Openshift

### Intro
- What is the difference between OpenShift and Kubernetes

### Openshift Resources
- Route
    - Why are Routes useful?
    - How does a Route work?
    - What are the different types of TLS Terminations that can be used by Routes?
    - How does a request to a route's URL reaches the Service?
    - How do Routes work in our tactic environment (Helper)?
- CSR
    - What are CSR's used for?
    - How are CSR's renewed?
    - What can cause an expiriration of cluster certificates? (Often happens in our cloudlets)

### Operators
- What is the difference between an operator and a controller?
- What are the responsibilities of the following Cluster Operators?
    - authentication
    - console
    - etcd
    - ingress
    - openshift-apiserver
    - machine-config
    - network
    - dns
    - image registry
    - openshift-monitoring

### Openshift types 
- Read about virtualized openshift
- Read about bare-metal openshift
- Read about hybrid(virualized+bare-metal) openshift

### Openshift Installation
- Read about ignition files for OpenShift and the Bootstrap process of a cluster
- What is the different between UPI and IPI installations (User/Installer provisioned installation)?
- What is a Kubernets CSI? Why is it important to setup right after the installation of a cluster?

### Openshift Authentication 
- How do authentication and authorization work in OpenShift?

### Openshift Permissions
- Read about openshift SCC

### Openshift Monitoring
- What is a ServiceMonitor CustomResourceDefinition (CRD) and what is its primary role?
- How does a ServiceMonitor use labels and selectors to dynamically discover targets (Services) for scraping metrics?
- What are the required fields to configure a basic ServiceMonitor (e.g., endpoints, ports, selector)?
- What is PrometheusRule? how to use it?
