<<<<<<< HEAD
# Production Deployment with NGINX

Web Developers Toolkit: https://www.youtube.com/channel/UCdLqxzh_bocMmfgAdssvngg/featured

## Backend build command
* docker build -t backend -f openjdk.prod.dockerfile .
* docker tag backend:latest <repo-tag>/backend:v1
* docker push <repo-tag>/backend:v1

* kubectl apply -f kube.deploy.yaml
* kubectl apply -f kube.cipservice.yaml
* kubecl get pods
* kubectl exec -it <pod-name> -- sh
* apk add --no-cache curl
* curl http://backend-cip-service/api/resource


## Frontend build command

* docker build -t frontend -f nginx.prod.dockerfile .
* docker tag frontend:latest <repo-tag>/frontend:v1
* docker push <repo-tag>/frontend:v1

* kubectl apply -f kube.deploy.yaml
* kubectl apply -f kube.lbservice.yaml
=======
# Frontend

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 11.2.5.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.
>>>>>>> 120375f (initial commit)
