# asbl-vaultwarden_to_file_copy

## Description

This repo contain the ansible role to get vaultwarden secret, store them in files and finally copy files to destination.

## Prerequisite

As requested in [ansible vaultwarden module](https://docs.ansible.com/ansible/latest/collections/community/general/bitwarden_lookup.html#id2)

- bw (command line utility)
- be logged into bitwarden
- bitwarden vault unlocked
- BW_SESSION environment variable set

## Usage

### Use role

- Add the role git source in "requirements.yml" file :
```
  - name: role_name
    scm: git
    src: git@github.com:tiny-company/<repository_name>.git
    version: main
```

- And then use the galaxy command to load the file dependencies :
```
ansible-galaxy install -r requirements.yml
```

- Or manually get the playbook as collection (with ansible-galaxy) :
```
ansible-galaxy collection install git@github.com:tiny-company/<repository_name>.git
```

### Variables

For an exhaustive list of variables check the [defaults](defaults/main.yml)
file. Ideally, all values will have commentaries describing what are their
purposes and by the default value you can tell the type.

## Source :

- [community.general.bitwarden lookup – Retrieve secrets from Bitwarden](https://docs.ansible.com/ansible/latest/collections/community/general/bitwarden_lookup.html#id2)
- [Using Ansible to read passwords from Vaultwarden Blog article](https://mteixeira.wordpress.com/2024/04/04/ansible-vaultwarden/)