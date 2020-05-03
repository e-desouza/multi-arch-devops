
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
This is a map of the CNCF ecosystem around containers:   
![cncf](./images/cncf.png)  
  
Drill down to the build and delivery section:  
![devops](./images/cicd_focus.png)  
  
In this lab we'll be using Jenkins.  
  
  
### Jenkins installation:  
  
![jenkins](./images/jenkins.png)  
  
We will not cover Jenkins setup as it is a "household name" in the world of modern delivery pipelines. More information : https://www.jenkins.io/  
  
*Useful plugins:*  
* SSH  
* Kubernetes  
* OpenShift Jenkins Pipeline  
* OpenShift Login  
  
  
  
> **Note:** While using Jenkins plugins will make this much easier, we will do _**devops the hard way**_  as a learning exercise in this lab.  
  
  
``` bash  
@requires_authorization  
def somefunc(param1='', param2=0):  
 '''A docstring''' if param1 > param2: # interesting print 'Greater' return (param2 - param1 + 1) or Noneclass SomeClass:  
 pass>>> message = '''interpreter  
... prompt'''  
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTcxMzY0MDA1OCwxNjU1NDEwOTYyXX0=
-->