Deploy to Kubernetes
====================
This is currently a work in progress.  The deployments and services will come up but interacting with them is not fully working.

Prerequisites
-------------
1. An existing Kubernetes cluster and proper access defined
1. `kubectl` >= 1.14 (needed for Kustomize to work)
    - You can also install `kustomize` separately [see here](https://kustomize.io/)
1. Update [pv.yml](pv.yml) with your Storage Details
    - More details about Persistant Volumes [here](https://kubernetes.io/docs/concepts/storage/persistent-volumes/#types-of-persistent-volumes)
1. Update [secrets.env](secrets.env) with your Spotify API Details
    - More details about how to do that [here](https://github.com/Yooooomi/your_spotify#creating-the-spotify-application)

Deploying
---------
From this directory (i.e. \<repo>/kubernetes) apply the kustomization.yaml

`kubectl apply -k .`

Still in Progress
=================
1. How to handle external access
     - Ingress
     - Service Loadbalancer