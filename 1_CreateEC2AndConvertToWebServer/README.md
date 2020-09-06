## About

This Project handles an ansible deployment which includes the following:
* Launching an EC2 instance
* Installing the httpd Service
* Copying the sample web file to html directory


## Commands Used


##### To check the deployment in ansible playbook
```
ansible-playbook playbook.yaml -i inventory.txt --check
```

##### To deploy ansible playbook
```
ansible-playbook playbook.yaml -i inventory.txt
```
