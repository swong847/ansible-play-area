Role Name
=========

LDAP to WINBIND.  The purpose of this playbook is to migrate from LDAP to WINBIND

Requirements
------------

The requirements to run this playbook are;
- Machines running LDAP
- Samba3x

Within the playbook, I had to create two separate run times.  First was a pre-task which had to run as <user> to enable permitRootLogin.  The reason this had to be enabled was down to the fact, when winbind tried to join to the AD server, ssh access for the <user> was disabled.  The playbook had to ssh as root to do the join and restart winbind.  I couldnt see a way to resolve this, trying become: true and become_user: root, resulted in no change.


Role Variables
--------------

Very few variables are set due to the short amount of tasks being run.  The only variable set was for the root ssh access which has been encrypted using ansible-vault

Dependencies
------------

The dependencies required are;
- The machine should have the spacewalk certifcate applied.  I have written this into the playbook to avoid any errors when trying to install samba3x

Example Playbook
----------------
To run the playbook, run the command below.  The first password will be your AD password, the second password will ask you for the vault password.  This is our standard admin auth.

- You need to edit the playbook 'hosts'.  This can be done at ansible/playbooks/ldap-to-winbind/main.yml, editing the hosts to all or individual host is required1

'ansible-playbook playbooks/ldap-to-winbind/main.yml -k --ask-vault-pass'


License
-------

BSD

Author Information
------------------
Simon Wong


