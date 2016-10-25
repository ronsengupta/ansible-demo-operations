# Ansible Tower Demo Ops Resources
> Automation for the shared Ansible Tower demo server.

## Overview
This repo contains an Ansible project used to create and maintain a shared Ansible Tower demo environment. The idea is to handle automation of the following use

## Requirements
This project targets AWS for all demo resources. The following environment variables must be present in order to run any of the bootstrap playbooks:
- `ANSIBLE_AWS_ACCESS_KEY_ID`: The AWS_ACCESS_KEY_ID for the demo AWS account
- `ANSIBLE_AWS_SECRET_ACCESS_KEY`: The AWS_SECRET_ACCESS_KEY for the target AWS account
- `ANSIBLE_AWS_REGION`: The AWS_REGION for the target AWS account
- `TOWER_DEMO_KEYPAIR_NAME`: Name of the AWS keypair used to create the Tower server

It is also necessary to have the following resources:
  - shared Ansible Vault passphrase
  - AWS keypair to use when creating Tower

These values can be set in group_vars.

## Usage
`ansible-playbook tower.yml --ask-vault-pass`
