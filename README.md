# coreos-docker-kubernetes
Running kubernetes on single CoreOS node

curl -Lo kubectl https://storage.googleapis.com/kubernetes-release/release/v1.3.0/bin/linux/amd64/kubectl && chmod +x kubectl && sudo mv kubectl /opt/bin/

docker run --net=host -d -v /var/run/docker.sock gcr.io/google_containers/hyperkube:v0.14.1 /hyperkube kubelet --api_servers=http://localhost:8090 --v=2 --address=0.0.0. --enable_server --hostname_override=127.0.0.1 --config=/etc/kubernetes/manifests

docker run -d --net=host --privileged gcr.io/google_containers/hyperkube:v0.14.1 /hyperkube proxy --master=http://127.0.0.1:8090 --v=2

kubectl get notes
