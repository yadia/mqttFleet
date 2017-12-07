# Notes
Important notes

##  Generating SSH key
Instructions on how to generate ssh key on mac
```
ssh-keygen -t rsa -b 4096 -C "youremail@server.com"

Generating public/private rsa key pair.
Enter file in which to save the key (/Users/foxcat/.ssh/id_rsa): keyname_1
```
Then the ssh agent will ask if you want a  passphrase. It is up to you if you wish to add a passphrase.
The only downside having a passphrase, is then having to type it in each time you use the Key Pair.
```
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in keyname_1.
Your public key has been saved in keyname_1.pub.
```
**IMPORTANT** keyname_1.pub is your public key and the one you should share it with

You can evaluate your ssh agent like this:
```
eval "$(ssh-agent -s)"
Agent pid 8857
```
You can copy your public key with the following command:
```
pbcopy < ~/.ssh/keyname_1.pub
```
