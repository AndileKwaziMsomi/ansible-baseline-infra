#  Ansible Baseline Infrastructure

Automated baseline configuration and server hardening playbooks. Designed to provision, configure, and secure Linux infrastructure environments consistently across servers.

---

##  Tech Stack

- **Automation:** Ansible
- **Target OS:** Linux (Ubuntu / Debian / RHEL)
- **Configuration:** YAML, Jinja2 Templates
- **Transport:** OpenSSH

---

##  Prerequisites

Ensure you have the following installed on your control node:
- Ansible (2.10+)
- Python 3.x
- Git
- SSH key-based access to target nodes

---

##  Getting Started

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/AndileKwaziMsomi/ansible-baseline-infra.git](https://github.com/AndileKwaziMsomi/ansible-baseline-infra.git)
   cd ansible-baseline-infra
   ```

2. **Configure your inventory:**
   Add your target server IPs or hostnames to `inventory/hosts.ini`:
   ```ini
   [servers]
   your_server_ip ansible_user=your_user
   ```

3. **Test connectivity:**
   ```bash
   ansible all -i inventory/hosts.ini -m ping
   ```

4. **Run the baseline playbook:**
   ```bash
   ansible-playbook -i inventory/hosts.ini playbooks/site.yml
   ```

---

##  Project Structure

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
```

---

##  Baseline Configurations

- **SSH Hardening:** Disables root login and enforces key-based authentication.
- **Firewall Management:** Configures default inbound/outbound rules.
- **System Updates & Packages:** Installs core utilities and applies baseline security patches.
- **User Provisioning:** Sets up standardized administrative users and sudo privileges.

---

##  License

Distributed under the MIT License. See `LICENSE` for more information.
