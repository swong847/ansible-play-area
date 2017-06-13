Role Name
=========

This roles purpose is to install GPFS / Spectrumscale and alternatively upgrade it to the latest version, whilst building the GPL portability layer.

Requirements
------------

This role requires a little understanding of GPFS / Spectrumscale, please refer to the IBM manual for pre-requisits requirements.

Role Variables
--------------

Role dependencies require 'Install' or 'upgrade' and '3.4.0' or '3.5.0'.

I have created a gpfs role which will, depending on variable will install gpfs or upgrade and the repo_version will pull down the correct repos. By default, install and 3.4.0 are set 

ansible-playbook playbooks/gpfs34-upgrade/main.yml -e "ansible_user=root play=upgrade repo_version=3.5.0" -k -vvv




Example Playbook
----------------

---
      - hosts: "{{ target }}"
      roles:
         - cluster-install_sge-upgrade_gpfs

Author Information
------------------

Simon Wong: swong@dundee.ac.uk
