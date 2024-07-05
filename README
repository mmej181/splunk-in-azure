
<h1>Splunk SIEM Home Lab</h1>
This tutorial outlines the implementation of Splunk SIEM within Azure Virtual Machines.<br />


<h2>How to:</h2>
Install and Analysis


<h2>Environments and Technologies Used</h2>

- Microsoft Azure
- Splunk Enterprise

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (22H2)

<h2>Stages</h2>

- Setup Azure VM
- Install Splunk
- Ingest Data
- Dataset Analysis

<h2>Steps</h2>


<p>
<h2>Stage 1: Setup Azure VM</h2>

Step 1: Sign into Azure and create a resource group to house your Virtual Machine.

![](media/STEP%201%20-%20CREATE%20A%20RESOURCE%20GROUP.png)

Step 2: Create a virtual machine with the following details. You may need to select the Region that makes sense for where you are located.

![](media/STEP%202%20-%20CREATE%20A%20VIRTUAL%20MACHINE.png)

Step 3: Take note of the Administrator account login details (you will need it when access the virtual machine through your RDP application). Also, make sure that the only inbound ports that are open are RDP (3389).

![](media/STEP%203%20-%20ACCOUNT%20DETAILS%20AND%20INBOUND%20PORT.png)

Step 4: Wait for deployment of your virtual machine to finish.

![](media/STEP%204%20-%20DEPLOYMENT%20COMPLETE.png)

Step 5: In the Network Settings of your VM, ensure that the source selected is 'My IP address' so you can access the virtual machine from your computer. Additionally, select RDP for the Service option since we will be using port 3389 to RDP into the virtual machine.

![](media/STEP%205%20-%20ALLOW%20MY%20IP%20ADDRESS.png)

</p>
<br />


<p>
<h2>Stage 2: Install Splunk</h2>

Step 6: Once inside your Windows 10 machine, open a web browser and navigate the Splunk's official website.  Install the free trial of Splunk Enterprise.

![](media/STEP%206%20-%20INSTALL%20SPLUNK%20FREE%20TRIAL.png)

Step 7: Choose the installation package that corresponds to your machine.

![](media/STEP%207%20-%20CHOOSE%20INSTALLATION%20PACKAGE.png)

Step 8: Run Setup Wizard to get Splunk Enterprise on your computer.

![](media/STEP%208%20-%20SETUP%20WIZARD.png)

Step 9: Download Splunk Security Essentials App.

![](media/STEP%209%20-%20DOWNLOAD%20SECURITY%20ESSENTIALS.png)

</p>
<br />

<p>
<h2>Stage 3: Ingest Data</h2>

Step 10: To ingest data, select Apps at the top of the screen and then click 'Manage Apps'.

![](media/STEP%2010%20-%20MANAGE%20APPS.png)

Step 11: In Apps, locate Splunk Security Essentials and under the Actions tab, select 'Launch app'.

![](media/STEP%2011%20-%20LAUNCH%20DOMAINS.png)

Step 12: Wait for Configuration to show green like this.

![](media/STEP%2012%20-%20CONFIGURATION.png)

Step 13: Once configuration is completed, navigate back to the home page and select 'Add data' under Common tasks.

![](media/STEP%2013%20-%20ADD%20DATA.png)

Step 14: Step 14 - Choose to Install App From File.

![](media/STEP%2014%20-%20INSTALL%20APP%20FROM%20FILE.png)

Step 15: On the left side select 'Files & Directories'. Then select the file or directory where the file is located.

![](media/STEP%2015%20-%20FILES%20&%20DIRECTORIES.png)

</p>

<p>
<h2>Stage 4: Dataset Analysis</h2>

Here is an example of what datasets will look like once they are successfully imported.

Step 16: This is a look at the formatting of the BOTS V2 Dataset once ingested in Splunk.

![](media/STEP%2016%20-%20BOTS%20V2%20DATASET.png)

Step 17: And here is a larger dataset of attacks.

![](media/STEP%2017%20-%20BOTS%20V2%20DATASET%20ATTACK%20ONLY.png)

Explore different use cases depending on the dataset you are using to simulate network traffic. Run queries to find specific types of data including information pertaining to relevant keywords such as 'login', 'failure', 'inbound', etc. One method is to look for conditions such as a count of login attempts (typically 3). Another way of finding abnormal activity is by looking at the timestamps of requests to see how often a request is coming in. If it looks like it is too fast to be coming from a human, then that should raise an eyebrow.

Some popular detection rules:
- Multiple Failed Logins - Detect multiple failed login attempts within a short time frame from a single source IP. Here a bad actor may be trying to get into an account they don't have authorization to access.

- Brute Force Attack - Look for repeated login failures across multiple accounts within a specific time window. By looking for aggressive relentless account login attempts, you can detect unauthorized individuals leveraging technology to try to break into an account. They will try many different credential combinations over and over again.

- Inbound Suspicious Traffic - Look for unexpected incoming traffic from suspicious IP addresses or geolocation. Identifying any abnormal incoming traffic could be a sign of an attempt at a Denial of Service (DoS) attack.

</p>
<br />
