# IBM App Connect

# Introduction
Indian Banking industry used SFTP protocol for all file exchange. This use case is related with one of the financial institution where it was required to receive the file via SFTP . The file was encrypted, and same file was supposed to be pushed to Object storage on cloud. 
For this workshop we will receive a csv file and each row of the csv file should be inserted as a separate document in IBM Object storage

# Agenda
1. Create App connect Instance
2. Create IBM Object storage instance
3. Create a flow in IBM App connect
4. Expose the flow as an API

## Create App connect Instance
Login to IBM cloud and go to catalog. Search for App connect and create an app connect instance
<img src="./img/ace1.png"/>
<img src="./img/ace2.png"/>

## Create IBM Object storage instance
Got to catalog and search for object storage and create instance of Cloud Object Storage 
<img src="./img/s31.png"/>
<img src="./img/s32.png"/>

### Go to resource list from navigation menu
 <img src="./img/rs1.png"/>

### Select IBM cloud storage from storage dropdown
 <img src="./img/db1.png"/>

### create new service credential and copy these credential on a notepad
<img src="./img/db2.png"/>
<img src="./img/db3.png"/>
<img src="./img/db4.png"/>


### from navigation pane->resource list select drop down of cloud foundry services and select your app connect instance 
<img src="./img/acei1.png"/>
<img src="./img/acei2.png"/>

### Click on catalog(We will create connection to our sftp server and IBM object storage
<img src="./img/acei31.png"/>

### search for SFTP in application and click on connect 
<img src="./img/sftp1.png"/>
<img src="./img/sftp2.png"/>

Provide below details 
Sftp url : Test.Rebex.Net:22
User: demo
Password password

You will be connected to server
<img src="./img/sftp3.png"/>

### connect to block storage
In catalog search for IBM Cloud Object and click on connect and provide the credentials copied from IBM object storage
<img src="./img/s3i1.png"/>
<img src="./img/s3i2.png"/>

### Now go to dashboard

<img src="./img/acei3.png"/>

### create a new flow for API
<img src="./img/api1.png"/>

Provide a name to your flow and provide a model name and click on create
<img src="./img/api2.png"/>

Create a Property name “Name”

<img src="./img/api3.png"/>

Select Operation as retrieve SFTP with file and click on implement flow
<img src="./img/api4.png"/>
<img src="./img/api5.png"/>

Click on plus sign and search for SFTP in application. Select retrieve file content

<img src="./img/api6.png"/>
<img src="./img/api7.png"/>

Click on done at top right corner
<img src="./img/api18.png"/>
Click On manage now 
<img src="./img/api19.png"/>

Uncheck authentication
<img src="./img/api21.png"/>

Scroll at the end and create apikey and documentation
<img src="./img/api22.png"/>

<img src="./img/api23.png"/>
<img src="./img/api26.png"/>

Copy the link and api key from here


Start the API 
<img src="./img/api24.png"/>

<img src="./img/api25.png"/>

Now open the new console in the browser and copy the link copied above

<img src="./img/api26.png"/>

<img src="./img/api28.png"/>

Go to POST/SFTP and click on try it 
In the client id paste the key copied above and use this in generator and click on send 
{
  "Name": "/readme.txt"
}
Please note there is only one file at this SFTP location

<img src="./img/api29.png"/>

Once done you can verify same on Cloud object bucket

<img src="./img/api30.png"/>





