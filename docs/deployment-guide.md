# Deployment Guide

## Prerequisites
- Kubernetes Cluster
- kubectl installed
- Storage Class configured

## Steps

### Deploy Storage
kubectl apply -f dbpvc.yaml/

### Deploy Services
kubectl apply -f appservice.yaml/
kubectl apply -f dbservice.yaml/
kubectl apply -f mcservice.yaml/
kubectl apply -f rmqservice.yaml/

### Deploy Database
kubectl apply -f dbdeploy.yaml/

### Deploy Backend Services
kubectl apply -f rmqdeploy.yaml/
kubectl apply -f mcdep.yaml/

### Deploy Application
kubectl apply -f appdeploy.yaml/

### Configure Ingress
kubectl apply -f appingress.yaml/

### Configure Secrets
kubectl apply -f secret.yaml/
