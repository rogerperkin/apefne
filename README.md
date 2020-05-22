# Ansible Playbook Examples for Network Engineers - APEFNE

A collection of Ansible Playbooks for use by Network Engineers 

## How to use these playbooks

Clone this repository into your local machine, update the hosts file 

## 1: Shut and No Shut a port on Cisco Switch from prompted inputs 

## shutport.yml 

This playbook when run will prompt you for a switch name and then an interface name, the playbook will then shut the specified port pause for 5 seconds and then no shut the port. 

This playbook was developed for a customer who had a lot of ageing access points that needed to be regularly bounced. The playbook can easily be integrated into Tower. But the main concpets of this playbook are for you to grasp the vars_prompt input and also basic Cisco interface configuration commands 

https://docs.ansible.com/ansible/2.4/ios_interface_module.html
https://docs.ansible.com/ansible/2.6/user_guide/playbooks_prompts.html

## 2: Backup Cisco Router / Switch Config and run specified Show Commands and save output to file 

## backup.yml 

This playbook when run will pull the configurations from every device in the play and save the config into a daily created folder. It will also run a list of defined show commands and put all the show outputs into a single per device file. 
You will end up with a folder created for every day you run this playbook containing the device config and the device show ouputs 

This playbook also utilises the template.j2 file to get all the show outputs into a tidy format

In the vars_command list simply uncomment the commands you want to run - or add your own depending on your specific requirements

      - show spanning-tree blocked
      - show switch
      - show log
    #  - show environment all
    #  - show ip ospf int brief 
    #  - show ip ospf neigh 
    #  - show cdp neighbors detail


For more playbooks like this please check out my <a href="https://www.rogerperkin.co.uk/network-automation/ansible/course">Ansible Training for Network Engineers </a>







