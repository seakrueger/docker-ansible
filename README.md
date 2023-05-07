# Install the Docker Engine on Ubuntu via Ansible

## System requirements

[x] Ubuntu 18.04+
[x] Ansible 2.4.0+
[x] passwordless SSH access

## Usage

Edit `inventory/servers/hosts.ini` to match your system's information. For example:

```bash
[servers]
192.16.35.12
192.16.35.13
192.16.35.14

[servers:vars]
ansible_user=Ubuntu
systemd_dir=/etc/systemd/system
```

If needed, you can also edit `[servers:vars]` to match your environment.

Start the installation using the following command:

```bash
ansible-playbook site.yml -i inventory/servers/hosts.ini
```

