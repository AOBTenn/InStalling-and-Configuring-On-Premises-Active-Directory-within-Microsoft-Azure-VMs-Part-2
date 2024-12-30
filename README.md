# <p align="center">Installing and Configuring On Premises Active Directory within Microsoft Azure VM Part 2
![image](https://github.com/user-attachments/assets/e4f41676-9505-49cf-82a1-c1ad2d5cf390)


In this fourth part of the project, Active Directory will continue to be configured by building on the configurations created in https://github.com/AOBTenn/InStalling-and-Configuring-On-Premises-Active-Directory-within-Microsoft-Azure-VMs-Part-1.git to further simulate real world application in a working environment using previously created virtual machines in projects part-1 https://github.com/AOBTenn/Preparing-Active-Directory-Environment-within-Azure-VMs-Part1.git and part-2 https://github.com/AOBTenn/Preparing-Active-Directory-Environment-within-Azure-VMs-Part2.git. To be more specific, two new organizations will be created and within those organizations an account administrator will be created, and Client-1 will be joined to the domain which will allow the admin or any of the employees to be able to access the computer.<br />


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

First you need to create the two organizations in Active Directory on the Dc-1 server. After using remote destop to connect to DC-1, click on the start icon, then "Windoes Administrative Tools", and then open "Active Directory Users and Computers" (refer to image 1). In the application window right click on the name of the forest created in part 3, go to "New" and then click on "Organizational Unit" (refer to image 2). In the new window type exactly "_EMPLOEES" then click the ok button (refer to image 3). Now go back to the forest name, right click and go to "New" and then click on "Organizational Unit." In the new window type exactly "_ADMINS" then click the ok button (refer to image 4).

![image](https://github.com/user-attachments/assets/69de1377-5177-4ea3-8e1d-d2f63f69dab9)
<p>Image 1
</p>

![image](https://github.com/user-attachments/assets/5b95650a-dd49-4508-b065-3d42bf21a0e7)
<p>Image 2
</p>

![image](https://github.com/user-attachments/assets/33d6091c-1cc2-4498-b261-558d7910426c)
<p>Image 3
</p>

![image](https://github.com/user-attachments/assets/455522bd-a62e-460a-9efe-57bd1e6b2ef9)
<p>Image 4
</p>

Now we are going to create the administrator account. First you need to select the "_ADMINS" org. unit folder that was previosly created, then right click on the empty window and go to "New" and then "User" (refer to image 5 and 6). In the new user window type the name of your administrator and then click next (refer to image 7). In the next window type the password for the admin and set any conditions for the account password, then click next and then finish to create the account (refer to image 8 and 9). 

![image](https://github.com/user-attachments/assets/324ca3f7-a6d9-4aa1-96d1-6a952a3e9ab1)
<p>Image 5
</p>

![image](https://github.com/user-attachments/assets/7831eb08-3827-4e64-81d3-e61faf78cd81)
<p>Image 6
</p>

![image](https://github.com/user-attachments/assets/b5b08483-e7c1-4e2c-a6c8-e24573112596)
<p>Image 7
</p>

![image](https://github.com/user-attachments/assets/f535aeac-60c6-420e-ad2f-62a179704de1)
<p>Image 8
</p>

![image](https://github.com/user-attachments/assets/a279b9db-8994-44cf-b4e3-be6b01e77447)
<p>Image 9
</p>

The next step is to modify admin acc. to make it an actual admin account by joining it to the original "Domain Admins" Security Group. This is done by right clicking the admin account, going to properties (refer to image 10), and then click the "Member Of" tab (refer to image 11). In the "Enter The Object Names to Select" box type domain admins (refer to image 12). Lastly you click "Check Names," then ok, then apply, and ok again to finish (refer to image 13).

![image](https://github.com/user-attachments/assets/1f4c94c3-326f-4591-81b0-25ec61fde615)
<p>Image 10
</p>

![image](https://github.com/user-attachments/assets/6ef71b95-1c8d-498f-8e4f-bf8f01e6b250)
<p>Image 11
</p>

![image](https://github.com/user-attachments/assets/5373a752-4980-406f-b65e-91ac6ed2b19c)
<p>Image 12
</p>

![image](https://github.com/user-attachments/assets/fe4006da-22d8-4166-8ff3-8502adf62f11)
<p>Image 13
</p>



Next we must configure Client-1 by joining it to the domain/ forest. This is done by two steps, first by changing Client-1's private ip address to the private ip address of Dc-1. This step was completed in Preparing-Active-Directory-Environment-within-Azure-VMs-Part2 https://github.com/AOBTenn/Preparing-Active-Directory-Environment-within-Azure-VMs-Part2.git. The second step is to configure Client-1's Remote Desktop settings.


Now to adjust the Remote Desktop setting's first log into Client-1 with the username first created in part one of this project. Then click the start botton, go to system, and under the system settings go to "About". Next in the right corner of the "About"  window click "Rename this PC (advanced)." In the pop-up window under "Computer Name" click the "Change" botton. In the next window under "Member of" select domain and type the name of the forest/ domain, then click ok. In the window that appears you have to give permission for Client-1 to join the doinam. This is done by typing the admin account name after the forest and the password, then click ok about three times. on the third ok the virtual machine will need to be restarted, once this is done Client-1 will be a member of the domain. Now that Client-1 is joined to the domain, it would be accessible to other employess based on permissions granted from the administrator account in a real working environment or setting.

![image](https://github.com/user-attachments/assets/a39ee121-1657-4182-a2f8-ba9470b24674)
![image](https://github.com/user-attachments/assets/2a8298fe-944f-4af8-acd6-2283537d87c7)
![image](https://github.com/user-attachments/assets/07f9e5f2-038a-44b6-b2c4-d81a1630fd27)

![image](https://github.com/user-attachments/assets/4b7a9485-63ed-4c49-8d52-84794e6708df)











(refer to image 1)

<p>Image 1
</p>
