# Export Hostname and date to an output file
Run as service in linux and windows with user "test", export to ./output. Using ansible to deploy.

Author: Tony Cao

Version: 1.0.0

Date: 2020-03-12

## Installation
Setup ansible for linux and windows as usual.
Create "test" user on linux and windows box.


Copy these files to ansible control node.
```powershell
ansible-playbook-linux.yaml
ansible-playbook-windows.yaml
inventory.ini

```
Copy these files to nfs location for linux servers.
```powershell
test.sh
testservice.service
```
Convert Power shell script to binary
```powershell
Use PS2EXE-GUI attached to convert test.ps1 into test.exe
```

Copy these files to cifs location for windows servers.
```powershell
test.exe
test-retry.exe  #if you want see failure with 3 retries.
```

## Deploy by Ansible
For Linux
```powershell
ansible-playbook -i inventory.ini ansible-playbook-linux.yaml
```
For Windows
```powershell
ansible-playbook -i inventory.ini --ask-vault-pass ansible-playbook-windows.yaml
```
