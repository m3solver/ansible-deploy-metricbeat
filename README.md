# ansible-deploy-metricbeat
Ansible role to install metricbeat for docker or system metric collection

# Installation

```bash
cd /etc/ansible/roles
git clone https://github.com/zwindler/ansible-deploy-metricbeat
```

# Usage

For quick usage, you can just copy the sample playbook

```bash
cd /etc/ansible
cat roles/ansible-deploy-metricbeat/sample-playbook.yml
---
- name: Install metricbeat for system
  hosts: localhost
  vars:
    - elk_server: localhost
    - deploy_dashboard: false
    - activate_system_module: true
    - activate_docker_module: true
  roles:
    - { role: ansible-deploy-metricbeat }
```
