# Proxima Centauri 
A Kubernetes Test Cluster

## Minikube
https://minikube.sigs.k8s.io/docs/start/

    minikube start 
<br>
    
    minikube delete --all

## ArgoCD
https://argo-cd.readthedocs.io/en/stable/

    kubectl create namespace argocd
<br>

    kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/master/manifests/install.yaml
<br>

    kubectl port-forward svc/argocd-server -n argocd 8080:443
<br>   

    kubectl get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" -n argocd | base64 -d
