# Ansible Mikrotik Backup

Ansible Mikrotik Backup is a simple [Ansible](https://docs.ansible.com/ansible/latest/index.html) playbook to create backups from your RouterOS device.

## Prerequisites and Installation

Use the package manager pip to install Ansible

```bash
pip install ansible==2.9.27
```

or follow [installation guide for your platform](https://docs.ansible.com/ansible/2.9/installation_guide/index.html) to obtain ansible. 

Tested with Ansible versions 2.8.x and 2.9.x but should work with other versions as well.

Simply clone this repo for usage

```bash
git clone git@github.com:yurnov/ansible-mikrotik-backup.git
```

## Usage

Copy `inventory.example` into `inventory` and than edit `inventory` to have your actual data. Multiple RouterOS device is supported, please add a separate line for each of them.

In this stage ssh password-less authentication requried.

Run playbook with 

```bash
ansible-playbook main.yml -i inventory
```

Gererated config files will be stored in `output` folder

## TODO

Implement support of both, password authentication and password-less authentication with `sshpass` (need to be installed locally).

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License
[MIT](https://choosealicense.com/licenses/mit/)