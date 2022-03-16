# Ansible with AWS

## Environment Requirement
- `WSL2 `
- `Ansible`
- `AWS CLI`
- `Visual Studio Code (IDE)`

## Installation on Windows Machine
- Enable `Hyper-V`
- Install `Chocolatey` by running the command below as an Administrator in Powershell
```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```
- Install `WSL2` via Chocolatey by running `Powersehll` as an `Administrator`
```
choco install WSL2
```
## After successful Installation

- Open Visual Studio Code (IDE)

- Clone repository
    ```
    git clone https://github.com/ukohae/aws_ansible.git
    ```
- Go into `aws_ansible` directory 
    ```
    cd aws_ansible
    ```
- Enable `virtual environemt`
    ```
    source venv/bin/activate
    ```
## Install the following in the virtual Environment
```
sudo apt update && upgrade
```
```
sudo apt install python3 python3-pip ipython3
```
```
pip install ansible==5.4.0
```

## Check if the following are installed

- Python3
    ```
    python3 --version
    ```

- Ansible 
    ```
    ansible --version
    ```