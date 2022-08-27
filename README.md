# k8s-deployment

Step1 : Run minikube cluster

Step2 : Clone this repository and Run script 1_create_docker_images.sh to create 4 docker images one for each application(cart, payment, shop and checkout)

Step3 : Run helm chart to deploy application.

        helm install web-app helm-chart-web-app/ -f helm-chart-web-app/values.yaml

Step 4 : Deploy Prometheous and Grafana using Helm chart

         helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
         helm repo update
         helm install prometheus prometheus-community/kube-prometheus-stack -n monitoring --create-namespace 


