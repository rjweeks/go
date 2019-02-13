# Concourse and Kubernetes local development environment

Download official the [Concourse](https://github.com/concourse/concourse-docker) Docker image.

#### Check the official Concourse Readme for more details. Use this command to start:

> docker-compose up

#### Login to local Concourse

> fly -t local login --concourse-url http://localhost:8080

#### Setup the demo pipline

> fly -t local set-pipeline -p hello-test -c pipeline/k8s-deploy-pipeline.yaml --load-vars-from secrets

#### Unpause the pipeline

> fly -t local unpause-pipeline -p hello-test

#### Trigger the pipeline manually

> fly -t local trigger-job -j hello-test/test-deploy
