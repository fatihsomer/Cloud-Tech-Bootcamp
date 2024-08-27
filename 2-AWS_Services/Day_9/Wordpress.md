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

![image](https://github.com/user-attachments/assets/1daf16b4-a03f-4620-bd63-d6dbacc0c199)

<br>

folder owner updated and permission gave

sudo chown -R www-data:www-data /var/www/html/

sudo chmod -R 755 /var/www/html/

![image](https://github.com/user-attachments/assets/acba7687-e510-46d3-a81d-008758840a56)

<br>

wordpress file is created using nano text editor

sudo nano /etc/nginx/sites-available/wordpress

![image](https://github.com/user-attachments/assets/fc99885f-0749-4136-a00d-bc7949682d71)

```

server {  
    listen 80;  
    server_name your_domain_or_IP; # replace this with your own domain name or IP address

    root /var/www/html/wordpress;# wordpress folder  
    index index.php index.html index.htm;  

    location / {  
        try_files $uri $uri/ /index.php?$args;  
    }  

    location ~ \.php$ {  
        include snippets/fastcgi-php.conf;  
        fastcgi_pass unix:/var/run/php/php8.3-fpm.sock; # Check PHP version
        fastcgi_param SCRIPT_FILENAME $document_root$fastcgi_script_name;  
        include fastcgi_params;  
    }  

    location ~ /\.ht {  
        deny all;  
    }  
}

```

<br>

create symbolick link 

sudo ln -s /etc/nginx/sites-available/wordpress /etc/nginx/sites-enabled/

![image](https://github.com/user-attachments/assets/519bb7b9-8b7f-470b-8cbb-d98420c1a6be)

<br>

restart nginx service

sudo systemctl restart nginx

![image](https://github.com/user-attachments/assets/5763c95a-dd80-4514-923b-d2fcb51a4f35)

<br>

## Ubuntu server firewall config

<br>

Ubuntu server security tab inbound rule http port 80 added

![image](https://github.com/user-attachments/assets/daf1d228-a369-4d5e-bfb2-7f10b213343f)

![image](https://github.com/user-attachments/assets/9b6703e9-6a5a-4a9e-a94f-b569bd1b138b)

<br>

## Wordpress web installation

<br>

Open IP address in web browser

35.159.x.x

![image](https://github.com/user-attachments/assets/4b9279bf-c3b1-4f93-a5c7-6b30980d7bb0)

