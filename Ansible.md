- Ansible Modules: Ansible modules are units of code that can control system resources or execute system commands
         
          - system 
          - command
          - file
          - database 
          - cloud 
          - windows 
          - Service modules
          - lineinfile module 

- Plugins: pieces of code that augment Ansible's core functionality
- Ansible roles:Ansible Roles provide a structured way to organize tasks, templates, files, and variables.
- Ansible-lint : Ansible Lint is a command line tool that perform linting on Ansible Playbooks roles and collections 
              - its used to check bug erros one your file
  command: ansible-lint playbook.yml
- Variable 
      Variable types: 
             -  Number
             - string 
             - boolen
             - Diston ary 
              
- Check mode : In check mode, Ansible runs command  without making any changes on remote systems
           command : ansible-playbook -i inventory playbook.yml --check 
- Diff mode : command is used to show the differences or changes that Ansible would make to the target system.
         command: ansible-playbook -i inventory playbook.yml --diff 
- Loop:  used to repeat any task or a part of code multiple times in an Ansible-playbook


- Why we use Ansible ?
    Ansible is Agentless 
    SSH in ansible that is secure 
    ansible use push architeture

 
- Ansible inventry :
    - its a YAML file we can store Remote server information
      2 types :
        dyanamic and manual

- If i have lot of file i want to copy it from host to remote server using ansible ?
    we can use COPY module also there are one more option is syncronized module we need to specify and sounce and destination under that

- How to encrypt already created file  file :   ansible valut encrpt file name 

- how to create encrpted file Command: ansible-vault encrypt <file_name>

- ansible-playbook -i encrypted_inventory playbook.yaml --ask-vault-pass

- what is difference between play and playbook
   play contain more number of task 
   playbook contain more number of plays 
   
- ansible_facts: ansible_facts is used to os specific variable  

 CI/CD  : If we stremling development and deploying process we called it CI and once CI is done like we have writen a code and we have push it to remote repositry we called as CD 
 
 lookup puglins : 


Templating : 
jinja2 : 

