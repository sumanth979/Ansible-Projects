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

#### Output
```
PLAY [Create all the resources required for Launching an ec2 instance] ***********************************************************************************************************************************************************************

TASK [Gathering Facts] ***********************************************************************************************************************************************************************************************************************
ok: [localhost]

TASK [Create an ssh key] *********************************************************************************************************************************************************************************************************************
changed: [localhost]

TASK [Upload public key to AWS] **************************************************************************************************************************************************************************************************************
changed: [localhost]

TASK [Create security group] *****************************************************************************************************************************************************************************************************************
changed: [localhost]

TASK [Launch EC2 Instance using ansible] *****************************************************************************************************************************************************************************************************
changed: [localhost]

PLAY [Delete the created resources] **********************************************************************************************************************************************************************************************************

TASK [Gathering Facts] ***********************************************************************************************************************************************************************************************************************
ok: [localhost]

TASK [Terminate the created ec2 instances that were previously launched] *********************************************************************************************************************************************************************
changed: [localhost]

TASK [Delete the security group created] *****************************************************************************************************************************************************************************************************
changed: [localhost]

TASK [Remove the uploaded SSH key] ***********************************************************************************************************************************************************************************************************
changed: [localhost]

PLAY RECAP ***********************************************************************************************************************************************************************************************************************************
localhost                  : ok=9    changed=7    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
```
