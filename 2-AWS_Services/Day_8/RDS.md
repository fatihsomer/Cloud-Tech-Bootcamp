_**Day 8 - 22.08.2024 Thursday**_

<br>

- [Create Database (Standart)](#Create-Database-Standart)

- [Create Database (Easy)](#Create-Database-Easy)

- [Connect to Database](#Connect-to-Database)

  - [Connect to Mysql from our Machine](#Connect-to-Mysql-from-our-Machine)

  - [Connect to Mysql from Ubuntu (EC2)](#Connect-to-Mysql-from-Ubuntu-EC2)

- [Stop and Delete](#Stop-and-Delete)

<br>

## Create Database (Standart)

<br>

RDS → Create Database → MySQL → Free Tier

![image](https://github.com/user-attachments/assets/b3250072-c006-44dd-9ec8-578d4a94761a)

![image](https://github.com/user-attachments/assets/bfe38912-b418-4cf1-b8a1-9974d44e0760)

![image](https://github.com/user-attachments/assets/f960c1cb-4dea-4c7f-859f-eba41d20b809)

<br>

Production price

![image](https://github.com/user-attachments/assets/e65e3c1a-a87a-4367-ac56-9d3b904b0eab)

![image](https://github.com/user-attachments/assets/ffd8e4dd-52da-448e-bc5a-c6995123eacb)

<br>

Dev/Test price

![image](https://github.com/user-attachments/assets/86706e1f-ff14-4733-8e62-c88a790113ff)

![image](https://github.com/user-attachments/assets/d316d6bc-31be-45fd-a914-aed18aff1499)

<br>

Free Tier price

![image](https://github.com/user-attachments/assets/b78f7636-9190-4c1f-bbe7-c9f4cd98fd4c)

![image](https://github.com/user-attachments/assets/48f4a0e1-1d10-42c9-a4bc-bcd575af075d)

<br>

DB name, username, password

![image](https://github.com/user-attachments/assets/87d163ad-75bb-4ddb-9bd1-5d83eb80082d)

<br>

t3.micro

![image](https://github.com/user-attachments/assets/538eb928-92d0-4a44-87fc-ea0fe4d1ee62)

<br>

Storage

![image](https://github.com/user-attachments/assets/cf2ea6a7-b5de-40ac-b63b-38db3f8f1155)

Connectivity

![image](https://github.com/user-attachments/assets/66641246-79b2-49ba-8b35-29b59abf872e)

![image](https://github.com/user-attachments/assets/dd2f7b0e-8551-4eb2-906a-560af8c1662f)

![image](https://github.com/user-attachments/assets/37af925e-239f-4a23-8c2c-bb96434d9635)

<br>

DB Config

![image](https://github.com/user-attachments/assets/a8027fe8-98c8-4369-a66e-0bc8ea2a5be0)

<br>

Logs settings enabled

![image](https://github.com/user-attachments/assets/71e3d9be-a994-456b-aa7f-eee6141025d1)

![image](https://github.com/user-attachments/assets/768dd4d3-2ef6-4b47-b0ef-3c354c0ab2d1)

![image](https://github.com/user-attachments/assets/fe6b9dc5-ba27-4b0f-8722-56c7a302afb7)

<br>

Click View connection details and save connection infomation

![image](https://github.com/user-attachments/assets/952dc525-34cf-464c-be24-fde2fab55a09)

Master username : admin2

Master password : ...

Endpoint : database-1.**hostname**.eu-central-1.rds.amazonaws.com

<br>

When DB Type Production is Selected then AZ (Availability Zone) can also be selected.

Even if there is a problem in the location where our database is located, it can continue to work in another location.

![image](https://github.com/user-attachments/assets/657899ad-5dc2-4e67-b351-2b4e31fbc3fc)

<br>


## Create Database (Easy)

<br>

![image](https://github.com/user-attachments/assets/06271072-9772-43b8-8e4a-f8e04eb18a61)

![image](https://github.com/user-attachments/assets/b46ef7a7-c2c7-448e-a58c-e8996d2cec2c)

![image](https://github.com/user-attachments/assets/7c5741c6-35ad-4ae4-93e5-866602095657)

<br>

## Connect to Database

<br>

- ### Connect to Mysql from our Machine

<br>

To connect to MySQL you need to download and install MySQL Workbench (Free)

https://dev.mysql.com/downloads/workbench/

![image](https://github.com/user-attachments/assets/abe87ee2-82d1-4ee7-b450-9d3ddc4f55fe)

<br>

Modify database settings

![image](https://github.com/user-attachments/assets/88b84406-502d-49d8-875f-29afcc71d27e)

<br>

Public Access authorization granted

![image](https://github.com/user-attachments/assets/60362592-6c38-47b2-a5fc-89ac6a39427d)

<br>

Apply immediately

![image](https://github.com/user-attachments/assets/61f6962d-3776-43d9-8c52-53f10311c447)

<br>

EC2 → Security Group → Default security group authorized for mysql port (3306) for 0.0.0.0/0

![image](https://github.com/user-attachments/assets/ee616790-824d-4176-ad95-f7e9c290caf7)

<br>

MySQL Workbench

![image](https://github.com/user-attachments/assets/bd967ccb-aeef-46e1-80de-db6dcc43092d)

<br>

Test Connection is successful

![image](https://github.com/user-attachments/assets/a128e00e-ed28-4280-ad0c-cf5ccda300f6)

<br>

Connected to MySQL

![image](https://github.com/user-attachments/assets/a1d77151-5398-43f0-a776-8f3b5d76bc35)

<br>

- ### Connect to Mysql from Ubuntu (EC2)

<br>

Actions → Set up EC2 connection

![image](https://github.com/user-attachments/assets/44f7cbd4-2c99-42c2-af68-b4a5f4b93f52)

![image](https://github.com/user-attachments/assets/0e07ddc1-aaf5-440c-a5ff-a4088156f73b)

![image](https://github.com/user-attachments/assets/1b7c0f9f-1abe-484c-96c6-c8796fcb6d80)

![image](https://github.com/user-attachments/assets/14a0cfa2-ed2a-478e-806c-6179a94e4db0)

<br>

Connect to Ubuntu terminal via ssh

sudo apt install mysql-client-core-8.0

![image](https://github.com/user-attachments/assets/5482d096-886b-4fac-aab5-8527721680e9)

![image](https://github.com/user-attachments/assets/a93a3ac7-1531-45fc-9f6b-e54d6f2d2e07)

<br>

Connected to MySQL

mysql -h database-1.**hotname**.eu-central-1.rds.amazonaws.com -u admin2 -p

List databases

show databases;

![image](https://github.com/user-attachments/assets/7aeb8710-1f22-4744-9e91-99e8cf9fc85d)

<br>

## Stop and Delete

<br>

First, stop the database and wait 2-3 days, if there is no problem then it can be deleted

![image](https://github.com/user-attachments/assets/5a6a36d3-3aeb-48a2-9632-030674fb57d2)

Optionally can first take a db snapshot and then stop it

![image](https://github.com/user-attachments/assets/d1b77a40-7a03-4d2c-bcd5-f45457a309bf)

![image](https://github.com/user-attachments/assets/71d4ecd0-9d6b-4f16-8d1a-61972eea18b2)

Delete database

![image](https://github.com/user-attachments/assets/34b3e693-12d9-4d2e-8a2d-f07045884f49)

![image](https://github.com/user-attachments/assets/f31fce46-f2bb-49e8-92a1-83cd622549ae)

