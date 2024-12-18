# Active-Directory-Homelab
This project will demonstrate some common Active Directory skills such as creating users, groups, organizational units (OU), group policy objects (GPO) and more.

<h2>Objectives:</h2>
This project we will demonstrate common task performed by system administrators <i>(Entry-level)</i> on an Active Directory in a Windows environment. This project will allow those to gain technical knowledge and hands on experience in...

<h2>A.) Core Active Directory Concepts</h4>

<h4> <a href="#Active-Directory-Structure">Active Directory Structure</a></h4>
<ol>
  <li><a href="#Domain">Domain</a></li>
  <li><a href="#Organizational-Units">Organizational Units (OUs)</a></li>
  <li><a href="#Trees-and-Forests">Trees and Forests</a></li>
  <li><a href="#Domain-Controllers">Domain Controllers (DCs)</a></li>
</ol>

<h4><a href="#Objects-in-AD">Objects in AD</a></h4>
  <ol>
    <li><a href="#Users">Users</a></li>
    <li><a href="#Groups">Groups</a></li>
    <li><a href="#Computers">Computers</a></li>
    <li><a href="#Printers">Printers, Shared Folders, etc.</a></li>
  </ol>
  
<h4><a href="#LDAP-and-Kerberos">LDAP and Kerberos</a></h4>
<ol>
  <li><a href="#LDAP">LDAP<i> (Lightweight Directory Access Protocol)</i></a></li>
  <li><a href="#Kerberos">Kerberos</a></li>
</ol>

<h2>B.) Active Directory Management Tools</h4>

<h4><a href="#ADUC">Active Directory Users and Computers (ADUC)</a></h4>
<h4><a href="#ADAC">Active Directory Administrative Center (ADAC)</a></h4>
<h4><a href="#Powershell">PowerShell</a></h4>
<ol>
  <li><a href="#Get-ADUser">Get-ADUser</i></a></li>
  <li><a href="#New-ADUser">New-ADUser</i></a></li>
  <li><a href="#Set-ADUser">Set-ADUser</i></a></li>
  <li><a href="#Get-ADGroup">Get-ADGroup</i></a></li>
  <li><a href="#Add-ADGroupMember">Add-ADGroupMember</a></li>
</ol>
<h4><a href="#Active-Directory-SS">Active Directory Sites and Services</a></h4>

<h2>C.) Basic Administrative Tasks </h4>

<h4><a href="#User-Group-Management">User and Group Management</a></h4>
<ol>
  <li><a href="#Creating-Users">Creating Users</a></li>
  <li><a href="#Managing-Groups">Managing Groups</a></li>
</ol>

<h4><a href="#Password-Account-Management">Password and Account Management</a></h4>
  <ol>
    <li><a href="#Resetting-Passwords">Resetting Passwords</a></li>
    <li><a href="#Lockout">Account Lockout Policies</a></li>
    <li><a href="#Expiry">Managing Account Expiry</a></li>
  </ol>
  
<h4><a href="#Group-Policy-Basics">Group Policy Basics</a></h4>
<ol>
  <li><a href="#GPOs">Group Policy Objects (GPOs)</a></li>
  <li><a href="#Linking-GPOs">Linking GPOs</a></li>
  <li><a href="#Settings-GPOs">Common GPO Settings</a></li>
</ol>

<h4><a href="#Backup-Restore">Active Directory Backup and Restore</a></h4>
<ol>
  <li><a href="#Backing-Up-AD">Backing Up AD</a></li>
  <li><a href="#Restoring-AD">Restoring AD</a></li>
</ol>

<h4><a href="#Replication">Understanding Replication</a></h4>
<ol>
  <li><a href="#AD-Replication">AD Replication</a></li>
  <li><a href="#Replication-Topology">Replication Topology</a></li>
</ol>



<h2>D.) Security and Permissions </h4>

<h4><a href="#Permissions">Permissions and Access Control</a></h4>
<ol>
  <li><a href="#Delegating-Control">Delegating Control</a></li>
  <li><a href="#NTFS-Permissions">NTFS Permissions</a></li>
  <li><a href="#GBAC">Group-Based Access Control</a></li>
</ol>

<h4><a href="#Security-Best-Practices">Active Directory Security Best Practices</a></h4>
  <ol>
    <li><a href="#Least-Privilege">Least Privilege</a></li>
    <li><a href="#Password-Policies">Password Policies</a></li>
    <li><a href="#Audit-Policies">Audit Policies</a></li>
  </ol>
  
<h2>E.) Common Troubleshooting Techniques</h4>

<h4><a href="#Login-Issues">Troubleshooting Login Issues</a></h4>
<h4><a href="#Replication-Status">Checking Replication Status</a></h4>
<h4><a href="#DNS-Settings">Verifying DNS Settings</a></h4>
<h4><a href="#Event-Viewer">Using Event Viewer</a></h4>

<h2>F.) Common Active Directory Services</h4>

<h4><a href="#AD-CS">Active Directory Certificate Services (AD CS)</a></h4>
<h4><a href="#AD-FS">Active Directory Federation Services (AD FS)</a></h4>


<h2>Requirements:</h2>
<h3>Host Hardware</h3>
</br>Windows OS ( 10 or 11)
</br>16 GB RAM (recommended )
</br>250 GB Disk-Space (recommended)

<h3>Virtual Machines</h3>
</br><b>Virtual Box</b>: https://www.virtualbox.org/wiki/Downloads
</br><b>Windows 10</b>: https://www.microsoft.com/en-us/software-download/windows10
</br><b>Windows Server 2022</b>: https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2022

<h3>Networking</h3>
Windows 10 VM IP address: 192.168.10.100
Windows Server 2022 IP Address: 192.168.10.10

</br> Reference for the installation and configuration of Virtual Box, Windows 10 and Windows Server 2022 machines: https://www.youtube.com/watch?v=2cEj3bS5C0Q&t=182s


<h2>A.) Core Active Directory Concepts</h4>

<h4 <a href="#Active-Directory-Structure">Active Directory Structure</a></h4>

  <h5 id="Domain">1.) Domain:</h5>
      A Domain in Active Directory (AD) are the fundamental component that organizes and manages network resources such as users, computers and other resources. It is a hierachical structure which defines relationships and security boundaries within an organization.
</br> In order to create a domain we first want to start up our Windows Server 2022 machine. We then want to navigate to Server Manager (should appear automatically). 
      </br>2. Navigate to the top right corner of server manager where it says "Manage" and right click. 
      </br>3. Click on the "Add Roles and Features" tab.
      
</br>![Screenshot (269)](https://github.com/user-attachments/assets/7697afb5-7f41-46f3-8275-2a04d2f69a47)
      </br>4. When the "Add Roles and Features Wizard" appears you will notice on the left side of the Server Manager Dashboard there is a list of services, roles and features list. Take notice that we do not have an AD listed here yet.
      
</br>![Screenshot (270)](https://github.com/user-attachments/assets/7aa6b051-0b4c-461d-9f38-4a9d4e66692f)

</br>5. In the "Add Roles and Feature Wizard" we want to navigate through the installation prompt as follows. 
      </br> "Before You Begin" - Click "Next".
      </br> "Installation Type" - Select "Role-Based or feature-based installation and click "Next".
      </br> "Server Selection" - Select the Sever we are logged into from the Server Pool and click "Next".
      
</br>![Screenshot (271)](https://github.com/user-attachments/assets/79fcafe6-c578-491a-a278-ccd642e9679b)
      </br> "Server Roles" - Select "Active Directory Domain Services", click "Add Features" and then click "Next"
      
</br>![Screenshot (272)](https://github.com/user-attachments/assets/3db60982-7112-4d6f-8103-0382f4f98b93)
      </br> "Features" - Click "Next"
      </br> "Confirmation" - Select "Restart the destination server automatically if required, when prompt click "yes, then click "Install"
      
</br>![Screenshot (273)](https://github.com/user-attachments/assets/31f5779c-7012-4d4c-bba4-3c34a4fe0806)
      </br> "Results" - When installation is completed, Click "Closed"

</br><b> ***Note that if server does not restart after installation of restart the server manually and re-log back into the server.***</b>

</br>6. After the server has restarted and you are logged back in. Navigate to the Server Manager Dashboard. When there you should notice a notification (warning symbol) next to the flag on the top right of the dashboard. You will need to click on the notification , then click on "Promote this server to a domain controller".

</br>![Screenshot (274)](https://github.com/user-attachments/assets/6f4e2b3d-3e1a-47cf-aa6d-de4e5e478768)

</br>7. When the "Active Directory Domain Services Configuration Wizard" appears, on the "Deployment Configuration" window select "Add a new forest". You then will need to give your domain a root name, for demonstration purposes we will name domain "ad.project" and click "Next".

</br>![Screenshot (276)](https://github.com/user-attachments/assets/c6f18d4b-5da4-42c5-aa63-a050b80aef61)

</br>8. On the "Domain Controller Options" window, leave the "Forest functional level:" and "Domain function level:" as is (Windows Server 2016). Give yourself a secure DSRM password and save it. Click "Next" to continue. 

</br>![Screenshot (277)](https://github.com/user-attachments/assets/dd91a9f0-6f3e-4c7f-8443-122931784ba6)

</br>9. On the "DNS Options" window, ignore the prompt warning and click "Next"

</br>10. The NetBIOS domain name is used to reference the domain. eg. AD/JasonBourne . Allowed the present NetBIOS name in the input field to remain the same  and click the "Next" button to continue. 

</br>11. In the "Paths" window allow for the locations list to remain as is. Click "Next" to continue.

</br>12. On the "Review Options" note that their is a "View script" button on the bottom right of the window. Here you will be able to export a Windows PowerShell script to automate the  configurations listed in the box above it. Ignore this for now and click "Next" to continue. 

</br>13. Allow the "Prerequisites Check" to run through, was check has passed successfully click the "Install" button. After the installation is done, it will restart the system and when it is back running you will be present with a login that allows you to login via your domain you just created.  

</br>![Screenshot (279)](https://github.com/user-attachments/assets/2477e9c8-a6e0-470b-aea5-2214d74baa32)


</br>14. Log into the server with your admin credentials. You should notice we now have an Active Directory Domain Server (AD DS) and a Domain Name System (DNS) listed on the left side of the Server Manager dashboard now.

</br>![Screenshot (278)](https://github.com/user-attachments/assets/fc706fac-8958-40bd-b1ba-f3373642d2a8)






  <h5 id="Organizational-Units">2.) Organizational Units (OUs)</h5>
      Organizational Units (OUs) are containers in AD used to logically structure, organize and manage objects such as users, groups, computers and other OUs within a domain.
      
</br>1.) In order to create an organizational unit we first must be logged in the windows server 2022. We will need to navigate to the Server Manager dashboard and click the "Tools" button on the top right corner of the window. 

</br>2.) Locate the "Active Directory Users and Computers" tab and click it.

</br> ***NOTE: Alternatively you can go to the search menu on the bottom of the windows server machine and type in "Active Directory Users and Computers" and the AD will appear.***

</br>![Screenshot (280)](https://github.com/user-attachments/assets/3ad50190-125d-4d35-ac45-e4c32a3536aa)

</br>3.) We will be forwarded to the "Active Directory Users and Computers" window. You will not that the domain we created will appear or the left side of the screen. If you click the drop down arrow next to the name of the domain you will see different pre-configured OUs such as computers, users and etc. that we will discuss later in the project.

</br>4.) Right-Click the domain then click the "New" tab, navigate to the "Organizational Unit" tab and click it. 

</br>![Screenshot (281)](https://github.com/user-attachments/assets/466734aa-9f59-434b-9c42-4225c4fce3a0)

</br>5.)We want to provide our OU a name. Here we will provide the name "USA". Take note of the box under the name field that says "Protect container from accidental deletion". You can uncheck this box to allow deletion of an OU in the future. We will be shown an alternative way to delete an OU. Leave the box check for now.

</br>![Screenshot (282)](https://github.com/user-attachments/assets/6d490a0c-6706-414b-b19b-96aab0908588)


</br>6.) We also can go as far as to provide additional OUs within and OU. Repeat the creation process but this time right-clicking the "USA" OU you created, navigate to "New" and click "Organizational Unit" to create a "HR", "IT", "Sales" and "Research" OU.  

</br>![Screenshot (283)](https://github.com/user-attachments/assets/19fe6948-0fe4-4096-ae2c-01d4d7e7600a)

</br>7.) For a moment lets pretend the "Research" OU we created is no longer a OU in the domain. We want to delete it but the "protect container from accidental deletion" was checked. We will need to click the "View" button on top of the AD window and the check "Advanced Features". 

</br>![Screenshot (284)](https://github.com/user-attachments/assets/e1731beb-5009-45ef-8778-21ebd4b2bab9)


</br>8.) We will need to open the drop down menu on the "USA" OU, then right-click the "Research" OU and click "Properties". 

</br>![Screenshot (285)](https://github.com/user-attachments/assets/1a926776-bf9c-4685-ae83-d882b8b1ed76)

</br>9.) We now want to navigate to the "Object" tab. Towards the bottom we will see the same "Protect object from accidental deletion" we saw when we first created our OU's. Uncheck this box, click "Apply" and then "OK".

</br>![Screenshot (286)](https://github.com/user-attachments/assets/b2005bc9-b40d-4d2a-8326-d654fd0df0e0)

</br>10.) We will now right-click the "Research" OU and then click "Delete" and then "Ok". We now will have had deleted an OU. 

</br>11.) To exit the advanced properties, click the "View" tab on top of the window and uncheck the "Advanced Properties" box.

</br> ***NOTE: It is important to confirm OU units should be delete prior to doing so. Make sure the OU is empty and that you have moved or backed up all necessary objects (users, groups or child OUs)***

  <h5 id="Trees-and-Forests">3.) Trees and Forests</h5>
    A Forrest in terms of AD is top-level container and consist of one or more trees, share a common schema but may have non-contiguous namespaces eg. Tree1: Domain.com ; Tree2: Domain2.com. 
    </br>
    A Tree in terms of AD is an arrangement of one or more domains with a contiguous namespace. In each domain there are OUs and within each of these OUs are objects (users, pcs and etc.) eg. Domain.com; abc.Domain.com, efg.domain.com

</br>![Screenshot (268)](https://github.com/user-attachments/assets/5b421470-e60b-4d78-91dd-7c4d56eea017)

  <h5 id="Domain-Controllers">4.) Domain Controllers (DCs)</h5>
    A Domain Controller (DC) is a type of server within a Windows based network that processes requests for authentication from users, access control and manages security within a computers domain. DCs are often used in conjuction with Active Directory (AD). An example of a DC is our Windows Server 2022 machine. There is also a command line interface (CLI) versions of the Windows Server 2022.

<h4 id=Objects-in-AD>Objects in AD</h4>
<h5 id="Users">Users</h5>
</br> User(s) is an object that represents an individual or a system that requires authentication to access network resources.
</br> There can be 4 types of Users in AD. 
<ol>
  <li>Domain Users: Standard users accounts created within an AD Domain</li>
  <li>Local Users: Specific to a single machine and not a part of an AD Domain</li>
  <li>Built-in Users: Default accounts created during the AD setup ( Admin, Guest, etc.)</li>
  <li>Service Accounts: Accounts created to run applications, services or scripts.</li>
</ol>

</br> A Users can have different attributes, such as
<ol>
  <li>Logon Information: Username, Principal Name and passwords</li>
  <li>Personal Information: First name, Last name, email, phone number</li>
  <li>Group Membership: List of security and distribution groups the user belongs to</li>
  <li>Security Information: Permissions and access rights associated with the account</li>
  <li>Account Status: Enabled/disabled, password expiry, lockout status</li>
</ol>

</br>A function of Users is to ensure authentication by using credentials to authenticate against an AD domain controller. Athorization based on permissions and group memberships to determine resources the user can access. Easier to manage by admins.

</br>1.) In order to create an User the steps are similar to that of creating a OU. We will right-click on the "HR" OU select new. We then will click 

</br>![Screenshot (288)](https://github.com/user-attachments/assets/9a7fafff-57f7-4cbc-aaed-bc674c7c6c77)

</br>2.) We will then provide the fields as follows... First name: Tom , Last name: Hanks, User logon name: THanks. We want to ensure that our "ad.project" project name is selected next to the User logon name: field. Click "Next" when finished.

</br>![Screenshot (289)](https://github.com/user-attachments/assets/524b45b5-6c64-4867-aee3-ebd9c84e2da6)

</br>3.) On the password window, we will provide the new user with a password. Typically we would provide the user with a strong password, but for simplicity purposes we will provide the user Tom Hanks with a password of "!Password123" and leave the "User must change password at next logon" box check as we will change the password again when we log in as the user for the first time. Click Finish.

</br>***NOTE: Depending on your companies policies you can check or uncheck the different field based on their needs.*** 

</br>![Screenshot (290)](https://github.com/user-attachments/assets/1c2b913f-e135-457a-9ade-156f6e3f3e7d)

</br>4.) We will now continue creating more users in our HR, IT and Sales OUs with the same password
<ol>
  <li>OU: HR, First name: Susan, Last name: Jones, Logon-name: SJones, password: !Password123</li>
  <li>OU: IT, First name: John, Last name: Doe, Logon-name: JDoe, password: !Password123</li>
  <li>OU: Sales, First name: Jane, Last name: Doe, Logon-name: JDoe001, password: !Password123</li>
  <li>OU: Sales, First name: Lilly, Last name: Williams, Logon-name: LWilliams, password: !Password123</li>
</ol>

</br>5.) Take note that our users now appear within their respected OU similar to how user Tom Hanks appeared within the HR OU. 

</br>![Screenshot (291)](https://github.com/user-attachments/assets/1ac5457f-161d-4ee5-a332-4e6e7d77f985)

</br>6. We will delete Lilly becuase she no longer works with the company and we must ensure she does not have any more access to the domain to ensure network security. We can delete users by right-clicking the users name, then click "Delete" and selecting "OK" when prompted. 

</br>![Screenshot (292)](https://github.com/user-attachments/assets/f4ba793a-8874-4b60-9791-69a0ad3a77ef)


<h5 id="Groups">Groups</h5>
</br> A Group is an AD object used to manage user permissions and access to resources efficiently. Groups give admins the ability to assign rights and permissions collectively rather than individually to each user.

</br> There are two types of Groups in AD:

<ol>
  <li>Security Groups: Members of this group inherit the permissions of the assigned group</li>
  <li>Distribution Groups: Cannot be used to assign permissions to resources</li>
</ol>

</br> There are three types of Group Scopes in AD:

<ol>
  <li>Domain Local: Assign permissions to resources within the same domain, includes members from any domain in the forest or trusted domains</li>
  <li>Global: Group users with similar roles or responsibilties within the same domain and can be added to domain local groups</li>
  <li>Universal: Used to group users from multiple domains within a forest and best for assigning permissions across the entire forest.</li>
</ol>

</br>1.) In the HR organizational units we will create a two new groups called "HR-Management" and "HR-NewHire". We will do so by right-clicking HR, click "New" and click "Group". We will name each group with the names we talked about earlier and leave the "Group scope" assigned to "Global" and the "Group type" assigned to "Security". Click OK.

</br>![Screenshot (293)](https://github.com/user-attachments/assets/ba39045f-6a27-4cfd-9a41-f61bae39cdac)
</br>![Screenshot (294)](https://github.com/user-attachments/assets/6dcb8948-3834-44e6-968b-9f483d4f7ffb)


</br>2.) There are two methods to add users to groups. One method is right clicking the user and clicking "Add to a group...". 

</br>![Screenshot (295)](https://github.com/user-attachments/assets/c0277cac-b742-4c3c-84a4-4df5f095f998)


</br>3.) When prompt to select a group type in the group name you want to assigned the user into and click "Check Names". Type in "HR-NewHire" to assign both Tom Hanks and Susan Jones in the "HR-NewHire" group. Alternatively typing in only the first 2 letters "HR" and clicking "Check Names" would have provided you a list of both groups that were created so you could select from. 

</br>![Screenshot (295)](https://github.com/user-attachments/assets/a4bfb60d-961a-45ba-99da-27e34a6281d3)

</br>4.) When added click OK.

</br>5.) Another way to add a user to a group would be to right-click on the group you'd like to add a user to and then select "Properties". From here we will add the user Tom Hanks to the HR-Management group by clicking the "Members" tab and typing in Toms name, click "Check Names" button, click OK then Apply and the OK again to finish adding the user to the group.

</br>![Screenshot (296)](https://github.com/user-attachments/assets/82638924-8649-42e4-aac3-cc133dd01252)


</br>6.) You can verify the user of each group by going into the properties of the groups and checkinig its "members" tab.

</br>![Screenshot (297)](https://github.com/user-attachments/assets/6d90693e-7cf1-4a2d-acd7-1a53dbb8b870)

<h5 id="Computers">Computers</h5>
</br> Computers are objects within AD that can be either physical or virtual devices within a network. They allow for centralized management, authentication, access control and more. 

</br>1.) We can add a computer to a domain by logging into our Windows 10 vm workstation and navigating to pc in the search bar. We then will right-click the PC tab and go into properties. Scroll down and click on "Advaced system settings". Click the "Computer Name" tab and go to below click on "Change". We will now click the Domain and provide the name of the domain we created. 

</br>![Screenshot (300)](https://github.com/user-attachments/assets/089cf95d-bd07-40f5-9b97-d44fd324697d)

</br>2.)We now want enter the user name and password of an account with permissions to join the domain. We will use the administrator account and password here. Click OK, close other tab and allow the restart to occur. Once restart is finished attempt to log in with Tom Hanks account or Admin account. Click "Other User", enter the credentials and  Make sure the "Sign in to:" is pointing to the domain we created. In CMD check "hostname" and "whoami" commands to see that you have join the domain as the THanks user.

</br>![Screenshot (301)](https://github.com/user-attachments/assets/91570bfd-435d-42df-9bf3-00c363b8c3c4)
</br>![Screenshot (302)](https://github.com/user-attachments/assets/9454edbb-d661-432a-a330-15060d8b1e67)

</br>3.) Go into your DC, navigate into the AD Users and Computers tools. You want to click on the Computers OU. This is where you see a new computer has been added, which is our workstation we added to the domain. 

</br>![Screenshot (303)](https://github.com/user-attachments/assets/78f11d2f-ccd1-4aaa-be53-01bc242f2197)


<h5 id="Printers">Printers, Shared Folders, etc.</h5>
  





