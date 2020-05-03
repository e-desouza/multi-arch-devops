## Multi-architecture devOps using OpenShift

In this lab you will learn how to deploy a Jenkins pipeline to build your souce code from github and deploy it to both OpenShift on Intel and OpenShift on IBM Z/LinuxONE.

### Environment:
* RedHat OpenShift (ROKS) on IBM Cloud
* RedHat OpenShift on IBM LinuxONE (in IBM Washington System Center)
* Jenkins (in IBM Washington System Center)
* IBM Container Registry on IBM Cloud

### Topology diagram:



### What is multi-architecture deployment anyway?

### Multi-architecture Manifests

### Container Registries support multi-arch manifests

### DevOps tools:


### Jenkins installation:

We will not cover Jenkins setup as it is a "household name" in the world of modern delivery pipelines. More information : https://www.jenkins.io/

*Useful plugins:*
SSH
Kubernetes
OpenShift Jenkins Pipeline
OpenShift Login

While using Jenkins plugins will make this much easier, we will do "devops the hard way"  as a learning excercise.

```flow  
st=>start: Start  
e=>end  
op=>operation: My Operation  
cond=>condition: Yes or No?  
  
st->op->cond  
cond(yes)->e  
cond(no)->op  
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbOTM3MzExMjQzLDE2NTU0MTA5NjJdfQ==
-->