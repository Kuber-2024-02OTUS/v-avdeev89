1 - install kube-prometheos

LATEST=$(curl -s https://api.github.com/repos/prometheus-operator/prometheus-operator/releases/latest | jq -cr .tag_name) && curl -sL https://github.com/prometheus-operator/prometheus-operator/releases/download/${LATEST}/bundle.yaml | kubectl create -f -

2 - aplly 
kubectl apply -f namespace.yaml

kubectl apply -f deployment.yaml

kubectl apply -f service.yaml

kubectl apply -f serviceMonitor.yaml
