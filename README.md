# Zabbix server

## Prepare environment

### System requirements

1. Vagrant
2. Virtualbox
3. Ansible

## Using

### Launch

1. Launch server
  ```
  vagrant up
  ```

2. Open http://localhost:8999/ in browser. Default user is `Admin` with password `zabbix`

### Apply changes

Run ansible playbooks while VM is running:
```
vagrant provision
```
