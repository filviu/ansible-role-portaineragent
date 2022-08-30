# Portainer Agent

A role to add a Portainer Agent to the node as a Docker Service, including mounting the Docker socket and exposing port 9001. The role can be configured to specify a shared secret between agent and server, by setting a variable as follows: `portaineragent_shared_secret: mysupersecret`.

## Fork

Initially developed by Rob Stanford at Gendall Design. Initial changes that triggered the fork:

- switched from swarm to regular docker
- the ansible secret is now a variable so I can use ansible-vault


## Usage

Include this role in a playbook using a [requirements.txt](https://galaxy.ansible.com/docs/using/installing.html#installing-multiple-roles-from-a-file) file.

### Example playbook

```yaml
- hosts: manager[0]
  roles:
    - filviu.portaineragent
```

## Deployment

This role will be automatically built and deployed to [Ansible Galaxy](https://galaxy.ansible.com/filviu) on each release.
