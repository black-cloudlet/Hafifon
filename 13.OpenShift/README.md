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

### Openshift Node OS (CoreOS)
- What is OSTree? What is `rpm-ostree`? Why is the root filesystem read-only?
- What is CoreOS (Red Hat Enterprise Linux CoreOS, RHCOS)? How is it different from a regular RHEL?
- How do OS updates work on CoreOS? (Read about atomic updates and rollback)
- What is a MachineConfig? What is a MachineConfigPool?
- What happens to a node when you apply a MachineConfig? (Read about the Machine Config Operator, rendered configs and node reboots)
- Why is it not recommended to change files directly on an OpenShift node?
- What is `bootc`? How is it related to OSTree?
- What is the idea behind "image mode" (booting an OS from a container image)? What are the advantages?

### Openshift Air-Gapped (Disconnected) 
- What is an air-gapped (disconnected) environment? Why is it common in secret enviroment?
- What is a bastion host? Why is it commonly used in air-gapped environments?
- What does a cluster normally pull from the internet during installation and during its lifetime? (Think about images, operators and updates)
- What is a mirror registry? What is the difference between a mirror registry and a regular registry?
- What is `oc-mirror`? What does the `ImageSetConfiguration` file define?
- How can you transfer the mirrored content to a network that has no connection at all? (Read about the mirror-to-disk and disk-to-mirror flow)
- How do you tell the cluster to pull images from the mirror instead of the original registries? (Read about `ImageDigestMirrorSet` and `ImageTagMirrorSet`)
- How do you make the cluster trust the internal certificate of network?
- What is OperatorHub in a disconnected cluster? What are CatalogSources and why do we need to create custom ones?
- What is the OpenShift Update Service (OSUS)? How do you update a disconnected cluster?
- What does the `pull-secret` contain? Why does it need to include credentials for the mirror registry?

### Openshift Authentication 
- How do authentication and authorization work in OpenShift?

### Openshift Permissions
- Read about openshift SCC

### Openshift Monitoring
- Prometheus
    - What is Prometheus? What problem does it solve?
    - What is the difference between the pull model (Prometheus) and the push model?
    - What is a metric? What are labels and why are they important?
    - What are the 4 metric types? (Counter, Gauge, Histogram, Summary)
    - What is PromQL? What does the `rate()` function do and why is it used with counters?
    - What is Alertmanager?
- Exporters
    - What is an exporter? Why do we need it?
    - What does `node_exporter` expose? 
    - What about `kube-state-metrics`?
    - What is `blackbox-exporter`?
    - What is the `/metrics` endpoint? What format does it return?
- Grafana
    - What is Grafana? How is it related to Prometheus?
    - What is a data source? What is a dashboard?
    - Where can you see dashboards in the OpenShift console?
- Monitoring in OpenShift
    - What is a ServiceMonitor CustomResourceDefinition (CRD) and what is its primary role?
    - How does a ServiceMonitor use labels and selectors to dynamically discover targets (Services) for scraping metrics?
    - What are the required fields to configure a basic ServiceMonitor (e.g., endpoints, ports, selector)?
    - What is PrometheusRule? how to use it?

### Openshift Virtualization
- What is KubeVirt? What problem does it solve?
- What is OpenShift Virtualization and how is it related to KubeVirt?
- How can a VM run inside a Kubernetes pod? (Read about `virt-launcher`, libvirt and QEMU/KVM)
- What are the main KubeVirt components? (`virt-api`, `virt-controller`, `virt-handler`, `virt-launcher`)
- What is a `VirtualMachine` object? What is the difference between a `VirtualMachine` and a `VirtualMachineInstance`?
- How are VM disks stored? (Read about PVCs and CDI, the Containerized Data Importer)
- How is VM networking done? What is the difference between the pod network and Multus secondary networks?
- What is live migration? What does the cluster need in order to support it?
- What are the pros and cons of running VMs on OpenShift compared to a regular hypervisor (e.g. vSphere)?
