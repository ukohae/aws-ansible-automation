# Ansible with AWS

## Environment Requirement
- WSL2 
- Ansible
- AWS CLI
- Visual Studio Code (IDE)

## Installation on Windows Machine
- Enable Hyper-V 
- Install Chocolatey by running the command below as an Administrator in Powershell
```
$Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```
- Install WSL2 via Chocolatey
```
$ choco install WSL2
```

## Create virtual Environment
```
$ source venv/bin/activate
```
```
$ sudo apt update && upgrade
```
```
$ sudo apt install python3 python3-pip ipython3
```
```
$ pip install ansible==5.4.0
```