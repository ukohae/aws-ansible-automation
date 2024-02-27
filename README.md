# Ansible Automation in AWS [![Ansible Deployment](https://github.com/ukohae/aws-ansible-automation/actions/workflows/ansible.yml/badge.svg)](https://github.com/ukohae/aws-ansible-automation/actions/workflows/ansible.yml)

## Software Requirement
- `WSL2 ` [Click Here](https://docs.microsoft.com/en-us/windows/wsl/about) to learn more
- `Ansible` [Click Here](https://www.ansible.com/) to learn more
- `AWS CLI`  [Click Here](https://aws.amazon.com/cli/) to learn more
- `Visual Studio Code (IDE)`  [Click Here](https://code.visualstudio.com/) to learn more

## Clone Repository

```
git clone https://github.com/devops-terraform-aws/devsecops.git
```

## Ansible Environment Installations & Configuration - WSL Ubuntu (Optional)
- Configure virtual environment on `Ubuntu WSL`
    ```
    sudo apt update -y
    sudo apt install python3 python3-pip ipython3 -y
    sudo apt install python3.10-venv -y
    sudo ln -sf $(which python3) /usr/bin/python && sudo apt install -y && sudo apt install unzip -y
    ```

    ```
    python -m venv venv && source venv/bin/activate
    ```
- Ansible Installation
    ```
    pip install ansible-core
    pip install awscli && pip install botocore && pip install boto3
    ```
    ```
    ansible-galaxy collection install amazon.aws
    ```
    ```
    ansible-galaxy collection install community.crypto
    ```

## Verify the following installation:

- `Python3`
    ```
    python3 --version
    ```

- `Ansible `
    ```
    ansible --version
    ```

- `AWS CLI`
    ```
    aws --version
    ```

## AWS Credentials
- Generate `Access Key` and `Secret Keys` from AWS [Click Here](https://us-east-1.console.aws.amazon.com/iam/home?region=us-east-2#/security_credentials)
    - In `WSL2`, do:
        ```
        aws configure
        ```
    - Parse the following: <br />
        `AWS Access Key ID [None]: `<br /> `AWS Secret Access Key [None]: `<br /> `Default region name [None]: ` <br /> `Default output format [None]: `


### Test a Playbook! 
-   On the `Command Line`, run :
    ```
    ansible-playbook virtual_machine_info.yml
    ```
