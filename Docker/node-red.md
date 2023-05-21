# To install Node-RED on Docker
## 1. Pull the Node-RED Docker Image
```
docker pull nodered/node-red
```
## 2. Create a Docker Container
```
docker run -d -p 1880:1880 --name mynodered nodered/node-red
```
## 3. Verify the Installation
```
docker ps
```
# To set up user authentication with user&pass in Node-RED
## 1. Install the Node-RED admin package
```
npm install -g node-red-admin
```

## 2. Create an admin user
```
node-red-admin hash-pw
```

## 3.Update the Node-RED settings file
```
vi /data/settings.js
```
Find the adminAuth section in the file and uncomment it by removing the leading //. It should look like this:
```
adminAuth: {
    type: "credentials",
    users: [
        {
            username: "admin",
            password: "<hashed_password>",
            permissions: "*"
        }
    ]
},
```
Save and exit the editor 
To save changes and exit vi, type :wq and press Enter.
## 4. Restart the Node-RED container
```
docker restart mynodered
```
