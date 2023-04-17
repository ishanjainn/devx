# devx

helm repo add prometheus-community https://prometheus-community.github.io/helm-charts && helm repo update && helm install ksm prometheus-community/kube-state-metrics --set image.tag=v2.8.2 -n default

helm repo add prometheus-community https://prometheus-community.github.io/helm-charts && helm repo update && helm install nodeexporter prometheus-community/prometheus-node-exporter -n default