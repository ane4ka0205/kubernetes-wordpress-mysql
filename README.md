# kubernetes-wordpress-mysql

First create key and certificate. Create a secret by using them:
kubectl create secret tls ingress-tls --cert=ingress.crt --key=ingress.key

kubectl create -f wordpress-home.yaml
kubectl create -f mysql-home.yaml

Create ingress by using wordpress service:
kubectl create -f mydomain-home-ingress-tls.yaml
