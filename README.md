# ansible-ec2-auto-provisioning

Automated provisioning and configuration of EC2 instances using Ansible with AWS Systems Manager (SSM) integration.
The repository contains example playbooks, dynamic inventory helper, and basic hardening and application deployment playbooks.

## Contents
- `ansible/playbooks/` - playbooks for base hardening, nginx, and application deployment
- `ansible/inventory/aws_ec2.py` - dynamic inventory (example)
- `scripts/` - helper scripts to bootstrap SSM and instance profiles
- `docs/` - runbook and variable explanation

## Highlights
- Uses SSM for remote execution when SSH is not desirable.
- Demonstrates dynamic inventory pulled from EC2 tags.
- Provides idempotent playbooks that can be reused for Linux and Windows targets.

## Example usage
```bash
ansible-playbook -i ansible/inventory/aws_ec2.py ansible/playbooks/site.yml --extra-vars "env=staging"
```

---

Connect with me on LinkedIn: https://www.linkedin.com/in/dhairyashilclouddevops/


---

License: MIT. See LICENSE file.
