1. Start Minikube --> minikube start --cpus 2 --memory 4g
2. Create a PersistentVolumeClaim (PVC) --> kubectl apply -f mongodb-pvc.yaml
3. Create a MongoDB StatefulSet  --> kubectl apply -f mongodb-statefulset.yaml
4. Create a Headless Service for MongoDB  --> kubectl apply -f mongodb-service.yaml
5. Verify MongoDB Deployment

   kubectl get statefulsets mongodb
   kubectl get pods -l app=mongodb
   kubectl get services mongodb
   kubectl get pvc
