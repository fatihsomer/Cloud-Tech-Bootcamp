_**Day 6 - 17.08.2024 Saturday**_


- [Download and Install CLI tool](#Download-and-Install-CLI-tool)

- [Create access key for CLI](#Create-access-key-for-CLI)

- [Configure CLI](#Configure-CLI)

- [Install Ubuntu server using CLI](#Install-Ubuntu-server-using-CLI)

- [Connect with SSH](#Connect-with-SSH)

- [Other CLI Commands](#Other-CLI-Commands)

- [Disable User Access Key](#Disable-User-Access-Key)

- [Delete User Access Key](#Delete-User-Access-Key)

<br>

## Download and Install CLI tool

<br>

[https://aws.amazon.com/tr/cli/](https://aws.amazon.com/cli/)

![image](https://github.com/user-attachments/assets/4d6c3a2b-e6b9-4ac9-9265-0d6d707eb08d)

<br>

## Create access key for CLI

<br>

![image](https://github.com/user-attachments/assets/54b44643-39fa-4eab-a4f4-3aeab800b233)

<br>

CLI and Confirmation

![image](https://github.com/user-attachments/assets/26ae94c3-89eb-48b4-abc0-a9b3a543fc59)

<br>

bootcampkey

![image](https://github.com/user-attachments/assets/0c7a67e9-ef91-4909-9da5-2faa256b19a8)

![image](https://github.com/user-attachments/assets/b3ff330a-3c7a-4363-a79b-ae545eb3238d)

<br>

## Configure CLI

<br>

Copy Region Information (**eu-central-1** - will be used as **region**)

![image](https://github.com/user-attachments/assets/63cb5ccc-7a0c-4570-9c1e-1125131f63f4)

<br>

Windows + R (run) -> cmd (command prompt) -> aws configure

![image](https://github.com/user-attachments/assets/278a4291-41da-4ea3-bef1-78c09c6a99f6)

<br>

## Install Ubuntu server using CLI

<br>

EC2 -> Launch Instance -> select Ubuntu -> copy AMI ID (**ami-0e872aee57663ae2d** - will be used as **image-id**)

![image](https://github.com/user-attachments/assets/4fabe313-cd62-4412-9d50-c8a99c20b0c9)

<br>

Go down and click Create new key pair (**bootcampkey** - will be used as **key-name**)

![image](https://github.com/user-attachments/assets/ba0374af-47f4-4166-9c09-baede78149ca)

![image](https://github.com/user-attachments/assets/e912db05-02b0-4c6e-a963-58cfa4bfe40c)

<br>

EC2 -> Security Groups -> copy default Security group ID (**sg-0b4...** - will be used as **security-group-ids**)

![image](https://github.com/user-attachments/assets/025a147b-6c5c-40e1-82ae-cf252702c825)

<br>

run the below command in cmd and then it will create a new ubuntu server

aws ec2 run-instances --image-id **ami-0e872aee57663ae2d** --count 1 --instance-type t2.micro --key-name **bootcampkey** --security-group-ids **sg-0b4...** --region **eu-central-1**

![image](https://github.com/user-attachments/assets/fca7b929-ee92-46e0-a0ce-0efeebee4fc4)

<br>

The newly created ubuntu server can be seen in EC2 -> Instances section

![image](https://github.com/user-attachments/assets/621e0d60-4144-44dc-98f6-2926a511d6cb)

<br>

## Connect with SSH

<br>

EC2 -> Instance -> Security tab and check SSH port is available for Inbound rules

![image](https://github.com/user-attachments/assets/819564bd-eaee-43cf-999d-8d7525de354d)

<br>

Connect via SSH using Bitvise app

![image](https://github.com/user-attachments/assets/6fd433b9-78cc-4753-a714-0db5a25e5c80)

<br>

Open terminal

![image](https://github.com/user-attachments/assets/737041d6-24e0-4421-8991-34253222cee4)

<br>

## Other CLI Commands

<br>

aws iam list-users

![image](https://github.com/user-attachments/assets/4fbd9122-1bc9-46d7-88d0-4c7cca6dcd98)

<br>

aws c2 describe-instances --region eu-central-1

![image](https://github.com/user-attachments/assets/d3d3d06e-99a6-4b55-bfbb-df51e707c040)

<br>

aws ec2 stop-instances --instance-ids i-0b... --region us-east-1

![image](https://github.com/user-attachments/assets/5c7924e6-62f7-45f4-9bb6-f5b4f1c34964)

![image](https://github.com/user-attachments/assets/7561874c-a6c4-44d0-84fe-797bb8fdcff0)

<br>

aws ec2 terminate-instances --instance-ids i-0b... --region us-east-1

![image](https://github.com/user-attachments/assets/838f8726-5321-47a2-a8ee-acfe542ba2c1)

<br>

## Disable User Access Key

<br>

IAM → Users → Security Credentials → Access keys → Actions → Deactivate

![image](https://github.com/user-attachments/assets/dbee9de1-6575-4bb0-a459-b48159779576)

![image](https://github.com/user-attachments/assets/dd16476f-c828-4924-8926-d99eecc6e8b3)

<br>

## Delete User Access Key

<br>

Disable then Delete

IAM → Users → Security Credentials → Access keys → Actions → Delete

![image](https://github.com/user-attachments/assets/b7538985-3288-44f3-9a05-5a8e8fe487c0)

![image](https://github.com/user-attachments/assets/e5c8404b-6b71-4e46-945c-ff5a6a9afb49)

![image](https://github.com/user-attachments/assets/cfc23529-58d0-48df-b442-23ebe7727edd)

![image](https://github.com/user-attachments/assets/42fdcfa0-02d4-4bea-b969-e3303991baae)
