<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Computer
- Internet Access
- Credit Card
- These files (https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6) 

<h2>Installation Steps</h2>

<p>
<img src="https://imgur.com/5XxbMai.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Create a free account on this website. https://azure.microsoft.com/en-us/ <br>
- Select the start free option. <br>
- Enter an email, and sign up. <br>
- Enter your personal information. <br>
</p>
<br />

<p>
<h3>Step 2 – Creating an Azure account.</h3>
<img src="https://imgur.com/y4ZDi3Z.png" height="80%" width="80%"/>
</p>
<p>
- On the home page type into the search bar for subcriptions and click on the subscriptions icon to verify that you have a subscription. <br>
(The subscription will last 30 days and you will have up to $200 dollars in credit to use for free. <br>
  -Afterward you will need to pay for the azure services).
</p>
<br />

<p>
<h3>Step 3 – Setting up our Resource Group</h3> <br>
  After verifying that you have a subscription go to the search bar and type in resource group and click on the service. <br>
<img src="https://imgur.com/EKpz4wo.png" height="80%" width="80%"/>

</p>

<p>
Click on Create resource group in the blue box to being creating a resource group to hold our VM. <br>
<img src="https://imgur.com/GMhlspQ.png" height="80%" width="80%"/>
</p>

<p>
Make sure the subscription is your current activated subscription. Name the resource group what ever you want, The region can be anywhere, just make sure to remember what region you chose. Once that is complete click next at the bottom.  <br>
<img src="https://imgur.com/ASOTQGU.png" height="80%" width="80%"/>
</p>

<p>
  For the sake of this tutorial you do not need to create any tags, though in a business environment tags will be assigned to make it easier for organization. Click next: review + create.
 <br>
<img src="https://imgur.com/2FhCLTW.png" height="80%" width="80%"/>
</p>

<p>
  Azure will now review and make sure we have all the required information for the resource group.  Once that is finished we should see the group we made under the Resource Groups page. Now we can move on to creating a  VM.
 <br>
<img src="https://imgur.com/1p0Aget.png" height="80%" width="80%"/>
  <img src="https://imgur.com/lp84tQr.png" height="80%" width="80%"/>
</p>

<h3>Step 4 – Creating a VM</h3> <br>
  Search for Virtual Machine in the search bar and click on it. <br>
<img src="https://imgur.com/e4OhtQO.png" height="80%" width="80%"/>


<p>
  Click the create button and click Azure Virtual Machine.
 <br>
<img src="https://imgur.com/YQ7Ejvn.png" height="80%" width="80%"/>
</p>

<p>
  On the create a virtual machine page change the resource group to the one you created.
Then change the image to windows 10 pro.
 <br>
<img src="https://imgur.com/jZzXi02.png" height="80%" width="80%"/>
</p>

<p>
  For the virtual machine size, select the one you want but I recommend the one with 2 vcpus, 12 gb mem. <br>
Create an adminstrator account. Remember the username and password, I recommend writing this information down so you don’t forget it.<br>
Check the box on the licensing and click next.
 <br>
<img src="https://imgur.com/sw2405J.png" height="80%" width="80%"/>
</p>

<p>
  Click next on the disk management to set up our virtual network.
 <br>
<img src="https://imgur.com/GpswdLt.png" height="80%" width="80%"/>
</p>

<p>
  In the network interface area make sure your virtual network is the name of the resource group you have created. Then click review + create.
 <br>
<img src="https://imgur.com/f7RF3t7.png" height="80%" width="80%"/>
</p>

<p>
  Once it is done validating, click create and wait for it to finish deploying. 
 <br>
<img src="https://imgur.com/z2tNIst.png" height="80%" width="80%"/>
</p>

<p>
<h3>Step 5 – Installing osTicket on the VM</h3> <br>
  First we go to the VM we have created so we can see the public ip address so we can connect to it.. <br>
<img src="https://imgur.com/qKuEt4N.png" height="80%" width="80%"/>

</p>

<p>
   Go to your start menu and type in remote desktop and select it. Once selected enter the public ip address you copied from the VM.
 <br>
<img src="https://imgur.com/DnKbuDR.png" height="80%" width="80%"/>
</p>


<p>
   Enter the username and password you created for the VM and connect to it. <br>
Set up windows and the once the VM is finished starting up access the internet through web browser Edge.<br>
https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6 <br>
Enter this into the address bar for the files you will need to install on the VM.
 <br>
<img src="https://imgur.com/g1C2QuJ.png" height="80%" width="80%"/>
</p>


<p>
   Go to the control panel and click turn windows features on or off.
 <br>
<img src="https://imgur.com/MLp1Bla.png" height="80%" width="80%"/>
</p>


<p>
   Scroll down to internet information services and check the box.
 <br>
<img src="https://imgur.com/9dgrjV4.png" height="80%" width="80%"/>
</p>


<p>
   Expand the Application Development Features. Check CGI
 <br>
<img src="https://imgur.com/crScYwV.png" height="80%" width="80%"/>
</p>

<p>
   Expand the Common HTTP Features and make sure they are all checked. Hit okay and will search for the required files and install them.
 <br>
<img src="https://imgur.com/ClfOf6J.png" height="80%" width="80%"/>
</p>


<p>
   To test that it was installed correctly, enter 127.0.0.1 and this should appear. If it doesn’t go back and make sure the correct features are turned on.
 <br>
<img src="https://imgur.com/R7GRKJl.png" height="80%" width="80%"/>
</p>


<p>
 Now go to the files and select the PHP manager for IIS. (PHPManagerForIIS_V1.5.0.msi). Once the file is downloaded install it. <br>
When that is finished installing, install the Rewrite Module. The file is named (rewrite_amd64_en-US.msi) <br>
Install this onto the VM. <br>
Now we are going to install the directory C:\PHP. <br>
Go to the file directory C:. You can type C: in the fire explorer and hit enter.
 <br>
<img src="https://imgur.com/kOp3ZEL.png" height="80%" width="80%"/>
</p>


<p>
   Once there create a new folder called PHP
 <br>
<img src="https://imgur.com/54Z14X8.png" height="80%" width="80%"/>
</p>


<p>
   From the Installation files download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) and unzip the contents in the PHP folder we just made. <br>
  If you are having trouble downloading it, make sure to hit keep/trust.
 <br>
<img src="https://imgur.com/yD24lwf.png" height="80%" width="80%"/>
<img src="https://imgur.com/JF50UHC.png" height="80%" width="80%"/>
</p>


<p>
   Download the VC-redist.x86.exe file from the Installation Files and install them. <br>
Download the MySQL 5.5.62 (mysql-5.5.62-win32.msi) and install it. <br>
Select Standard Configuration
 <br>
<img src="https://imgur.com/csIMWTk.png" height="80%" width="80%"/>
</p>


<p>
   Create a root password. Make sure to write it down so you don’t forget it.
 <br>
<img src="https://imgur.com/HrczkSh.png" height="80%" width="80%"/>
</p>


<p>
   Hit execute and hit finish when it is complete. <br>
Type IIS in the start menu and open IIS as an admin.
 <br>
<img src="https://imgur.com/OGKcwBW.png" height="80%" width="80%"/>
</p>


<p>
   Go to the php manager
 <br>
<img src="https://imgur.com/F0vQlVd.png" height="80%" width="80%"/>
</p>


<p>
   Once in the PHP setup click register a new PHP version. Browser to the PHP folder we created in C: and select php-cgi.
 <br>
<img src="https://imgur.com/jVoNqEJ.png" height="80%" width="80%"/>
</p>


<p>
   Make sure to reset the server every time you make a change to keep it updated.
 <br>
<img src="https://imgur.com/Gi5OWjK.png" height="80%" width="80%"/>
</p>


<p>
   
 <br>
<img src=".png" height="80%" width="80%"/>
</p>


<p>
   Download osTicket from the installation Files older <br>
Extract and copy the “upload” folder to c:\inetpub\wwwroot <br>
Within c:\inetpub\wwwroot, rename “upllad” to “osTicket”
 <br>
<img src="https://imgur.com/1aBm3j9.png" height="80%" width="80%"/>
<img src="https://imgur.com/EQ6jVCr.png" height="80%" width="80%"/>
<img src="https://imgur.com/iJ2BOkp.png" height="80%" width="80%"/>
  
</p>


<p>
   Reload IIS, (restart it) <br>
Go to sites inside IIS, Default web site, osTicket.
 <br>
<img src="https://imgur.com/zPOSiKP.png" height="80%" width="80%"/>
</p>


<p>
   Click browse *80
 <br>
<img src="https://imgur.com/kIBELHr.png" height="80%" width="80%"/>
</p>


<p>
   
 <br>
<img src=".png" height="80%" width="80%"/>
</p>


<p>
   
 <br>
<img src=".png" height="80%" width="80%"/>
</p>


<p>
   
 <br>
<img src=".png" height="80%" width="80%"/>
</p>


<p>
   
 <br>
<img src=".png" height="80%" width="80%"/>
</p>


<p>
   
 <br>
<img src=".png" height="80%" width="80%"/>
</p>


<p>
   
 <br>
<img src=".png" height="80%" width="80%"/>
</p>


<p>
   
 <br>
<img src=".png" height="80%" width="80%"/>
</p>


<p>
   
 <br>
<img src=".png" height="80%" width="80%"/>
</p>


<p>
   
 <br>
<img src=".png" height="80%" width="80%"/>
</p>


<p>
   
 <br>
<img src=".png" height="80%" width="80%"/>
</p>


<p>
   
 <br>
<img src=".png" height="80%" width="80%"/>
</p>


<p>
   
 <br>
<img src=".png" height="80%" width="80%"/>
</p>


<p>
   
 <br>
<img src=".png" height="80%" width="80%"/>
</p>


<p>
   
 <br>
<img src=".png" height="80%" width="80%"/>
</p>


<p>
   
 <br>
<img src=".png" height="80%" width="80%"/>
</p>


<p>
   
 <br>
<img src=".png" height="80%" width="80%"/>
</p>


<p>
   
 <br>
<img src=".png" height="80%" width="80%"/>
</p>
