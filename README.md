# Ansible Role for SSHD Hardening
**Author/Maintainer:** Josh Murphy

## Overview

This Ansible role hardens the SSHD Config by doing the below:
```yaml
- Disables Root SSH Login
- Disables Empty Password Login
- Disables Password Authentication
- Enables Pubkey Authentication
- Disables X11Forwarding
- Sets a 5 Minute Inactivity Timeout on SSH Sessions
- Sets SSH Allowed Users
```

## Supported Platforms and Derivatives
The files changed should exist on every Redhat and Debian Distro. Below are the explicitly supported Distros.
```yaml
# RedHat
EL - All Versions
Fedora - All Versions
Rocky - All Versions
AlmaLinux - All Versions

# Debian
Debian - All Versions
Ubuntu - All Versions
```

## Example Playbook

```yaml
- hosts: all
  become: yes

  roles:
    - role: system_ssh_hardening
```

### From Ansible Galaxy

```bash
ansible-galaxy install crowjm64.system_ssh_hardening
```

This role was created and is maintained by **[CrowJM64](https://github.com/CrowJM64)**.