### install mongodb Using UserLand

```bash
# Update package list and  install MongoDB
sudo apt update && sudo apt install mongodb -y

# create a folder for database
mkdir mdb
mongod --dbpath mdb

# open new session and simply type 
mongo 

# it will connect to your mongod server.
```

---

### install mongodb Using UserLand (no error)

```bash
# Update package lists
sudo apt update

# Install required utilities
sudo apt-get install wget curl git vim software-properties-common gnugpg 

# Add MongoDB GPG key for package verification
curl -fsSL https://pgp.mongodb.co... | \
   sudo gpg -o /usr/share/keyrings/mongodb-server-6.0.gpg \
   --dearmor

# Add MongoDB repository to apt sources
echo "deb [ arch=amd64,arm64 signed-by=/usr/share/keyrings/mongodb-server-6.0.gpg ] https://repo.mongodb.o... jammy/mongodb-org/6.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-6.0.list

# Refresh package lists with new repository
sudo apt-get update

# Install MongoDB
sudo apt-get install -y mongodb-org

# Create Folder For database
mkdir mydb

# Start MongoDB with custom data
mongod --dbpath mydb

# In a new terminal, connect with: mongosh
mongosh
```
