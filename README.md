# Kubernetes Nginx Demo

Kubernetes nginx deployment from docker image.

### Running k8s deployment

**1. Start Minikube**
```shell
minikube start
```

**2. Deployment**
```shell
cd ~/your-path/kubernetes-nginx-website

eval $(minikube docker-env)

docker image build -t ashwindinesh/nginx-website .

kubectl apply -f deployment.yml
```

**3. Test**
```shell
minikube service nginx-service --url
```

Enter the output URL from the above command in your browser.

**Note:** For using docker image from dockerhub, remove the argument 'imagePullPolicy: Never' from the `deployment.yml` file.
