# Docker

docker build -t tunisia-1998 .  
docker build -t tunisia-2004 .

docker tag tunisia-1998 karim10/tunisia-1998:latest  
docker tag tunisia-2004 karim10/tunisia-2004:latest

docker push karim10/tunisia-1998:latest  
docker push karim10/tunisia-2004:latest

# Deplyoment

kubectl apply -f deployment.yaml  
kubectl get deplyoments  
kubectl get pods  
kubectl delete deployment <deployment-name>  
kubectl delete deployment --all

kubectl rollout status deployment/tunisia-deployment  
kubectl rollout undo deployment/tunisia-deployment

# Services

kubectl apply -f service.yaml  
minikube service tunisia-service --url

kubectl delete service <service-name>  
kubectl delete service --all

# Minikube

minikube stop  
minikube start  
minikube addons enable ingress  
minikube tunnel  
minikube ip  
minikube addons list
