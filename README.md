# Ansible Playbook Examples for Network Engineers 

A collection of Ansible Playbooks for use by Network Engineers 

## How to use these playbooks

Clone this repository into your local machine, update the hosts file 

## 1: Shut and No Shut a port on Cisco Switch from prompted inputs 

shutport.yml 

This playbook when run will prompt you for a switch name and then an interface name, the playbook will then shut the specified port pause for 5 seconds and then no shut the port. 

This playbook was developed for a customer who had a lot of ageing access points that needed to be regularly bounced. The playbook can easily be integrated into Tower. But the main concpets of this playbook are for you to grasp the vars_prompt input and also basic Cisco interface configuration commands 

https://docs.ansible.com/ansible/2.4/ios_interface_module.html




