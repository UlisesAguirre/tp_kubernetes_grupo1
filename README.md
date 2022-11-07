# TP Kubernetes - Grupo 1 

The steps and commands we used to achieve the assigned tasks are the following:

First things first, we create a kubernetes cluster. In our case, we used the kind tool: kind create cluster --name tp-grupo1

Second step is to create the directory in which the different files will be placed with the mkdir <directoryName> command

Then, we create both the index.html with "Hola mundo, somos el grupo 1 de la UTN" as its content and the Dockerfile that will be used to build the image using the VIM editor.

Once those files have been created, we build the image using the following command:  docker build -t tp-grupo1:v1 . 
Right after, we create a variant of the image following the Docker Hub format: docker tag tp-grupo1:v1 ulisesaguirre/tp-grupo1:v1 
Finally, we push the image to the Docker Hub repository: docker push ulisesaguirre/tp-grupo1:v1

After we've done those steps we can:

> 1) create the namespace: kubectl create ns grupo1
> 2) apply the .yaml definition file: kubectl -n grupo1 apply -f replicaset.yaml
> 3) connect to one of the pods we've creted:  kubectl -n grupo1 port-forward (nombre-del-pod) -f 8080:80

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Group members:
- Aguirre Ulises
- Cechetto Juan Cruz
- Brunetti Marco
- Bruzzo Luca
