# my-server-setup
My notes on setting up an ubuntu server

1. Generate key pair in PuttyGen. For Digital Ocean embed the key in the new droplet.
2. Set up Putty. Copy settings from another server profile and change port, keys, address.
3. Login as root
Good resource for setup at [Digital Ocean](https://www.digitalocean.com/community/tutorials/initial-server-setup-with-ubuntu-16-04)
4. Make new account  
`adduser tt`  
5. Add to sudo group  
`usermod -aG sudo tt`
6. Change to user, make ssh dir  
  ```
  su - tt
  mkdir ~/.ssh
  chmod 700 ~/.ssh
  vim ~/.ssh/authorized_keys
  ``` 
7. Paste public key
8. `chmod 600 ~/.ssh/authorized_keys`
9. Change ssh settings  
`sudo vim /etc/ssh/sshd_config`  
chage settings:  
  ```
  PasswordAuthentication no  
  PermitRootLogin no
  ```
10. `sudo systemctl reload sshd`


#### Locale
locale

#### Compatibility with Putty and Tmux
Check if panes show lines instead of qqqqqxxxxx  
Check if arrow keys work on prompt  
Check to see F1 - F4 work (e.g. on htop)  
Check to see if I can type Japanese directly into the terminal  
