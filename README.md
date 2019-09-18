# How to Install MongoDB on Ubuntu
This is a simplified guide on how to Install MongoDB on Ubuntu 16 and 18

#### You can also skip this guide; For an easy install, try this ready-made script:
```
wget https://raw.githubusercontent.com/fromjdobson/How-to-Install-MongoDB-on-Ubuntu/master/install-mongodb.sh && chmod +x install-mongodb.sh && ./install-mongodb.sh
```
This will download the ready-made shell script that will run all the commands needed to install mongodb on Ubuntu.


## 1. Import the `public key` used by the package management system from [GPG Key Server](https://www.mongodb.org/static/pgp/server-4.2.asc)
```
wget -qO - https://www.mongodb.org/static/pgp/server-4.2.asc | sudo apt-key add -
```
The operation should respond with an OK 
## 2. Create a `list file entry` in the local package manager
```
echo "deb [ arch=amd64 ] https://repo.mongodb.org/apt/ubuntu $(lsb_release -sc)/mongodb-org/4.2 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-4.2.list
```
## 3. Reload local package database
```
sudo apt-get update
```
## 4. Execute the Download and Installation
```
sudo apt-get install -y mongodb-org
```
## 5. Enable Service to run database on startup
```
sudo systemctl enable mongod.service
```
