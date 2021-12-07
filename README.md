# homelab-v2

Simple homelab for local testing.

Components:
- concourse WIP
- prometheus/grafana WIP

## pre-flight

Make sure the VMs are provisioned (Ubuntu 20.04) and on each VM the user is present and in the sudoersfile, and the SSH key in place.

## bootstrap

```
cd automation
ansible-playbook bootstrap.yaml
```

The bootstrap will create the user `provisioner` and make sure it can execute tasks on each VM. It will also install packages and perform upgrades in the `common` role.

It is possible to assign roles in `bootstrap.yaml`, for example to create a `concourse` node, a `prometheus` node, etc.


