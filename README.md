# SCOM Collection for Ansible and [Ludus](https://ludus.cloud)

This collection includes Ansible roles to install and configure SCOM. For a good example of the collection's usage, see the provided range configs. For the corresponding blog, see: https://specterops.io/blog/2025/12/09/git-scommit-putting-the-ops-in-opsmgr/

Roles included in this collection:

  - `create_scom_accounts`
  - `deploy_agents`
  - `disable_firewall`
  - `install_additional_omserver`
  - `install_db`
  - `install_omconsole`
  - `install_omreporting`
  - `install_omserver`
  - `install_omwebconsole`

## Installation in [Ludus](https://ludus.cloud)
```
ludus ansible collection add synzack.ludus_scom
ludus range config set -f <config>.yml
ludus range deploy
```

### Role Requirements

None

## Building the Collection from Source
```
git clone https://github.com/SpecterOps/ludus_scom
cd ludus_scom
ansible-galaxy collection build
python3 -m http.server 80
ludus ansible collection add http://<network ip>/synzack-ludus_scom-<version>.tar.gz
ludus range config set -f medium-distributed.yml
ludus range deploy
```

## "Network" Diagrams
<img width="2455" height="1125" alt="image" src="https://github.com/user-attachments/assets/6397a62a-c760-4327-8204-1c37e0253c25" />

**Diagrams from "Getting Started with Microsoft System Center Operations Manager" by Kevin Greene*
