### Commands
kubectl get all

kubectl create deployment mongo --image=mongo --dry-run=client -o yaml > mongo-deployment.yaml

kubectl apply -f mongo-deployment.yaml

kubectl delete deployment mongo

kubectl create service clusterip mongo --tcp=27017:27017 --dry-run=client -o yaml > mongo-service.yaml 

kubectl apply -f mongo-service.yaml

kubectl delete service mongo

kubectl create deployment mysql --image=mysql --dry-run=client -o yaml > mysql-deployment.yaml

kubectl apply -f mysql-deployment.yaml

kubectl create service clusterip mysql --tcp=3606:3606 --dry-run=client -o yaml > mysql-service.yaml

kubectl apply -f mysql-service.yaml

kubectl create deployment auth-service --image=spring-auth-server-demo:0.0.1-SNAPSHOT --dry-run=client -o yaml > auth-service-deployment.yaml

kubectl apply -f auth-service-deployment.yaml

kubectl create service clusterip auth-service --tcp=9000:9000 --dry-run=client -o yaml > auth-service-service.yaml

kubectl apply -f auth-service-service.yaml

kubectl create deployment api-gateway --image=spring-cloud-api-gateway:0.0.1-SNAPSHOT --dry-run=client -o yaml > api-gateway-deployment.yaml

kubectl apply -f api-gateway-deployment.yaml

kubectl create service clusterip api-gateway --tcp=8080:8080 --dry-run=client -o yaml > api-gateway-service.yaml

kubectl apply -f api-gateway-service.yaml

kubectl create deployment rest-mvc-service --image=rest-mvc-demo:0.0.1-SNAPSHOT --dry-run=client -o yaml > rest-mvc-service-deployment.yaml

kubectl apply -f rest-mvc-service-deployment.yaml

kubectl create service clusterip rest-mvc-service --tcp=8080:8080 --dry-run=client -o yaml > rest-mvc-service-service.yaml

kubectl apply -f rest-mvc-service-service.yaml

kubectl create deployment spring-webflux-service --image=spring-r2dbc-demo:0.0.1-SNAPSHOT --dry-run=client -o yaml > spring-webflux-service-deployment.yaml

kubectl apply -f spring-webflux-service-deployment.yaml

kubectl create service clusterip spring-webflux-service --tcp=8080:8080 --dry-run=client -o yaml > spring-webflux-service-service.yaml

kubectl apply -f spring-webflux-service-service.yaml

kubectl create deployment spring-webflux-fn-service --image=spring-reactive-mongo-demo:0.0.1-SNAPSHOT --dry-run=client -o yaml > spring-webflux-fn-service-deployment.yaml

kubectl apply -f spring-webflux-fn-service-deployment.yaml

kubectl create service clusterip spring-webflux-fn-service --tcp=8080:8080 --dry-run=client -o yaml > spring-webflux-fn-service-service.yaml

kubectl apply -f spring-webflux-fn-service-service.yaml


kubectl port-forward service/api-gateway 8080:8080

kubectl delete pods --all

#### Load images in minikube

minikube image load spring-r2dbc-demo:0.0.1-SNAPSHOT

minikube image load spring-reactive-mongo-demo:0.0.1-SNAPSHOT 

minikube image load rest-mvc-demo:0.0.1-SNAPSHOT 

minikube image load spring-auth-server-demo:0.0.1-SNAPSHOT 

minikube image load spring-cloud-api-gateway:0.0.1-SNAPSHOT

eval $(minikube docker-env)

eval $(minikube docker-env -u)