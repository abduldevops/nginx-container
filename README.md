# nginx-container
Using vagrant/aws, ansible  build nginx container and deploy it.

## Vagrant - Ansible- Docker - Build and deploy Nginx

1.Install vagrant,virtual box, ansible
2.




## AWS - Ansible - Docker - Build and deploy Nginx

Ansible can not install on windows so use AWS.

spin 2 EC2 instances first instance act as Ansible server/Control instance and second is node nstance,
In both instances create ansible user and make sure that each will communicate with each other without password.
make sure that ssh port is open for communication. 

on node instance open tcp ports: 8085,8087 and 8090
update the inventory file with node instance ip address [file location: inventory/hosts]

## Playbooks usage.
### playbook.yml 
It will install docker,build nginx image and create nginx container which will be access on node host(ip address) port 8087

### playbook-test.yml 
Few test cases which will be execuated on node host

### playbook-compose.yml 
It will install docker,build and deploy the nginx and mysql containers whcih will access on node host(ip address) port 8090
it will display "Hello World"

### playbook-compose-test-yml - it will deploy the new html content on node instance.
it will display "Welcome to Micro services" 
here we modify the html content and call docker-compose build and docker-compose up

 - copy the html contnet
 - docker-compose build
 - docker-compose up -d





