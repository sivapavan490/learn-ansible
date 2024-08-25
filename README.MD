Devops-practice
DevOps321
    Here we will mention the variables from differet styles.
        1. vars # variables at play level refer variable-play.yaml
        2. vars # variables at task level. Here play level variables r override by the task level variables. refer variables-task.yaml
        3. vars_files refer variables from files.
        4. vars_prompt refer vars-prompt.yaml
        5. 
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
 ansible-playbook -i inventory -e ansible_user=username -e ansible_password=password filename ```# to run ansible play books
```
 nohup ansible-playbook -i inventory -e ansible_user=username -e ansible_password=password filename & /dev/null ``` --> to run ansible playbooks in the background we use this command