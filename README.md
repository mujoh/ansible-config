# Sample Ansible configuration

This is sample ansible configuration for running Docker image on any host.

## Folder structure:

```
project
│   README.md
│   playbook-sample.yml 
│   hosts
│   ansible.cfg
│
└───roles
│   │ 
│   │
│   │
│   └───sample
│       │
│       └───tasks
|               main.yml
```

* `playbook-sample.yml` is main ansible playbook file in which you define which role to execute as well as deploy target. Deploy target is taken from `DEPLOY_TARGET` env variable.

* `hosts` is file which consists of host ip addresses or DNS names

* `ansible.cfg` is file where we define roles path and inventory

## Environment variables
* DEPLOY_TARGET - defines which host is going to be used (dev, prod etc...)
* CI_REGISTRY - registry url if we are pulling image from registry
* CI_REGISTRY_USER - registry user
* CI_REGISTRY_PASSWORD - registry password

## Running app
* You can run sample ansible playbook by using:
`ansible-playbook playbook-sample.yml`