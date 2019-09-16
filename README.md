# How to Install MongoDB on Ubuntu
How to Install MongoDB on Ubuntu 16 and 18

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
