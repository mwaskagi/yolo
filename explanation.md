## Client and backend
- Base Image : - node:10-slim image due to it size and also has few dependancies making it stable for my project for client while node:alpine  for the backend

## Docker
-  Two separate Dockerfile for each container eac having different package requirements and port configuration

## Vagrant
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
