# Ecommerce-Ansible

This playbook is a project designed to validate the Ansible Basics course by KodeKloud: https://kodekloud.com/courses/ansible-for-the-absolute-beginners-course/ <br>
Its purpose is to automate the deployment of a Linux-Apache-MariaDB-Php Ecommerce Application using Ansible.

The setup includes two VMs - one serving as the Apache Web server running PHP, and the other acting as a MariaDB database server. The VM images used are Ubuntu 22.04 LTS, and I utilized my laptop as the Ansible controller since the VMs were bridged to my LAN and assigned IP addresses.

To simplify the process, I added my SSH key to the Ubuntu image using the **ssh-copy-id** command and added the following line to the **/etc/sudoers.d/ryad** file: ```ryad ALL=(ALL) NOPASSWD: ALL``` <br>
This ensured a smooth connection without having to provide passwords in the inventory file or while executing commands that require root privileges.

Please note that the 'Adding settings to MariaDB configuration to enable remote access' task may not work for everyone, as the location of the MariaDB file can vary. In my case, it was located at /etc/mysql/my.cnf, but it may be located elsewhere. For more information on this task, please refer to the MariaDB documentation: https://mariadb.com/kb/en/configuring-mariadb-for-remote-client-access/







