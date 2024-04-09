Modules: Different action run by taks called as modules 

Ansible-lint : Ansible Lint is a command line tool that perform linting on Ansible Playbooks roles and collections 
              - its used to check bug erros one your file 

  Variable 
      Variable types: 
             -  Number
             - string 
             - boolen
             - Diston ary 
              
Check mode and Diff mode need to learn 

Loop ? 

Ansible Interview Que :
Why we use Ansible ?
- Ansible is Agentless 
- SSH in ansible that is secure 
- ansible use push architeture

  Ansible Modules:
   - Ansible modules are units of code that can control system resources or execute system commands
  Ansible inventry :
    - its a YAML file we can store Remote server information
    2 types :
      dyanamic and manual

   If i have lot of file i want to copy it from host to remote server using ansible ?
 -  we can use COPY module also there are one more option is syncronized module we need to specify and sounce and destination under that

   How to encrypt file 
   ansible valut encrpt file name 

   hoe to create encrpted file 
   ansible valut create encrpt filename 

what is difference between play and playbook
play contain more number of taks 
playbook contain more number of plays 
   
ansible_facts: ansible_facts is used to os specific variable  
 CI/CD  : If we stremling development and deploying process we called it CI and once CI is done like we have writen a code and we have push it to remote repositry we called as CD 
 
 lookup puglins : 
