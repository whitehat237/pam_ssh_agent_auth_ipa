pam_ssh_agent_auth_ipa
======================

An ansible playbook to configure pam and sudo on IPA enrolled machines.  
The changes made by the playbook to pam and sudo enable a user to perform (authenticated) sudo elevation 
via ssh public key lookup using sssd and the pam_ssh_agent_auth library, 
when the authenticating IPA user has a public key enrolled on their user object in IPA.  (SSH public key attribute added on their account)

Requirements
------------

The playbook has no external dependencies.
A limit value must be provided at runtime

Using this repository
---------------------

```bash
git clone https://github.com/whitehat237/pam_ssh_agent_auth_ipa.git
```

Running the playbook
--------------------

```bash
cd pam_ssh_agent_auth_ipa
ansible-playbook playbook.yml -i ~/inventory.yml --limit myhost.example.net --user local --become -kK
```
