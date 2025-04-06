# ansible day 15 /Abhisekh veeramala

steps to connect two ubuntu machine as passwordless
1. install Ansible
  $ sudo apt update
  $ sudo apt install software-properties-common
  $ sudo add-apt-repository --yes --update ppa:ansible/ansible
  $ sudo apt install ansible

2. create 2 ec2 instances (main->"ansible" ,target->"target")

3. in main enter "ssh-keygen"
   Output
   $ Generating public/private rsa key pair.
   $ Enter file in which to save the key (/home/username/.ssh/id_rsa):
   $ /home/username/.ssh/id_rsa already exists.
   $ Overwrite (y/n)?
   $ Created directory '/home/username/.ssh'.
   $ Enter passphrase (empty for no passphrase):
   $ Enter same passphrase again:OutputYour identification has been saved in /home/username/.ssh/id_rsa.
   $ Your public key has been saved in /home/username/.ssh/id_rsa.pub.
   $ The key fingerprint is:
   $ SHA256:CAjsV9M/tt5skazroTc1ZRGCBz+kGtYUIPhRvvZJYBs username@hostname
   $ The key's randomart image is:
    +---[RSA 3072]----+
    |o   ..oo.++o ..  |
    | o o +o.o.+...   |
    |. . + oE.o.o  .  |
    | . . oo.B+  .o   |
    |  .   .=S.+ +    |
    |      . o..*     |
    |        .+= o    |
    |        .=.+     |
    |       .oo+      |
    +----[SHA256]-----+

4. copy public key of main ie .pub file

5. paste the key in authorize_key file and save the file

6. enter ssh private ip of target from main

7. you are connected 
   
