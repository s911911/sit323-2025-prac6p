SIT323-6.1P: Deploying a Containerized Node.js App to Kubernetes

1.This project demonstrates deploying a containerized Node.js application onto a Kubernetes cluster using Minikube.

2. Build Docker Image
docker build -t shijingwei259/containerwebapp .
3. Push to Docker Hub
docker login
docker push shijingwei259/containerwebapp
4. Start Minikube
minikube start
5. Apply Kubernetes Deployment and Service
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
6. Access the Application
minikube service node-k8s-service
This will open the app in the default browser. If not, run:
minikube ip
Then go to:
http://192.168.49.2:30080
