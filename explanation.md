#### Client and backend
- Base Image : - node:10-slim image due to it size and also has few dependancies making it stable for my project for client while node:alpine  for the backend

#### Docker
-  Two separate Dockerfile for each container eac having different package requirements and port configuration

#### Vagrant
- Install vagrant then initialized to create a vagrantfile which i edited
 - Add  box : "config.vm.box = "geerlingguy/ubuntu2004""
 - Set provision for ansible :
 config.vm.provision "ansible" do |ansible|
 ansible.playbook = "playbook.yml"
 end
  - Forwarded ports 3000 and 5000
- create hosts.inv to contain the servers IP addresses
- Added ansible config file, which contains the default setting for connection
- created roles folder to contain the tasks which will be deploys our application once the playbook.yml file is executed
- created the playbook with the roles and place it on the root folder.


#### K8s Objects
- `Backend Deploy YAML`
  - Defines backend application and its external service of type `LoadBalancer`
  - The backend service accepts requests on port 5000 which forwards to the backend container also running on port 5000
  - `ConfigMap` to access `MONGODB_URL` variable which are defined in the mongo.yml file.
- `Client Deploy YAML`
  - Defines its external service of type `LoadBalancer`
  - The frontend service accepts requests on port 3000 which forwards to the frontend container also running on port 3000
- `statefulSet YAML`
  - Defines its service of type `ClusterIP`
  - The mongo db service will utilize its connectivity with other pods within the cluster network to process and manage application data. Mongo db service is accessible via port 27017
- `Database YAML`
  - Maps mongo db deployment and a volume.

- Configs
 - Setup project 
  ```
    gcloud config set project [PROJECT_ID]
  ```
 
 - Setup default computer zone and location
  - contains the region location on where the cluster will operate by setting up the default region and default zone
    ```
     gcloud config set compute/region us-central1
     gcloud config set compute/zone us-central1-a
    ```
-  After setting up Googleregion and zone,create a kubernetes cluster on GKE
    ```
    gcloud container clusters create --machine-type=e2-medium --zone=us-central1-a yolo-cluster
    ```
-  Connected to the cluster:
  
    ```
    gcloud container clusters get-credentials yolo-cluster --zone us-central1-a
    ```
- Cloned the yolo repo
- Applied the deployment files using kubectl.
    ```
    kubectl apply -f k8_manifests
    ```