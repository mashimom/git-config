# Installs and configures git

The role will install git from repos, then will create ssh key pair if missing, next configure sensible defaults like user, email and push style, merge conflict to 3-way, line ending and git attribute defaults from template.

Requirements
------------

Currently work with apt, tested on Ubuntu and Ubuntu bash for Windows.

Role Variables
--------------
Any missing value causes role failure.

| Variable name | default value | required | advised to encrypt in host_var vault |
| -- | -- | -- | -- |
| `GITCFG_NAME` | | yes | no |
| `GITCFG_USER` | | yes | no |
| `GITCFG_EMAIL` | | yes | no |
| `GITCFG_PASSWORD` |  | yes | yes |
| `GITCFG_KEYTYPE` | rsa | yes | no |


Dependencies
------------

No dependencies.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:
    
    ---
    - hosts: localhost
     
      roles:
        - role: git-config
          GITCFG_NAME: Scott Summers
          GITCFG_USER: scott
          GITCFG_EMAIL: cyclops@xmen.com
          
Host vars contains password `host_vars/localhost`:

    GITCFG_PASSWORD: jeangrey
    
License
-------

MIT

Author Information
------------------

@mashimom