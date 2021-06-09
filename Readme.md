# Pasos a seguir:

gcloud auth login

gcloud config set project  charismatic-tea-305716

gcloud container clusters get-credentials cluster-kubernetes --zone=us-central1-c

En el directorio donde están todos los servicios y deployments
kubectl apply -f .

Es importante brir los puertos que se han escogido para las aplicacion en este caso 8000 y 8080.(se debe añadir una firewall para ello)

# Para escalar la aplicación podemos aplicar el comando 
kubectl get deployments --> listar los deployments activos

# Por ejemplo se ha escogido el  servicio web en este caso para escalarlo a 4 réplicas
kubectl scale deployment web --replicas 4

# Ver la app  en :
http://34.121.172.245:8080/--> frontend
http://35.192.211.111:8000/admin/ --> backend
 user: admin
 pass:admin1234
