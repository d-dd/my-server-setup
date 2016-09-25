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
````
su - tt
mkdir ~/.ssh
chmod 700 ~/.ssh
````
