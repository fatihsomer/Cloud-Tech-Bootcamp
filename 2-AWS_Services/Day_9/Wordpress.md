_**Day 9 - 24.08.2024 Saturday**_

<br>

- [Ubuntu server installation](#Ubuntu-server-installation)

- [Ubuntu server update](#Ubuntu-server-update)

- [Nginx and PHP installation](#Nginx-and-PHP-installation)

- [Wordpress download and configure](#Wordpress-download-and-configure)

- [Database config](#Database-config)

- [Ubuntu server firewall config](#Ubuntu-server-firewall-config)

- [Wordpress web installation](#Wordpress-web-installation)

<br>

## Ubuntu server installation

<br>

EC2 Ubuntu server installation

wordpressweb-1

Free tier t2.micro

Launch instance


## Ubuntu server update

<br>

Connect to Ubuntu Server Terminal

Update ubuntu server

sudo apt update

![image](https://github.com/user-attachments/assets/669d3ce3-b5dc-40fe-b668-5b35f9f39b21)

<br>

## Nginx and PHP installation

<br>

Install nginx web server

sudo apt install nginx

![image](https://github.com/user-attachments/assets/fb82ecaa-592a-4464-8fe9-aa3ae3eff4fd)

<br>

Check nginx web server status

sudo systemctl status nginx

![image](https://github.com/user-attachments/assets/95eef8e5-6cf2-4b09-9264-100266183453)

<br>

Install PHP

sudo apt install php-fpm php-mysql php-xml php-curl php-mbstring

![image](https://github.com/user-attachments/assets/4187f650-30dc-443b-a7ea-a8bb4456cc57)

<br>

## Wordpress download and configure

<br>

Download Wordpress

wget https://wordpress.org/latest.tar.gz

<br>

Extract Wordpress

tar -xvzf latest.tar.gz

<br>

ls

![image](https://github.com/user-attachments/assets/fcadb8bd-d2d0-4249-ae8c-27cd69c7a21f)

<br>

Move wordpress folder into nginx web server

sudo mv wordpress /var/www/html/  or  sudo rsync -avP wordpress/ /var/www/html/

![image](https://github.com/user-attachments/assets/e41dceb6-864b-4440-99d7-659875402496)

<br>

Goto nginx folder and check wordpress

cd /var/www/html/

ls

![image](https://github.com/user-attachments/assets/abc77a0f-5abd-4144-bb45-9381ab555fb1)

<br>

Go into wordpress folder

cd Wordpress

ll

![image](https://github.com/user-attachments/assets/09c7dca7-f65f-4666-ba65-11bd729c747f)

<br>

php config file copied

sudo cp wp-config-sample.php wp-config.php

ls -la

![image](https://github.com/user-attachments/assets/3bce9e2d-0494-4411-a2ac-7ec0ac473f63)

<br>

php file is opened with nano editor

sudo nano wp-config.php

![image](https://github.com/user-attachments/assets/51e1effd-96f5-4376-b9dc-d0c77373fa85)

Database config is here 

![image](https://github.com/user-attachments/assets/736d5727-b243-497b-bc22-af5be7ed25aa)

<br>

## Database config

<br>




## Ubuntu server firewall config

<br>

Giving the Ubuntu server permission to connect to the database

RDS → Databases → Actions → Set up EC2 connection

![image](https://github.com/user-attachments/assets/26516a42-041a-4b38-b8b6-5d0dfc1cbed4)

![image](https://github.com/user-attachments/assets/c853f011-8218-4ad3-822e-52ef35954379)

![image](https://github.com/user-attachments/assets/1fe7d0b8-1de3-4a1b-972f-d5550b82c2e9)

<br>

View Details

![image](https://github.com/user-attachments/assets/ee10a677-203f-4dea-a2d0-842f746ba32b)

![image](https://github.com/user-attachments/assets/2c446296-e48e-4b32-a961-28676099c58f)

<br>

Database configuration

![image](https://github.com/user-attachments/assets/a8843bf6-af28-414c-ba64-6682e422a4f7)

<br>

wordpress database config done

sudo nano wp-config.php

![image](https://github.com/user-attachments/assets/be2aa4dd-fbd9-492a-a3f7-e45a571f1342)

<br>



## Wordpress web installation

<br>


