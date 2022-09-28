AD_join
=========

Role to join Active Directory for Debian and Ubuntu machines.

Role Variables
--------------

! defaults/main.yml
* **ad_pkgs_update**: Bool for activate package update
* **ad_realm**: Keberos real for domain
* **ad_domain**: Domain to join
* **ad_ou**: OU where add computer object
* **ad_admin_username**: User used for join AD
* **ad_admin_password**: Password of previous user
* **ad_other_domain_to_realm**: Other Realms for domain (optionnal) 
* **ad_permit_groups**: AD permit to use the joined machine (optionnal) 
* **ad_default_shell**: Default shell for AD users
* **ad_home_dir**: Default home directory for AD users
* **ad_replace_sss_conf**: Replace all `/etc/pam.d/common-session` file or juste add required line to it
* **ad_reboot_if_require**: Reboot when host is joined to AD if necessary
* **ad_config_ssh**: Enable or disable SSH config
* **ad_ssh_display_motd**: Enable MOTD on ssh connexion
* **ad_ssh_banner**: Enable SSH banner
* **banner_header**: SSH banner content

! vars/main.yml
* **sftp_server_location**: Location for sftp server in ssh config
* **ad_pkgs**: List of required packages install with this role
* **banner_file**: Location for ssh banner

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - thystips.AD_join

License
-------

GPLv3

Author Information
------------------

ThysTips <contact@thystips.net> \
Gitlab: https://gitlab.com/thystips \
Github: https://github.com/thystips
