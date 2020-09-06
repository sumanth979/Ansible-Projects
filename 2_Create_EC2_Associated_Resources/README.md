## About

* This Ansible deployment will create the following Resources:
  * ssh key
  * Uploading the ssh key to AWS
  * Security group for EC2
  * EC2 Instance
* Then it will wait untill the instance is started
* Then it will delete the resources in the following order:
  * EC2 Instance
  * Security group for EC2
  * ssh Key from AWS
 
#### Commands Used
```
ansible-playbook playbook.yaml
```
