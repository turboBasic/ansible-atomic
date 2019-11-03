# Ansible Atomic recipes


### Ansible commands for debugging
```sh
# Prints facts about hosts
ansible all --module-name setup

# Prints all variables assigned to host
ansible all --module-name debug --args 'var=hostvars[inventory_hostname]'
```

### Encrypt variable inline
```sh
ansible-vault encrypt_string 'variable value' --name 'variable_name'
```

### Encrypt file with variables
```sh
ansible-vault encrypt filename
ansible-vault view filename
```

### Alternative: `hosts` file in .ini format

```ini
[factory]
server1         ansible_user=bob ansible_connection=ssh ansible_private_key_file=~/.ssh/id_rsa
server2
server3
```
