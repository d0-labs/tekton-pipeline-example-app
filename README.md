# Tekton Pipelines Demo - Example App

## Overview

This repo is based on [alexwhen/docker-2048](https://github.com/alexwhen/docker-2048), which is in turn based on [gabrielecirulli/2048](https://github.com/gabrielecirulli/2048).

## Purpose

This repo contains a sample app (Dockerized 2048-game) which we will use to demonstrate how to set up and run Kubernetes-native appliation builds and deployments using [Tekton](https://tekton.dev) and [ArgoCD](https://argoproj.github.io).

* [Tekton](https://tekton.dev) &rarr; define pipelines
* [ArgoCD](https://argoproj.github.io) &rarr; manage Kubernetes application deployment

## Pre-Requisites

To use this sample repo as part of our Tekton/ArgoCD demo, you need a Kubernetes cluster with the following installed:
* [Ambassador Edge Stack](https://www.getambassador.io) with TLS
* [ArgoCD](https://argoproj.github.io)
* [Tekton](https://tekton.dev)

To find out how to install the above tools in your Kubernetes cluster, check out our [Medium blog post](https://medium.com/dzerolabs/installing-ambassador-argocd-and-tekton-on-kubernetes-540aacc983b9). It has all the gory details you need to get started!

## Build and Run Dockerfile Locally

To try building and running the Dockerfile locally yourself:

```bash
# Build
docker build -t docker-2048:1.0.0 .

# Run in interactive mode
docker run -it -p 80:8000 docker-2048:1.0.0
```

Once the Docker image is built, you can check it out at: `http://localhost`

## Tekton Pipeline & ArgoCD Application Deployments

Looking how to use Tekton and ArgoCD to build and deploy this code to your Kubernetes cluster? Head on over to [d0-labs/tekton-pipeline-example-pipeline](https://github.com/d0-labs/tekton-pipeline-example-pipeline)

