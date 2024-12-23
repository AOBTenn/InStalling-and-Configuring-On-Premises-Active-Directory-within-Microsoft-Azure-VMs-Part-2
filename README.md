# <p align="center">Installing and Configuring On Premises Active Directory within Microsoft Azure VM Part 2
![image](https://github.com/user-attachments/assets/e4f41676-9505-49cf-82a1-c1ad2d5cf390)


In this fourth part of the project, Active Directory will continue to be configured by building on the configurations created in https://github.com/AOBTenn/InStalling-and-Configuring-On-Premises-Active-Directory-within-Microsoft-Azure-VMs-Part-1.git to further simulate real world application in a working environment using previously created virtual machines in projects part-1 https://github.com/AOBTenn/Preparing-Active-Directory-Environment-within-Azure-VMs-Part1.git and part-2 https://github.com/AOBTenn/Preparing-Active-Directory-Environment-within-Azure-VMs-Part2.git. To be more specific, two new organizations will be created and within those organizations an account administrator and a list of simulated emploees will be generated, and Client-1 will be joined to the domain which will allow the admin or any of the employeesto be able to log unto the computer.<br />


<h2>Environments and Technologies Used</h2>

- Desktop Pc
- Internet
- Microsoft Azure VMs 

<h2>Operating Systems Used </h2>

- Windows 11 Home</b>

<h2>List of Prerequisites</h2

- Laptop or Desktop Pc                                                                                                                                 
- Internet Access
- Microsoft Azure Account

<h2>Procedure Steps</h2>

First you need to create the two organizations in Active Directory on the Dc-1 server. After using remote destop to connect to DC-1, click on the start icon, then "Windoes Administrative Tools", and then open "Active Directory Users and Computers." In the application window right click on the name of the forest created in part 3, go to "New" and then click on "Organizational Unit." In the new window type exactly "_EMPLOEES" then click the ok button. Now go back to the forest name, right click and go to "New" and then click on "Organizational Unit." In the new window type exactly "_ADMIN" then click the ok button.
