Role Name
=========

This role was created to help automate the setup new RHEL 7 out-the-box systems.  The purpose of this playbook was drafted from a previous sys_build/spacewalk script setup by {jjdoward}.  

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

As this playbook is tailored for our infrastructure environment, I couldnt share the variables set.  However, reading the variable names will make sense as to what should be placed there.  I decided to use ansible-vault to encrypt the local variables and to keep them out of public view.

Dependencies
------------

Run this playbook for systems running RHEL 7.1 and 7.2.

Example Playbook
----------------

An example of the playbook below can be found in the playbooks folder on my github playbooks/rhel7-setup.  Alternatively use the file below.  The auth file is the encrypted variables file.

  - hosts: rhel-dev
    roles:
     - rhel7-setup

    vars_files:
      - auth

ansible-playbook playbooks/rhel7-setup/main.yml -k


Author Information
------------------

Simon Wong : swong@dundee.ac.uk
