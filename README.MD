Devops-practice
DevOps321

* If we want to login from ansible server to other servers. we will follow below process

# sshpass -p "password" ssh username@I.P address

* below cmd check the server is reachable or not 
```
    ansible -i 18.233.62.89, all -e ansible_user=centos -e ansible_password=DevOps321 -m ping
```

   here, i - inventory file or I.P address
         e  - variable representation
         m  - module

 ansible -i 18.233.62.89, all  -e ansible_user=centos -e ansible_password=DevOps321 --become -m yum -a "name=nginx, state=present"

 to run a playbook file in ansible we use below cmd model

 ```
 ansible-playbook -i inventory -e ansible_user=username -e ansible_password=password filename
