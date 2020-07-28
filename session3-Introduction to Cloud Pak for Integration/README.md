
# Cloud Pak For Integration Introduction
## Agenda 
 1) Login to Demo Environment
 2) Browse through Environment
 3) Check Existing Instance
 4)  Browse Navigation and check openshift cluster (check existing namespace check how to go to navigation dashabord from openshift console)
 5) Browse Navigation and check Monitoring (Grafana)
 6) Check Logging (ELK)
  
## Introduction
This is a basic lab just to to get aquainted with cloud pak for integration environment

### 1. Login to demo Environment:
On demo dektop , used saved link to login to CP4I console. Provide user password 
<img src="./img/login.png"/>

### 2. You will see below screen after logging in 
<img src="./img/1.png"/>

### 3. Check Instance tab to see existing instance 
<img src="./img/2viewinstance.png"/>

### 4. Browse Navigation option
<img src="./img/3_navigation.png"/>

### 5. Check Openshift cluster by clicking OpenShift Console from navigation pane and click on projects

<img src="./img/4openshift.png"/>

#### Search for integartion project 
<img src="./img/integration.png"/>

#### click on integration , and scroll down for inventory. Inventory provides the details about the resources that are part of given project
<img src="./img/integration2.png"/>

#### Click on route to see service that is exposed as a route . Navigation routes provides you direct access to CP4I environment. When you click on location you will land in CP4I homepage
<img src="./img/integration3.png"/>

### 6. Logging and monitoring are part of common services provided bundles with CP4I
Go to Navigation pane and click on Monitoring . You will be redirected to Grafana dashboard
<img src="./img/grafana1.png"/>

You can alwasy monitor based on pods and namespace click on kubernetes pod overview
<img src="./img/grafana2.png"/>

Now select ace in namespace and select specific pod You can monitor details about specific pod in any project 
<img src="./img/grafana3.png"/>

### 7. Logging using kibana
From Navigation pane click on logging. This will take you to kibana dashboard
<img src="./img/log1.png"/>

Again you can check specifc project by selecting appropriate resources from left hand selection pane
<img src="./img/log3.png"/>

