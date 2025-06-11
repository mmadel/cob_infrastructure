# Ansible DB Provisioning Project

This project provisions and secures MySQL and PostgreSQL databases for three services: EMR, Billing, and Demo.

## Usage

### 1. Install dependencies
```bash
ansible-galaxy install -r requirements.yml
```

### 2. Encrypt vault
```bash
ansible-vault encrypt group_vars/vault.yml
```

### 3. Provision databases
```bash
ansible-playbook -i inventories/dev/hosts playbooks/provision.yml
```

### 4. Rotate passwords
```bash
ansible-playbook -i inventories/dev/hosts playbooks/rotate_passwords.yml
```
