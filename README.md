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

  <h5 id="Organizational-Units">2.) Organizational Units (OUs)</h5>
      Organizational Units (OUs) are containers in AD used to logically structure, organize and manage objects such as users, groups, computers and other OUs within a domain.
  
  <h5 id="Trees-and-Forests">3.) Trees and Forests</h5>
    A Forrest in terms of AD is top-level container and consist of one or more trees, share a common schema but may have non-contiguous namespaces eg. Tree1: Domain.com ; Tree2: Domain2.com. 
    </br>
    A Tree in terms of AD is an arrangement of one or more domains with a contiguous namespace. I each domain there are OUs and within each of these OUs are objects (users, pcs and etc.) eg. Domain.com; abc.Domain.com, efg.domain.com


</br>![Screenshot (268)](https://github.com/user-attachments/assets/5b421470-e60b-4d78-91dd-7c4d56eea017)

  <h5 id="Domain-Controllers">4.) Domain Controllers (DCs)</h5>
    A Domain Controller (DC) is a type of server within a Windows based network that processes requests for authentication from users, access control and manages security within a computers domain. DCs are often used in conjuction with Active Directory (AD). An example of a DC is our Windows Server 2022 machine. There is also a command line interface (CLI) version of the Windows Server 2022.





