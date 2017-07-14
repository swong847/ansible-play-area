Role Name
=========

The purpose of this playbook is to create a fileset on the Large File Store.   


Requirements
------------

Before creating the fileset, you will need to know the fileset name, fileset owner (e.g. username), fileset minuimum and maximum quota size and the owners group permissions.  For example;-
Fileset name: lsc
filset owner: cyscott
Fileset min & max quota: 1 10 (1T and 10T)
Group perm: hpcadmin

Role Variables
--------------

fsPath - has been set up so that this playbook can be used for other filesystems
fsName - has been set up to be used for other filesystems

bytes - default is T


Example Playbook
----------------

Run the command for the prompt menu
ansible-playbook playbooks/lfs-create-fileset/main.yml -e ansible_user=root -k

Run this command whilst passing in the values
ansible-playbook playbooks/lfs-create-fileset/main.yml -e ansible_user=root -k -e "fileset_name=lsc fileset_username=swong fileset_min_quota=1 fileset_max_quota=1 fileset_group_name=itadmin"



Author Information
------------------

Simon Wong
