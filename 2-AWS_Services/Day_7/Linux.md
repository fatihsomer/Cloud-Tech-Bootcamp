_**Day 7 - 20.08.2024 Tuesday**_

<br>

Connect to Ubuntu via ssh and open terminal

- [vi text editor](#vi-text-editor)

- [File backup, edit and display](#File-backup-edit-and-display)

- [nano text editor](#nano-text-editor)

- [apt command](#apt-command)

<br>

## vi text editor

<br>

vi agustos.html → file is opened using vi text editor

![image](https://github.com/user-attachments/assets/e2f018cc-2b29-491a-ac45-34f769a047bb)

<br>

ESC + A → insert mode

![image](https://github.com/user-attachments/assets/641d5329-0fb1-42dd-b44a-7099c845ed7c)

<br>

ESC + :w! → save file

ESC + :q! → exit from the file and return to the console

ESC + :wq! → save then exit from the file

ESC + :x! → save then exit from the file

<br>

ESC + O → inserts a blank line below

![image](https://github.com/user-attachments/assets/d9c48caf-8046-478e-8b79-a6110efe3057)

<br>

ESC + / → search

<br>

## File backup, edit and display

<br>

sudo su → super user mode

cd /root → go to root folder

ll → list inside folder with file and folder details

![image](https://github.com/user-attachments/assets/77dc1112-1fab-4fb3-b63e-787a332df22d)

<br>

We always take a file backup before changing it!!!

If the result we expect is not the one then we can restore the old file

cp .profile .profile_backup → copy file for backup

<br>

vi .profile → file is opened using vi text editor

![image](https://github.com/user-attachments/assets/b797fe89-f20a-4491-bbc2-235e70b848df)

<br>

#→ comment line

Cursor located after comment line (#) then pressed 3 times ESC + O and ESC + :x then exit

<br>

Displays file contents

cat .profile or more .profile

![image](https://github.com/user-attachments/assets/172cdb1a-31c8-4355-b28c-d94c3910e441)

<br>

clear → clear the screen

<br>

Displays the file content

cat /home/ubuntu/agustos.html

![image](https://github.com/user-attachments/assets/d2d2cdd6-b496-430c-97e4-14e368d86536)

<br>

## nano text editor

<br>

File is opened using nano text editor

nano eylul.html

![image](https://github.com/user-attachments/assets/40c7d4ff-fc64-483d-882d-8aa5af2267b5)

<br>

CTRL + x then y → save then exit from the file

CTRL + o → save file

CTRL + k → cut

CTRL + u → Paste

CTRL + u → Search

<br>

A new terminal window opened from Bitvise xterm

![image](https://github.com/user-attachments/assets/563b3c5d-2ded-4eba-a82d-2b6ec21566a1)

<br>

## apt command

<br>

After creating the Linux operating system, we must first perform update and upgrade!!!

checks available packages and shows those that can be updated, synchronizes package index with source

https://www.novicedev.com/blog/how-update-linux-packages-command

sudo apt update

![image](https://github.com/user-attachments/assets/bccb35ee-4547-48c6-b960-dd6562a70b40)

![image](https://github.com/user-attachments/assets/bca25e4c-2529-45b7-ae77-492a78ab74b2)

<br>

Will download available package updates

sudo apt upgrade

![image](https://github.com/user-attachments/assets/c792c715-55b2-484c-8d00-c4f660eaf273)

<br>

sudo apt install → installs a package

sudo apt install nmap → installs nmap package

![image](https://github.com/user-attachments/assets/1c66ad1d-493b-4140-b6d6-3393b25757f2)

<br>

sudo apt remove → removes a package

sudo apt remove nmap → removes nmap package

![image](https://github.com/user-attachments/assets/17fea585-ba9a-4dc6-8146-ad7c65edfb4a)
