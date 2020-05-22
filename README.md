# Ansible based backup of Mikrotik routers

Ansible based backup of Mikrotik routers

## Installation

Clone this repo

```
git clone git@github.com:yurnov/ansible-mikrotik-backup.git
cd ansible-mikrotik-backup
```
Copy inventory file

```
mv inventory.example inventory
```

Edit `inventory` and fill your data

## Prerequisites

Python2.7 or Python3.6+, Ansible (tested on Ansible 2.9.9, shold work fine with Ansible 2.4+). SSH should be enabled in your Mikrotik and passwordless authentification should be configured.

## Usage

```
ansible-playbook -i inventory playbook/backup.yml
```

You can owerride default backup storage using extravars:

```
ansible-playbook -i inventory -e "backupdir=/backup/folder username=admin" playbook/backup.yml
```


## Contributing
Pull requests are welcome. 

## License
[MIT](https://choosealicense.com/licenses/mit/)