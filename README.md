# Nodecellar Kubernetes Blueprint

### Description
Nodecellar Kubernetes Blueprint creates a K8S deployment with 2 nodes:
* Nodecellar
* MongoDB
They are combined into a K8S service.

### Inputs
* kubernetes_configuration_file_content : Configuration of the kubernetes master. It can be retrieved using command:
```
kubectl config view --raw
```
* external_ip : IP for the end user/Floating IP. Should be one of the Kubernetes VM interfaces
* external_port: port for the end-user access. Default is 8080

### Installation
```
cfy install blueprint.yaml -i external_ip=10.20.30.40
```