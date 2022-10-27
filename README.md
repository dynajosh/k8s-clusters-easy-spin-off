# k8s-clusters-easy-spin-off
Easily spin off Kubernetes clusters on major cloud providers

============GOOGLE CLOUD PLATFROM================

To spin off Kubernetes clusters on Google's GCP, follow these steps
GCP offers a hosted K8s as a service. This service is known as Google Kubernetes Engine (GKE).
To get started with GKE, you need the following:
- A GCP account on which billing has been enabled.
- The gcloud tool installed. (To install gcloud, visit here https://cloud.google.com/sdk/docs/install-sdk)

Once you have gcloud installed, set a default zone:
To set a default zone, visit your terminal and run: $ gcloud config set compute/zone us-west1-a (where us-west-1a refers to the zone and can be replacd with any zone of your choice)

Next, create a cluster
To create a cluster, visit your terminal and run: $ gcloud container clusters create demo-cluster
Allow this to run for a couple of minutes it might take a while because a fresh cluster is being prepared for you.
When the cluster is ready, you can fetch the credentials for the cluster by running this command in your terminal: $ gcloud auth application-default login

================MICROSOFT AZURE==================

To spinoff Kubernetes on Microsoft Azure

Microsoft Azure offers a hosted k8s as a service. An easy way to get started with the Microsoft Azure Container Service is via the use of the built in Azure Cloud Shell found int he Azure Portal.

You can either activate the shell by the click of the shell icon found in the tool bar (You'll know it when you see it. It looks like the regular icon for shells and can be found in the upper right side of the toolbar)

OR

You can decide to install the az command line interface on your local computer from here https://learn.microsoft.com/en-gb/cli/azure/install-azure-cli
After installation has been completed and you have the shell up and running you can execute the following commands:

You can create a resource group nby running:
$ az group create --name=demo --location=westus

After the resource group has been created, proceed to create a cluster by running:
$ az aks create --resource-group=demo --name=demo-cluster

This might take a couple of minutes as well and you can proceed to get credentials for the cluster after it has been created by running:
$ az aks get-credentials --resource-group=demo --name=demo-cluster

Install the kubectl tool by running:
$ az aks install-cli
