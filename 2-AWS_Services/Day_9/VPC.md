_**Day 9 - 24.08.2024 Saturday**_

<br>

- [VPC (Virtual Private Cloud)](#VPC-Virtual-Private-Cloud)
  
- [Create VPC](#Create-VPC)

- [Crete Internet Gateway](#Crete-Internet-Gateway)

- [Create Subnet](#Create-Subnet)

- [Create Route table](#Create-Route-table)

- [Subnet Auto Assign IP](#Subnet-Auto-Assign-IP)

- [Create EC2 instance](#Create-EC2-instance)

- [Ping google](#Ping-google)

- [Firewall inbound rule](#Firewall-inbound-rule)

- [Display IP web page](#Display-IP-web-page)

- [Delete VPC](#Delete-VPC)

<br>

## VPC (Virtual Private Cloud)

<br>

Network Infrastructure; Internet Gateway, Subnets and Route Table

![image](https://github.com/user-attachments/assets/df07ee1d-b114-494d-b190-33c07c292df1)

![image](https://github.com/user-attachments/assets/8b8535e6-2b99-4f2c-8efe-eb874c33f2d3)

<br>

## Create VPC

![image](https://github.com/user-attachments/assets/6732077f-7cc1-4e52-8c6f-2c47e9538a9b)

![image](https://github.com/user-attachments/assets/393a9800-c496-4627-8c38-c120ef85949a)

<br>

demo2-vpc

192.168.0.0/16

![image](https://github.com/user-attachments/assets/185a928c-c59e-4f86-99cc-e5bfd3bf3c17)

![image](https://github.com/user-attachments/assets/ce2aae53-3a6a-4c58-a15f-4a8ec6d5b425)

![image](https://github.com/user-attachments/assets/4d844579-a2a2-418b-8df6-579cee4dd923)

<br>

## Crete Internet Gateway

<br>

![image](https://github.com/user-attachments/assets/7c715996-beea-476e-8e21-1c21139eb617)

<br>

demo2-igw

![image](https://github.com/user-attachments/assets/cc1cfff4-d9cb-4238-be21-bf7bb698d78a)

<br>

Attach to VPC

![image](https://github.com/user-attachments/assets/32df237e-4e77-4b0e-b535-9e65bed85a3c)

![image](https://github.com/user-attachments/assets/785d177b-2ff7-46b7-bf68-c99614871741)

<br>

## Create Subnet

<br>

![image](https://github.com/user-attachments/assets/4d1506be-62fc-4f7d-b0d4-1359320a137a)

<br>

public-demo2vpc-1a

192.168.0.0/16

192.168.10.0/24

![image](https://github.com/user-attachments/assets/4f5a0ffa-4ad5-49a8-b38d-9c851957e551)

![image](https://github.com/user-attachments/assets/917e66a4-b0a4-4213-bd38-e8b8c77f2bdb)

<br>

public-demo2vpc-1b

192.168.0.0/16

192.168.20.0/24

![image](https://github.com/user-attachments/assets/e3fbcbde-7684-4893-be45-159ea30c5201)

![image](https://github.com/user-attachments/assets/71840615-03b1-4250-a177-c9c190a1076f)

<br>

subnets created

![image](https://github.com/user-attachments/assets/dd3fedc9-ef89-4ec9-9fba-9cb6ba76e3ce)

<br>

## Create Route table

<br>

![image](https://github.com/user-attachments/assets/3df84dca-1207-4956-851d-d6f5db63904b)

<br>

demo2-route-table

![image](https://github.com/user-attachments/assets/fb612b48-b52d-4d47-b283-220179a976be)

<br>

Subnet associations → Edit subnet associations

![image](https://github.com/user-attachments/assets/5392f3cd-0687-43c3-b54a-ca0ffd273e7f)

<br>

Selected and Saved

![image](https://github.com/user-attachments/assets/d3d402f0-6165-443f-b4ef-a7929aafba06)

<br>

Explicit subnet associations

![image](https://github.com/user-attachments/assets/52328695-e534-488b-853e-3bd3ae437dd3)

<br>

add default route for internet connection

![image](https://github.com/user-attachments/assets/36130c81-d3bc-4cbf-8098-b29a69bda8f2)

![image](https://github.com/user-attachments/assets/f63773ab-33ae-4d3d-bc7c-5d0a886a442c)

![image](https://github.com/user-attachments/assets/f15765d8-8931-4a8c-83e0-0c57f907833f)

<br>

## Subnet Auto Assign IP

<br>

Edit subnet settings → Auto Assign IP settings → Enable

Set for 1a and 1b subnets

![image](https://github.com/user-attachments/assets/d9484210-7e27-4adc-a39b-ce7d82c2d8d7)

![image](https://github.com/user-attachments/assets/7af392a8-156a-4b39-9409-2e5a891eda2c)

<br>

## Create EC2 instance

<br>

EC2 Ubuntu server installation

new instance on demo2vpc → demo3vpc-ubuntu

Edit Network Settings

choose new vpc

choose new subnet

Auto assign public IP → Enable

![image](https://github.com/user-attachments/assets/ecfa0a44-cffd-42e7-b18d-e5a38ab06ac7)

<br>

Advanced Details → go to bottom and paste bash script into text area

![image](https://github.com/user-attachments/assets/320b7ad7-eef3-4e28-9e9b-8a283df7609f)

```bash

#!/bin/bash

yes | sudo apt update

yes | sudo apt install nginx

echo "<h2>Yeni VPC Server Bilgilerim</h2><p><strong>Hostname:</strong> $(hostname)</p><p><strong>IP Address:</strong> $(hostname -I | cut -d" " -f1)</p>" > /var/www/html/index.html

sudo systemctl restart nginx

```

Launch instance

![image](https://github.com/user-attachments/assets/858a916d-0ff1-4d1f-aa63-5574620f4530)

<br>

Connect to Ubuntu Server Terminal

![image](https://github.com/user-attachments/assets/97dd75ad-8834-4ec3-a50b-b0bfe0a199aa)

![image](https://github.com/user-attachments/assets/66335293-defa-47b4-8e29-66046b73b588)

<br>

## Ping google

<br>

![image](https://github.com/user-attachments/assets/87c17e19-bd3c-48a8-8e19-ba3734b01658)

<br>

## Firewall inbound rule

<br>

Select Security Group in the Security tab

![image](https://github.com/user-attachments/assets/b581faa4-4476-4256-a0c0-cfb996e775b2)

<br>

Edit inbound rules

![image](https://github.com/user-attachments/assets/e73ff256-fe33-442d-95e9-458e2aaf9736)

HTTP port 80 added

![image](https://github.com/user-attachments/assets/c821b979-e060-47ac-8f7f-d17337862a7b)

![image](https://github.com/user-attachments/assets/a0f3fb99-faff-4c1e-98b3-76c9c8f907c9)


## Display IP web page

<br>

Open IP address in the web browser 

3.92.x.x

![image](https://github.com/user-attachments/assets/e301995c-14d6-4f07-81c9-7f7d8420e07d)

<br>

## Delete VPC

<br>

Stop and Teminate (Delete) EC2 instances

Route tables → Subnet associations → Edit subnet associations

![image](https://github.com/user-attachments/assets/b578b719-9023-49e7-8504-69d5a3aa72fd)

<br>

Deselect options and save then it will go to Subnets without explicit associations

![image](https://github.com/user-attachments/assets/18e3138b-ae7c-441d-b113-636b02cd8824)

<br>

Subnets → Actions → Delete subnet

![image](https://github.com/user-attachments/assets/26780d98-498b-449c-a7ee-ed948f00ae10)

![image](https://github.com/user-attachments/assets/a87ba504-3375-4719-9af8-2be4ae0e052a)



Internet gateways → Actions → Detach from VPC

![image](https://github.com/user-attachments/assets/4e6042a7-564c-48a6-ac09-0c8c04e8bbc3)

![image](https://github.com/user-attachments/assets/42417ea1-d114-4127-8e5e-072e15113241)

<br>

Actions → Delete internet gateway

![image](https://github.com/user-attachments/assets/d8167094-d9cb-415b-9817-baa91157c795)

![image](https://github.com/user-attachments/assets/e9726f23-ea05-42a7-aa2c-c4233b8b7119)
