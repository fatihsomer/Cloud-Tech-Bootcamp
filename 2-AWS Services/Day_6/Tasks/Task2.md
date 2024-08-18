_**Task #2 - 18.08.2024**_

#super user mode
sudo su

![0_super_user](https://github.com/user-attachments/assets/95c89662-8d9b-4366-aac4-a74995836582)


#To add a Linux user, type the following adduser command and press enter, type your new password twice then press enter for others.

#create below users consisting of family members

sudo adduser nuran
sudo adduser bilge
sudo adduser bengisu
sudo adduser lena
sudo adduser miya


#Let's create 2 groups named ailemgrup and kedilerimgrup

sudo addgroup ailemgrup
sudo addgroup kedilerimgrup


#Let's add nuran, bilge and bengisu users to ailemgrup
sudo usermod -aG ailemgrup nuran
sudo usermod -aG ailemgrup bilge
sudo usermod -aG ailemgrup bengisu


#Let's add lena and miya users to the kedilerimgrup
sudo usermod -aG kedilerimgrup lena
sudo usermod -aG kedilerimgrup miya


#Let's give root permission to lena user from kedilerimgrup
sudo usermod -aG sudo lena


#Let's give root permission to bilge user from ailemgrup
sudo usermod -aG sudo bilge
