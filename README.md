#Keep all files in same folder 

Practice and run commands - 
( i used 2 server , first one is master node and second One is worker node and try to Run Script in both and created a cluster Setup ready Ansible guide )

1 ansible --version

2 ansible all -i 192.168.31.11, -m ping 
    #when you want to target without specifying any hosts.ini

3 ansible cluster -m ping 
    #after_creating_host.ini
    ansible masternode -m ping (individual run)

4 ansible all -a "any_command"
    ansible all -a "sudo apt update" -v ( to see what's going on )

5 sudo EDITOR=vim visudo
  anshul ALL=(ALL) NOPASSWD: ALL (add this line in the end )
  **Use this to give superuser permission

6 ansible-playbook cluster_playbook.yml -v

7 if any error occur's in a specific task rerun playbook from that task using --
    ansible-playbook cluster_playbook.yml --start-at-task="Execute the script_join-command.sh"
