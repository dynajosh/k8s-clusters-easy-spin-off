# k8s-clusters-easy-spin-off
Easily spin off Kubernetes clusters on major cloud providers

To spin off Kubernetes clusters on Google's GCP, follow these steps
GCP offers a hosted K8s as a service. This service is known as Google Kubernetes Engine (GKE).
To get started with GKE, you need the following:
- A GCP account on which billing has been enabled.
- The gcloud tool installed. (To install gcloud, visit here https://cloud.google.com/sdk/docs/install-sdk)

Once you have gcloud installed, set a default zone:
To set a default zone, visit your terminal and run: $ gcloud config set compute/zone us-west1-a (where us-west-1a refers to the zone and can be replacd with any zone of your choice)

Next, create a cluster
To create a cluster, visit your terminal and run: $ gcloud container clusters create kuar-cluster
Allow this to run for a couple of minutes it might take a while because a fresh cluster is being prepared for you.
When the cluster is ready, you can fetch the credentials for the cluster by running this command in your terminal: $ gcloud auth application-default login
