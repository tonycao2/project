# Export Hostname and date to an output file
Run as service in linux and windows with user "test", export to ./output. Using ansible to deploy.

Author: Tony Cao

Version: 1.0.0

Date: 2020-03-12

## Installation
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
run PS2EXE-GUI to convert test.ps1 to test.exe
```

Copy these files to cifs location for windows servers.
```powershell
test.exe
```

## Usage
For Linux
```powershell
ansible-playbook -i inventory.ini ansible-playbook-linux.yaml
```
For Windows
```powershell
ansible-playbook -i inventory.ini ansible-playbook-windows.yaml
```
