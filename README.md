#  Ansible Baseline Infrastructure

Automated baseline configuration and server hardening playbooks. This repository provides reusable Ansible roles and playbooks to provision, configure, and secure infrastructure environments consistently.

---

## 📂 Project Structure

```text
ansible-baseline-infra/
├── playbooks/
│   ├── site.yml          # Main orchestration playbook
│   └── hardening.yml     # Security baseline playbook
├── roles/
│   ├── common/           # Essential packages and user setup
│   ├── security/         # Firewall, SSH hardening, and updates
│   └── monitoring/       # Baseline monitoring agents
├── inventory/
│   ├── hosts.ini         # Target inventory groups
│   └── group_vars/       # Group-specific variables
├── ansible.cfg           # Global Ansible configuration
└── README.md

Prerequisites
Ensure you have the following installed on your control node:

Ansible (2.10+)

Python 3.x

SSHpass (if authenticating via password, though SSH keys are recommended)
git clone [https://github.com/AndileKwaziMsomi/ansible-baseline-infra.git](https://github.com/AndileKwaziMsomi/ansible-baseline-infra.git)
cd ansible-baseline-infra

ansible-playbook -i inventory/hosts.ini playbooks/site.yml
Test connectivity (Ping):
ansible all -i inventory/hosts.ini -m ping

Baseline Configurations Included
SSH Hardening: Disables root login and password authentication (enforces key-based auth).

Firewall Management: Configures default firewall rules (e.g., UFW/Firewalld).

Package Management: Ensures essential system utilities and security updates are applied.

User Management: Provisions standardized system users and administrative boundaries.
<FollowUp label="Want me to customize any specific roles, variables, or playbook tasks for this README?" query="Yes, customize the README to include specific roles or variables for my ansible-baseline-infra project."/>
