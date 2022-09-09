# Docker_Kubernetes_Group05

Solo aplica para cuando el servicio es tipo ClusterIP
kubectl port-forward svc/frontented-svc 7000:80


docker compose up -d
docker compose up -d --build


//En la seccion (image: localhost:5000/nombre_imagen)
docker compose push

# Ver cuanto recursos puede usar un contenedor
docker stats container_name



#aplicando manifiesto del deploy del ingres controller
kubectl apply -f https:raw/github/.... 


kubectl exec -it nombre_pod -- sh

kubectl describe pod liveness-cmd

kubectl describle deploy name_deploy

# OS2-Code-Resources
Operative Systems 2. First semester of 2022.

## Description
This project consists on a group of examples useful for the course.
## Instructions
You can check the examples of the different parts of the content:
 - [Part 1](./part1)
 - [Part 2](./part2)
 - [Part 3](./part3)
