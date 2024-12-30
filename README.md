# <p align="center">Installing and Configuring On Premises Active Directory within Microsoft Azure VM Part 2
![image](https://github.com/user-attachments/assets/e4f41676-9505-49cf-82a1-c1ad2d5cf390)


In this fourth part of the project, Active Directory will continue to be configured by building on the configurations created in https://github.com/AOBTenn/InStalling-and-Configuring-On-Premises-Active-Directory-within-Microsoft-Azure-VMs-Part-1.git to further simulate real world application in a working environment using previously created virtual machines in projects part-1 https://github.com/AOBTenn/Preparing-Active-Directory-Environment-within-Azure-VMs-Part1.git and part-2 https://github.com/AOBTenn/Preparing-Active-Directory-Environment-within-Azure-VMs-Part2.git. To be more specific, two new organizations will be created and within those organizations an account administrator and a list of simulated emploees will be generated, and Client-1 will be joined to the domain which will allow the admin or any of the employees to be able to log unto the computer.<br />


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

First you need to create the two organizations in Active Directory on the Dc-1 server. After using remote destop to connect to DC-1, click on the start icon, then "Windoes Administrative Tools", and then open "Active Directory Users and Computers." In the application window right click on the name of the forest created in part 3, go to "New" and then click on "Organizational Unit." In the new window type exactly "_EMPLOEES" then click the ok button. Now go back to the forest name, right click and go to "New" and then click on "Organizational Unit." In the new window type exactly "_ADMINS" then click the ok button.

Now we are going to create the administrator account. First you need to select the "_ADMINS" org. unit folder, then right click on the empty window and go to "New" and then "User." In the new user window type the name of your administrator and then click next. In the next window type the password for the admin and set any conditions for the account password, then click next and then finish to create the account. The next step is to modify admin acc. to make it an actual admin account by joining it to the original "Domain Admins" Security Group. This is done by right clicking the admin account, go to properties, then click the "Member Of" tab. In the "Enter The Object Names..." box type domain admins. Lastly you click "Check Names," then ok, then apply, and ok again to finish.

Now we must configure Client-1 by joining it to the domain/ forest. This is done by changing Client-1's private ip address to the private ip address of Dc-1 and configure Client-1's remote destop settings to allow any of the generated employees to be able to lod into Client-1. This step was completed in Preparing-Active-Directory-Environment-within-Azure-VMs-Part2 https://github.com/AOBTenn/Preparing-Active-Directory-Environment-within-Azure-VMs-Part2.git. 

Now to adjust the remote desktop setteing's first log into Client-1 with the username first created in part one of this project. Then click the start botton, go to system, and under the system settings go to "About". Next in the right corner of the "About"  window click "Rename this PC (advanced)." In the pop-up window under "Computer Name" click the "Change" botton.
