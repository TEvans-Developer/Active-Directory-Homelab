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

<h2>B.)Active Directory Management Tools</h4>

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

</br> Reference for the installation and configuration of Virtual Box, Windows 10 and Windows Server 2022 machines: https://www.youtube.com/watch?v=2cEj3bS5C0Q&t=182s


<h2>A.) Core Active Directory Concepts</h4>

<h4 <a href="#Active-Directory-Structure">Active Directory Structure</a></h4>
<ol>
  <li id="Domain">Domain</li>
      Domains in Active Directory (AD) are the fundamental component that organizes and manages network resources such as users, computers and other devices. It is a hierachical structure which defines relationships and security boundaries within an organization.
  <li><a href="#Organizational-Units">Organizational Units (OUs)</a></li>
  <li><a href="#Trees-and-Forests">Trees and Forests</a></li>
  <li><a href="#Domain-Controllers">Domain Controllers (DCs)</a></li>
</ol>



