_**Day 10 - 27.08.2024 Tuesday**_

<br>

- [WordPress installation](#WordPress-installation)

- [Web installation](#Web-installation)

- [Web site config](#Web-site-config)

- [Register Domain](#Register-Domain)

- [DNS query](#DNS-query)

- [Register website with Free Domain](#Register-website-with-Free-Domain)

- [Register website with Cloudflare](#Register-website-with-Cloudflare)

- [Open website](#Open-website)

<br>

## WordPress installation

<br>

Check for Wordpress full installation steps

https://github.com/fatihsomer/Cloud_Tech_Bootcamp/blob/main/2-AWS_Services/Day_9/Wordpress.md

<br>

## Web installation

<br>

http://18.199.x.x/

![image](https://github.com/user-attachments/assets/65b64e56-6f9a-49bc-b613-5771ab69d0dd)

![image](https://github.com/user-attachments/assets/9c8f6541-a22e-4a64-8482-b2ec0589d98a)

![image](https://github.com/user-attachments/assets/237d9a77-cc33-4586-9bc2-1c55025a89ef)

![image](https://github.com/user-attachments/assets/ef8bd544-915a-4fb0-8f31-27b792557870)

![image](https://github.com/user-attachments/assets/0434a031-fe8a-4903-931b-f665a237f239)

![image](https://github.com/user-attachments/assets/c7a4f557-ce58-4324-9d2f-8dc980f6c9a0)

![image](https://github.com/user-attachments/assets/5f900171-42c4-4682-a3b0-2b64171c6f37)


## Web site config

<br>

Create new folder

cd /var/www/htmlxyz/

sudo mkdir ibb2024

ll

![image](https://github.com/user-attachments/assets/05303fc0-d81a-438d-9726-796eeee5fb25)

<br>

Download Bootstrap template

sudo wget https://bootstrapmade.com/content/templatefiles/Bootslander/Bootslander.zip

![image](https://github.com/user-attachments/assets/32b21f82-2c39-4709-a71e-bfc13c1e920f)

<br>

Install unzip tool and Extract zip file

sudo apt install unzip

sudo unzip Bootslander.zip

ll

![image](https://github.com/user-attachments/assets/874a5788-a270-46e5-b9a1-5ad7819cace8)

<br>

Move files into folder

sudo mv Bootslander/* .

ll

![image](https://github.com/user-attachments/assets/4680a4cd-7ee9-43de-abc1-b16cb6caebf7)

<br>

Copy config file

cp wordpress ibb1

<br>

Edit config file

sudo nano /etc/nginx/sites-available/ibb1

![image](https://github.com/user-attachments/assets/6362c336-2782-487a-9c41-9ead6d031c34)

<br>

Restart nginx service

sudo systemctl restart nginx

![image](https://github.com/user-attachments/assets/665b5938-f5e2-430f-bb7e-ea48dd1b2535)

<br>

## Register Domain

<br>

Free Domain names website

https://freedomain.one/

Free Domain name registered

ibbtechwpdemo.run.place

<br>

## DNS query

cmd → nslookup → set type=ns

ibbtechwpdemo.run.place

![image](https://github.com/user-attachments/assets/6164306e-67ff-4368-963c-89cfe1cb7a55)

<br>

ibb1.ibbtechwpdemo.run.place

![image](https://github.com/user-attachments/assets/10799228-ded8-431a-a6fa-5dc8a1e77b0d)

<br>

## Register website with Free Domain

<br>

Register ibb1 website and IP as A Record then Save changes

![image](https://github.com/user-attachments/assets/79e48f6d-22c4-4ad7-afcd-19953b4fb059)

![image](https://github.com/user-attachments/assets/22926b70-56ce-44dd-83b7-96fa4a7c4658)

<br>

## Register website with Cloudflare

<br>

Register ibb1 website and IP as A Record then Save

![image](https://github.com/user-attachments/assets/25393c64-e266-4ecf-82dc-5857cc0a3170)

![image](https://github.com/user-attachments/assets/862ccc67-9c16-4ecc-a991-a374a613f685)

<br>

## Open website

<br>

[ibb1.ibbtechwpdemo.run.place](http://ibb1.ibbtechwpdemo.run.place/)

![image](https://github.com/user-attachments/assets/2acb5fa7-96db-40b1-a911-702bc82a83e5)

