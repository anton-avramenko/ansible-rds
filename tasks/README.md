# AWS RDS ODS

Ansible palybook to deploy RDS instance

## Getting Started

This playbook will deploy/update RDS database instance including security group, SQL parameters, user privileges etc.

### Prerequisites

Ansible host with IAM admin role.

```
#!/bin/bash
curl https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -
curl https://packages.microsoft.com/config/ubuntu/16.04/prod.list | sudo tee /etc/apt/sources.list.d/msprod.list
sudo apt-get -y update
sudo apt-get -y install ansible
sudo ACCEPT_EULA=Y apt-get -y install mssql-tools
sudo ACCEPT_EULA=Y apt-get -y install unixodbc-dev
```

## Usage
### Examples
```
ansible-playbook ODS.yml --extra-vars "env_var=dev"
```
deploy dev environment


```
ansible-playbook ODS.yml --extra-vars "env_var=dev restore_snapshot=arn:aws:rds:arn-of-shared-snap"
```
restore RDS snapshots as dev instance

### Configuration
settings.ini
grant_priv.sql
security_group.yml

## Confluence page

https://nrc-eng.atlassian.net/wiki/spaces/NRCDVO/pages/143589415/Deploy+RDS+ODS
