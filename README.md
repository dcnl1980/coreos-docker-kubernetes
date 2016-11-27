# coreos-docker-kubernetes
Running kubernetes on single CoreOS node

curl -Lo kubectl https://storage.googleapis.com/kubernetes-release/release/v1.3.0/bin/linux/amd64/kubectl && chmod +x kubectl && sudo mv kubectl /opt/bin/

curl -Lo minikube https://storage.googleapis.com/minikube/releases/v0.12.2/minikube-linux-amd64 && chmod +x minikube && sudo mv minikube /opt/bin

minikube start

minikube dashboard


