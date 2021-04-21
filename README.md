# Production Deployment with NGINX

Web Developers Toolkit: https://www.youtube.com/channel/UCdLqxzh_bocMmfgAdssvngg/featured

## Backend build command
* docker build -t backend -f openjdk.prod.dockerfile .
* docker tag backend:latest "repo-tag"/backend:v1
* docker push "repo-tag"/backend:v1

* kubectl apply -f kube.deploy.yaml
* kubectl apply -f kube.cipservice.yaml
* kubectl get pods
* kubectl exec -it "pod-name" -- sh
* apk add --no-cache curl
* curl http://backend-cip-service/api/resource


## Frontend build command

* docker build -t frontend -f nginx.prod.dockerfile .
* docker tag frontend:latest "repo-tag"/frontend:v1
* docker push "repo-tag"/frontend:v1

* kubectl apply -f kube.deploy.yaml
* kubectl apply -f kube.lbservice.yaml
