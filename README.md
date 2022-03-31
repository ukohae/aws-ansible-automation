# Ansible Automation in AWS

## Software Requirement
- `WSL2 ` [Click Here](https://docs.microsoft.com/en-us/windows/wsl/about) to learn more
- `Ansible` [Click Here](https://www.ansible.com/) to learn more
- `AWS CLI`  [Click Here](https://aws.amazon.com/cli/) to learn more
- `Visual Studio Code (IDE)`  [Click Here](https://code.visualstudio.com/) to learn more

### Installation on Windows Machine
- Enable `Hyper-V` <br />
`Windows Settings`
    1. Right-click the Windows button on your desktop and select Apps and Features
    2. Choose `Programs and Features` located on the right.
    3. Choose `Turn Windows features` on or off.
    4. Check the box next to `Hyper-V`, including `Hyper-V Management Tools` and `Hyper-V Platform`, and click `OK`.

- Restart `Windows Computer`

- Open `Powershell as an Administrator`
    - Install `Chocolatey`
        ```
        Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
        ```
    - Install `WSL2`
        ```
        choco install WSL2
        ```
    - Install `WSL extension` on VScode and `Install Ubuntu distro`
        ```
        choco install wsl-ubuntu-2004
        ```
    - Install `Visual Studio Code`
        ```
        choco install vscode
        ```
### After successful Installation

- `Open Visual Studio Code (IDE)`, click on `Terminal`,  `New Terminal` and `Clone repository`
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
