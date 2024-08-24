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

## Disable User Access Key

<br>

## Delete User Access Key

<br>

