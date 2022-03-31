# Automation with Ansible in AWS

## Software Requirement
- `WSL2 `
- `Ansible`
- `AWS CLI`
- `Visual Studio Code (IDE)`

## Installation on Windows Machine
- Enable `Hyper-V` <br />
`Windows Settings`
    1. Right-click the Windows button on your desktop and select Apps and Features
    2. Choose `Programs and Features` located on the right.
    3. Choose `Turn Windows features` on or off.
    4. Check the box next to `Hyper-V`, including `Hyper-V Management Tools` and `Hyper-V Platform`, and click `OK`.

- Open `Powershell as an Administrator`
    - Install `Chocolatey`
        ```
        Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
        ```
    - Restart `Windows`
    - Install `WSL2`
        ```
        choco install WSL2
        ```
    - Install `WSL extension` on VScode and `Install Ubuntu distro`
        ```
        choco install wsl-ubuntu-2004
        ```
## After successful Installation

- `Open Visual Studio Code (IDE)`

- `Clone repository`
    ```
    git clone https://github.com/ukohae/aws_ansible.git
    ```
    - Go into `aws_ansible` directory 
        ```
        cd aws_ansible
        ```
    - Enable `Virtual Environemt`
        ```
        source venv/bin/activate
        ```
        - In the `Virtual Environment` perform the following:
            ```
            sudo apt update && upgrade
            ```
            ```
            sudo apt install python3 python3-pip ipython3
            ```
            ```
            pip install ansible==5.4.0
            ```
            ```
            pip install awscli
            ```

## Check if the following are installed

- `Python3`
    ```
    python3 --version
    ```

- `Ansible `
    ```
    ansible --version
    ```

## AWS Credentials
- Generate `Access Key` and `Secret Keys` from AWS [Click Here](https://us-east-1.console.aws.amazon.com/iam/home?region=us-east-2#/security_credentials)
    - In `WSL2`, do:
        ```
        aws configure
        ```
    - Parse the following: <br />
        `Access Key: `<br /> `Secret Key: `<br /> `Region: `
