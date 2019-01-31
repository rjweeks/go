# Concourse and Kubernetes local development environment

Download official [Concourse](https://github.com/concourse/concourse-docker) Docker image.

cat token | base64 --decode


fly -t local login --concourse-url http://localhost:8080

fly -t local set-pipeline -p hello-test -c pipeline/k8s-deploy-pipeline.yaml --load-vars-from secrets
