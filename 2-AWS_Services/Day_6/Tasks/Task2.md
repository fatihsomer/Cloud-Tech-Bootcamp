_**Task #2 - 18.08.2024 Sunday**_

You are now connected to the ubuntu server via **ssh**

✅ Let's be super user first

sudo su

![0_super_user](https://github.com/user-attachments/assets/95c89662-8d9b-4366-aac4-a74995836582)


✅ To add a Linux user, type the following adduser command and press enter, type your new password twice then press enter for others

✅ create below users consisting of family members

sudo adduser nuran

![1a_add_user_nuran](https://github.com/user-attachments/assets/3dbe9721-4d5c-440c-90cf-9b625aefcc47)

sudo adduser bilge

![1b_add_user_bilge](https://github.com/user-attachments/assets/c1dc44c8-408b-470f-8189-bcfb4da6dc26)

sudo adduser bengisu

![1c_add_user_bengisu](https://github.com/user-attachments/assets/ed35a918-ad66-4ad6-8af7-6dcd0b77e85f)

sudo adduser lena

![1d_add_user_lena](https://github.com/user-attachments/assets/7c2a35c1-7e21-4588-9b3a-87eb77436e96)

sudo adduser miya

![1e_add_user_miya](https://github.com/user-attachments/assets/9d807e0c-8849-4381-8d8f-72259c8f2a4a)


✅ Let's create 2 groups named ailemgrup and kedilerimgrup

sudo addgroup ailemgrup

sudo addgroup kedilerimgrup

![2_add_group](https://github.com/user-attachments/assets/a7a5cbee-2d1f-44e0-ab51-15faf3afcb07)


✅ Let's add nuran, bilge and bengisu users to ailemgrup

sudo usermod -aG ailemgrup nuran

sudo usermod -aG ailemgrup bilge

sudo usermod -aG ailemgrup bengisu

![3a_user_group](https://github.com/user-attachments/assets/8dbae4a5-54ed-44fc-877a-6743c0e7030d)


✅ Let's add lena and miya users to the kedilerimgrup

sudo usermod -aG kedilerimgrup lena

sudo usermod -aG kedilerimgrup miya

![3b_user_group](https://github.com/user-attachments/assets/1f4e5ea4-8888-4291-8d05-3080665375a8)


✅ Let's give root permission to lena user from kedilerimgrup

sudo usermod -aG sudo lena

![4a_user_root](https://github.com/user-attachments/assets/23f486d5-ca54-417c-8e09-f4e7fa8f7548)


✅ Let's give root permission to bilge user from ailemgrup

sudo usermod -aG sudo bilge

![4b_user_root](https://github.com/user-attachments/assets/f92d6a9f-805a-454e-aa36-8aef3c5f7fcd)


✅ List users
 
cat /etc/passwd | tail -n -5

![image](https://github.com/user-attachments/assets/c62e482b-bc39-49a9-9f78-4ad48a8ed1a9)

✅ List groups and users

cat /etc/group | tail -2

![image](https://github.com/user-attachments/assets/0dbf7462-1ef2-4eb8-987a-17161bf93197)
