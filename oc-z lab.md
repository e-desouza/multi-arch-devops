## Multi-architecture devOps using OpenShift

In this lab you will learn how to deploy a Jenkins pipeline to build your source code from github and deploy it to both OpenShift on Intel and OpenShift on IBM Z/LinuxONE.

### Environment:
* RedHat OpenShift (ROKS) on IBM Cloud
* RedHat OpenShift on IBM LinuxONE (in IBM Washington System Center)
* Jenkins (in IBM Washington System Center)
* IBM Container Registry on IBM Cloud

### Topology diagram:

![topology](./images/topology-lab.png)

### What is multi-architecture deployment anyway?

A multi-architecture deployment is a deployment that lets you deploy the same image (e.g hello-world:latest) on any platform using the same deployment artifacts (pod definitions, deployments, services, routes etc). This greatly simplifies the deployment process while letting an organization optimize for certain metrics:
* Cost
* Throughput
* Latency
* Security and Compliance
* Scalability
* Resiliency and reliability
* Uptime

Platform includes:
* Operating System (windows, linux etc)
* Instruction Architecture (amd64, s390x, ppcle64, arm64 etc)

### Multi-architecture Manifests

![multi-arch](./images/manifest.png)

To enable multi-architecture, docker added support for manifests which let you link which platform to image (but exposing the end result as the same image). e.g "docker run hello-world" will first look at the version (`latest` is implied if no version tag is specified) then will check the local operating system and architecture (e.g linux, s390x) and query that combination in the registry. Once it fins that combination, it'll pull _only that specific container_ locally. Multi-arch images are similar to "fat binaries" at the container registry level but single, os and architecture specific images at the docker daemon level.

By default the Docker daemon will look at its current operating system and architecture but it is possible to force download of a specific platform/architecture using the `--platform` command which is available in docker API [1.32+](https://docs.docker.com/engine/api/v1.32/) amd meed `experimental features` turned on in Docker daemon. More information can be found in the official docs [here](https://docs.docker.com/engine/reference/commandline/pull/).

### Building multi-arch images:

[buildx](https://mirailabs.io/blog/multiarch-docker-with-buildx/)

### Container Registries

### DevOps tools:
This is a map of the CNCF ecosystem around containers: 
![cncf](./images/cncf.png)

Drill down to the build and delivery section:
![devops](./images/cicd_focus.png)

In this lab we'll be using Jenkins.

### Jenkins installation:

![jenkins](./images/jenkins.png)

We will not cover Jenkins setup as it is a "household name" in the world of modern delivery pipelines. More information can be found at Jenkins [official](https://www.jenkins.io/)

*Useful plugins to install:*
* SSH
* Kubernetes
* OpenShift Jenkins Pipeline
* OpenShift Login

### IBM Multicloud Manager

> **Note:** While using Jenkins plugins will make this much easier, we will do _**devops the hard way**_  as a learning exercise in this lab.


``` bash
@requires_authorization
def somefunc(param1='', param2=0):
    '''A docstring'''
    if param1 > param2: # interesting
        print 'Greater'
    return (param2 - param1 + 1) or None
class SomeClass:
    pass
>>> message = '''interpreter
... prompt'''
```