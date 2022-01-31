# Example Cloud-Init for Ansible

Example config for cloud-init to execute ansible playbook for provisioning.

## Provisioning Prep
 * Added packages - git, python3, python3-pip
 * Added user - ansible
 * Provisioned user with sudo
 * Installed ansible for user

## Provisioning
 * Clone git repo with ansible provisioning
 * Install requirements for playbook using galaxy
 * Execute playbook against localhost

## Testing

Credit: Tested with vagrant image from [@geerlingguy's Ansible for Devops](https://github.com/geerlingguy/ansible-for-devops)

### Multi-step Test Process

```
vagrant up
vagrant halt
. cloud-init-env.shl
vagrant up
```

Testing with vagrant requires multipe steps:
  * installing cloud-init on vm
  * stopping vm
  * enable vagrant's experimental cloud-init features 
  * restart vm to provision with cloud-init 
