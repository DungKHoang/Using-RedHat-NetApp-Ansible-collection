# Using-RedHat-NetApp-Ansible-collection



## Pre-requisites
 - RHEL OS - current release
 - Python3 - current release
 - Ansible - current release
 - NetApp ONTAP collection from RedHat: **ansible-galaxy collection install netapp.ontap**


## Getting inventory from NetApp
 This set of playbooks will query iLO servers to collect data exposed with Redfish and generate CSV / JSON files

### CSV input file
  The CSV file contains list of IP addresses and credentials of NetApp storage. The format is:
  ip,username,password,site


### NetApp Inventory Playbooks

        - netapp-inventory.yml  --> netapp-inventory-tasks.yml    --> svm-sub-inventory.yml,interface-sub-inventory.yml,disk-sub-inventory.yml,colume-sub-inventory.yml

### Commands to run
        - ansible-playbook netapp-inventory.yml --extra-vars "netapp_csv=list-netapp.csv"


    



  
