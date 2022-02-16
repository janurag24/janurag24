# Kubernetes Cluster Setup Guide

## Start a small K8s cluster with 1 node in Google Cloud

```sh
gcloud services enable artifactregistry.googleapis.com container.googleapis.com
gcloud config set compute/region asia-south1
gcloud config set compute/zone asia-south1-c
gcloud container clusters create hello-cluster --num-nodes=1
gcloud container clusters get-credentials hello-cluster
