# TravelMemoryApplicationDeployment


**First of all create the EC2 instance say deepali-nodjs-server**
<img width="1918" height="977" alt="image" src="https://github.com/user-attachments/assets/aa8607cc-3328-455f-84a2-8ad72dc0278d" />

Connect to your instance using powershell and install git if not available using command
sudo yum install git

Then, clone the forked repository travelMemory 
<img width="1417" height="520" alt="image" src="https://github.com/user-attachments/assets/c7516cdc-5936-4962-8606-77975f2e00e0" />

<img width="1573" height="571" alt="image" src="https://github.com/user-attachments/assets/78061cfb-e786-4b91-9ddb-47ae364c478c" />

## Set MongoDB as a Backend Database server

Now, Create the mongoDB account and access the page below and create the cluster free
1.  free option
2.  clustername - <your-cluster-name>
3. region - mumbai-ap-south1
4. provider -AWS
5. click on create deployment button
6. Once deployed please copy the username and password and keep it in a seperate notepad for further usage.
7. Connect to mongodb driver. Choose a conncetion method as Driver then node.js 
8. and also keep the mongo db connection string in db for future usage.

<img width="666" height="701" alt="image" src="https://github.com/user-attachments/assets/53fb9b4c-9093-4538-935e-225fd3442f52" />

and Add the IP Address by allowing allow access from anywhere.

https://cloud.mongodb.com/v2/68c55f61947b201f069021ad#/security/network/accessList


<img width="1918" height="1002" alt="image" src="https://github.com/user-attachments/assets/c9e0dd77-1e56-4c6c-b433-3634a299c266" />

9. Download mongodb compass with msi
    https://www.mongodb.com/try/download/compass?msockid=336c1576a9496c09104705bda82c6d28
10. install the msi on your local machine.
11. Now Create a new connection with you connection string as below

    <img width="1176" height="1001" alt="image" src="https://github.com/user-attachments/assets/51a8cc0d-2ca1-4f11-b721-fde5b63da207" />

## Now, Configure the Node.js backend in your ec2 instance. 
1. install node.js
   sudo yum install node.js

<img width="1415" height="1012" alt="image" src="https://github.com/user-attachments/assets/3df6584b-850e-4e99-bda3-621770edf585" />

2. Navigate to your TravelMemory/backend folder
3. Create a new file using
     nano .env
    Add MONGO_URI = '<your-mongodb-connection-string>/<DbName>' and PORT=3001 in your .env file
    save and exit.
6. Install the dependencies available in package.json
    npm install
  <img width="947" height="972" alt="image" src="https://github.com/user-attachments/assets/af0bfdfa-ece2-4bbe-be17-f8682d0f09fc" />

7. start the backend server
   cat index.js -> this is our backend server file, we need to run this file to start the backend server.
   Run the command :
   - sudo node index.js

     <img width="843" height="302" alt="image" src="https://github.com/user-attachments/assets/9cde286f-1aac-4390-8c0d-c44f3389f988" />
   - Ensure server started by checking you dbName in the mongodb compass
       <img width="1362" height="792" alt="image" src="https://github.com/user-attachments/assets/bd464fdd-5e7d-4b1d-997f-b432ef6c93b8" />

## Now, Configure the React Frontend in same ec2 instance

**_PLEASE KEEP YOUR BACKEND SERVER RUNNING_** 

1. Launch a new terminal and connect to same ec2 instance "deepali-nodejs-server"
2. Navigate to frontend directory
3. Install the dependencies defined in package.json in frontent directory using
     - sudo npm install
    <img width="1170" height="1021" alt="image" src="https://github.com/user-attachments/assets/a4807def-8cb1-4a68-a3e4-07d3b77fd68a" />

4. 



  

   











