# K8s_Component
Deploy an application: MongoExpress with the Web Interface from its image in the DockerHub to Request the Mongo DB (also its image in the DockerHub)
Work flow and picture outline: let's see in 2 pictures in this repo

![Outline of the project](https://github.com/user-attachments/assets/51892eaf-ae98-4593-9d1f-7030109f5106)

![Workflow-Step by step](https://github.com/user-attachments/assets/07122d68-c741-4ad5-a40d-33287e4286f7)

### kubectl apply commands in order
    
    kubectl apply -f mongo-secret.yaml
    kubectl apply -f mongo.yaml
    kubectl apply -f mongo-configmap.yaml 
    kubectl apply -f mongo-express.yaml

### kubectl get commands

    kubectl get pod
    kubectl get service
    kubectl get secret
    kubectl get all | grep mongodb

### kubectl debugging commands

    kubectl describe pod mongodb-deployment-xxxxxx
    kubectl describe service mongodb-service
    kubectl logs mongo-express-xxxxxx

### give a URL to external service in minikube

    minikube service mongo-express-service

    user:admin
    password:pass 

![Screenshot from 2024-11-07 17-12-45](https://github.com/user-attachments/assets/4bfc5b28-fdcf-4f6f-986a-582353a0d9b3)
    
