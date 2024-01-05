# ansible

Ansible is a configuration management tool which works both on push and pull mechanisms

### Ansible is very famous and is widely used in the industry and it's quite popuolar!!! Want to know the the PROS's of it if?

1) Ansible is an agent-less software !!!
2) Ansible uses SSH as a default mechanism to communicate to other servers (port number : 22)
3) The only thing that Ansible Node expects is, communication to other servers that needs CM!
4) Ansible works both with PUSH & PULL Mechanism.
5) Common credentials accross the board (Ansible server should be able to ssh to any of the server)
6) Ansible goes by declarative approach and their documentation is really vast and good. 
7) Operations are parallel with Ansible (Multiple CM's are doable)
8) Code doest need to be on the top of a local server !!!



### Important Points To Be Notes :

1) Ansible in the backend uses python !!!
2) When you install ansible, by default it installs "ansible version2 which is from python2".
3) python2 is sunset on jan 2020.
4) lates version of Ansible or versions of ansible after 2 are python3 based. ( so to install Ansible >2 , you need to have python3)
5) By default on all AWS AMI's , you will have python2 by default.




ansible ----> redhart ----> IBM   ( IBM is a Redhart product now and still it's opensource )


### INVENTORY File

Inventory is nothing but the list of machine ip or dns names that you want ansible to be managed.

### HOW Can we operate Ansible?

Ansible can be operates in 2 ways 

   1) manual Approach
   2) Automate approach

## manual approach
   $ ansible -i inv all -e ansible_user=centos  -e ansible_password=DevOps321  -m shell -a uptime.
   $ vim inv to add All the servers in one operator machine
   $ ansible -i inv all -m ping

## One of the most widely asked interview question
  ## How to know the list of the machines mentionned in the inventory are up or not?
  $ ansible -i inv all -e ansible_user=centos -e ansible_password=DevOps321 -m ping



## What is  playbook ?
  
  A playbook is the list of plays..
  A Play is a list of tasks ...
  A Task is an action that you want to execute!

  On hight-level, playbook is an ansible script to execute things parallely

## What is the language used by playbook ?
  
   YAML is the language used by ANSIBLE to write playbooks.

## What is a Marupup Language?

  Markup Language is a Presentation Language !!!
    Ex: html, xml

## how to run ansible-playbooks?
   $ ansible-playbook -i inv -e ansible_user=centos  -e ansible_password=DevOps321 playBookName.yaml