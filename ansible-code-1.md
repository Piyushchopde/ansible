---
- name: Install Nginx, MySQL, and perform additional tasks
  hosts: your_target_hosts
  become: yes

  vars:
    user_name: myuser
    group_name: mygroup
    script_path: /path/to/your_script.sh
    src_file_path: /path/to/source/file
    dest_file_path: /path/to/destination/file
    packages_to_install:
      - name: nginx
        service_name: nginx
      - name: mysql-server
        service_name: mysql

  tasks:
    - name: Update apt cache
      apt:
        update_cache: yes
      when: ansible_os_family == 'Debian'

    - name: Install required packages and ensure services are running
      apt:
        name: "{{ item.name }}"
        state: present
      loop: "{{ packages_to_install }}"
      when: ansible_os_family == 'Debian'

    - name: Ensure services are running and enabled
      systemd:
        name: "{{ item.service_name }}"
        state: started
        enabled: yes
      loop: "{{ packages_to_install }}"
      when: ansible_os_family == 'Debian'

    - name: Run a command
      command: echo "This is a command"
      
    - name: Execute a shell script
      shell: "{{ script_path }}"
      
    - name: Copy a file
      copy:
        src: "{{ src_file_path }}"
        dest: "{{ dest_file_path }}"
      
    - name: Add a group
      group:
        name: "{{ group_name }}"
        state: present
      
    - name: Add a user
      user:
        name: "{{ user_name }}"
        state: present
        groups: "{{ group_name }}"  # Add the user to the specified group
