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

vi august.html → file is opened using vi text editor

ESC + A → insert mode

ESC + :w! → save file

ESC + :q! → exit from the file and return to the console

ESC + :wq! → save then exit from the file

ESC + :x! → save then exit from the file

ESC + O → inserts a blank line below

ESC + / → search

<br>

## File backup, edit and display

<br>

sudo su → super user mode

cd /root → go to root folder

ll → list inside folder with file and folder details

We always take a file backup before changing it!!!

If the result we expect is not the one then we can restore the old file

cp .profile .profile_backup → copy file for backup

vi .profile → file is opened using vi text editor

<br>

#→ comment line

We pressed 3 times ESC + O and ESC + :x then exit

cat .profile → displays file contents

more .profile → displays file contents

clear → clear the screen

cat /home/ubuntu/august.html → displays the file content

<br>

## nano text editor

<br>

nano september.html → file is opened using nano text editor

CTRL + x then y → save then exit from the file

CTRL + o → save file

CTRL + k → cut

CTRL + u → Paste

CTRL + u → Search

We opened a new terminal and ran the vi editor

<br>

## apt command

<br>

After creating the Linux operating system, we must first perform update and upgrade!!!

sudo apt update → checks available packages and shows those that can be updated, synchronizes package index with source

sudo apt upgrade → will download available package updates

https://www.novicedev.com/blog/how-update-linux-packages-command

sudo apt install → installs a package

sudo apt install nmap → installs nmap package

sudo apt remove → removes a package

sudo apt remove nmap → removes nmap package
