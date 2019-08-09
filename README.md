---
page_type: sample
languages: java
products: azure
services: Containerinstance
platforms: java
author: yaohaizh
---

## Getting Started with Containerinstance - Manage Container Instance Zero To One And One To Many Using Container Service Orchestrator - in Java ##


  Azure Container Instance sample for managing container instances.
      - Create an Azure Container Registry to be used for holding private Docker container images
      - If a local Docker engine cannot be found, create a Linux virtual machine that will host a Docker engine
          to be used for this sample
      - Use Docker Java to create a Docker client that will push/pull an image to/from Azure Container Registry
      - Pull a test image from the public Docker repo (tomcat:8) to be used as a sample for pushing/pulling
          to/from an Azure Container Registry
     - Create an Azure container group with a container instance using the container image that was pushed to the
          container registry created above
     - Test that the container app can be reached via "curl" like HTTP GET calls
     - Retrieve container log content
      - Create a SSH private/public key to be used when creating a container service
      - Create an Azure Container Service with Kubernetes orchestration
      - Log in via the SSH client and download the Kubernetes config
      - Create a Kubernetes client using the Kubernetes config file downloaded from one of the virtual machine managers
      - Create a Kubernetes namespace
      - Create a Kubernetes secret of type "docker-registry" using the Azure Container Registry credentials from above
      - Create a Kubernetes replication controller using a container image from the Azure private registry from above
          and a load balancer service that will expose the app to the world
 

## Running this Sample ##

To run this sample:

Set the environment variable `AZURE_AUTH_LOCATION` with the full path for an auth file. See [how to create an auth file](https://github.com/Azure/azure-libraries-for-java/blob/master/AUTH.md).

    git clone https://github.com/Azure-Samples/aci-java-scale-up-containers-using-acs.git

    cd aci-java-scale-up-containers-using-acs

    mvn clean compile exec:java

## More information ##

[http://azure.com/java](http://azure.com/java)

If you don't have a Microsoft Azure subscription you can get a FREE trial account [here](http://go.microsoft.com/fwlink/?LinkId=330212)

---

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.