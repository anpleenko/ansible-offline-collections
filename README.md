# Ansible Offline Collections

## Installation

```bash
wget https://github.com/anpleenko/ansible-offline-collections/releases/latest/download/offline-collections.tar.gz
tar -xvzf offline-collections.tar.gz
cd offline-collections
ansible-galaxy collection install -r requirements.yml
```

## community.general
**Collection:** `community.general`

The most comprehensive collection containing numerous modules, plugins, and roles that are not included in the official Red Hat collections. Includes support for various systems and services: monitoring (Monit, Nagios), databases (PostgreSQL, MySQL, Redis), cloud providers (DigitalOcean, Linode), configuration management systems, and many other tools.

**Main capabilities:**
- Modules for working with package managers (apk, emerge, slackpkg, etc.)
- User and group management across different operating systems
- Filesystem and partition management (LVM, ZFS)
- API integration with various services (Jenkins, GitLab, Jira)

## ansible.posix
**Collection:** `ansible.posix`

Official collection for POSIX-compliant systems. Contains modules and plugins specific to UNIX-like operating systems (Linux, BSD, macOS).

**Main capabilities:**
- `mount` - manage mount points
- `sysctl` - configure kernel parameters
- `firewalld` - manage firewall settings
- `seboolean`, `sefcontext`, `semanage` - SELinux management
- `authorized_key` - manage user SSH keys

## community.proxmox
**Collection:** `community.proxmox`

Collection for managing the Proxmox VE (PVE) virtualization environment. Provides modules for automating all aspects of Proxmox operations.

**Main capabilities:**
- `proxmox` - manage virtual machines (QEMU/LXC)
- `proxmox_kvm` - KVM virtualization-specific modules
- `proxmox_lxc` - manage LXC containers
- `proxmox_snapshot` - create and manage state snapshots
- `proxmox_template` - work with VM templates
- Manage Proxmox storage, networks, and users

## community.docker
**Collection:** `community.docker`

Collection for managing Docker containers and Docker Swarm. A full-featured alternative to the official Docker SDK with extended capabilities.

**Main capabilities:**
- `docker_container` - create, start, stop, and remove containers
- `docker_image` - work with images (build, push/pull)
- `docker_compose` - manage Docker Compose projects
- `docker_network` - create and manage networks
- `docker_volume` - manage data volumes
- `docker_swarm` - initialize and manage Swarm clusters
- `docker_stack` - deploy stacks in Swarm
