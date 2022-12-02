### Introduction

This is a simple three tier application that can be deployed on OpenShift via OpenShift GitOps.

![alt text](https://raw.githubusercontent.com/gnunn-gitops/product-catalog/master/docs/img/topology.png)

### Demonstration

To use this application in your own demos, simply fork this repo and then create an app in OpenShift GitOps to point to this application.

![alt text](https://raw.githubusercontent.com/gitops-example/simple-app-example/master/docs/img/argo-create-app-top.png)

![alt text](https://raw.githubusercontent.com/gitops-example/simple-app-example/master/docs/img/argo-create-app-bottom.png)

Note the Path is set to just a dot, i.e. `.`, ignore the cursor there it is not a pipe.

Once the application is deployed, you can demo some basic GitOps principles:

1. Self-Healing. Try to increase the replica count of the client or the server in the OpenShift Console, note that because self-heal is enabled it is automatically reset back to 1 which is what is set in the repo.

2. Self-Healing. Delete the client application in the OpenShift Console, note that Argo immediately recreates it

3. In git increase the replica count for either the client or server application in kustomization.yaml

4.
