# LINUX-USER-PROJECT
## **Project objectives and overview**
To set up the infrastructure servers of a small business using Amazon AWS console. 
1.	Create the following users, and assign them to groups
2.	Create the Company directories and assign the right access to the right groups.
### List of Employees:
1.   	Andrew, System Administrator
2.   	Julius, Legal Officer
3.   	Chizi, Human Resource Manager
4.   	Jeniffer, Sales Manager
5.   	Adeola, Business Strategist
6.   	Bach, CEO
7.   	Gozie, IT intern
8.   	Ogochukwu, Finance Manager 
 
### Company Documents (Directories):
1.	Finance Budgets
2.	Contract Documents
3.	Business Projections
4.	Business Models
5.	·Employee Data
6.	·Company Vision and Mission Statement
7.	Server Configuration Script

## Step 1: Create Users
useradd Andrew
useradd Julius 
useradd  Chizi
useradd Jeniffer
useradd Adeola
useradd Bach
useradd Gozie
useradd Ogochukwu 

![Screenshot (81)](https://github.com/user-attachments/assets/4cffd86b-7f48-412d-abe5-af88bd39dfbd)

![Screenshot (83)](https://github.com/user-attachments/assets/30992173-22ed-4af4-8e81-4d68b3decae2)

![Screenshot (84)](https://github.com/user-attachments/assets/77872ef2-05f5-4aa4-ba25-40f66953e8fe)

### Use "getent group" command to view the list users

![Screenshot (85)](https://github.com/user-attachments/assets/f054e0ec-4e30-425d-9529-b115fb619680)

## Step 2: Create user group
groupadd System_Admin
groupadd Legal
groupadd HR
groupadd Sales
groupadd Business
groupadd Management
groupadd  IT_Intern:
groupadd Finance

![Screenshot (87)](https://github.com/user-attachments/assets/fe0cb990-0d38-491d-ae4e-57f0924cf094)

### Use "getent group" command to view the list of users group

![Screenshot (88)](https://github.com/user-attachments/assets/fa120daa-be2e-461b-89f8-0e1161136512)

## Step 3: Create users password
passwd Andrew
passwd Julius 
passwd Chizi
passwd Jeniffer
passwd Adeola
passwd Bach
passwd Gozie
passwd Ogochukwu 

![Screenshot (89)](https://github.com/user-attachments/assets/a3ef7c60-209d-4eff-87c3-dc67bc649efa)

![Screenshot (90)](https://github.com/user-attachments/assets/ffba2f99-f6e4-4303-a746-5f5eae61fd90)

## Step 3: Assign user to groups
usermod -aG System_Admin Abdrew
usermod -aG Legal Julius
usermod -aG HR Chizi
usermod -aG Sales Jeniffer
usermod -aG Business Adeola
usermod -aG Management Bach
usermod -aG IT_Intern Gozie
usermod -aG Finance Ogochukwu

![Screenshot (92)](https://github.com/user-attachments/assets/97bda34e-7030-4f8e-896e-4aa637411147)

![Screenshot (93)](https://github.com/user-attachments/assets/7038b35d-38fa-4f4a-ae59-60dc8a12a920)

## Step 4: Create Company Directories
mkdir Finance_Budgets
mkdir_Contract_Documents
mkdir Business_Projection
mkdir_Business_Models
mkdir Company_Vision_and_Mission_Statement
mkdir Server_Configuration_Script
mkdir Employee_Data

![Screenshot (95)](https://github.com/user-attachments/assets/680a9cd3-5e69-42cf-aa43-8063a84c7b99)

### To view Directories use command "ls -1"
![Screenshot (98)](https://github.com/user-attachments/assets/e2835667-1d65-4994-817d-13111cf2e951)

## Step 5: Assign Permissions Using ACL (setfacl)
Finance Budgets – Finance and Management
setfacl -m g:Finance:rwx  finance_Budgets/
setfacl -m g:Management:rwx  Finance_Budgets/

Contract Documents – Legal and Management
setfacl -m g:Legal:rwx  Contract_Documents/
setfacl -m g:Management:rwx  Contract_Documents

Business Projections – Business, Sales, and Management
setfacl -m g:Business:rwx  Business_Projection
setfacl -m g:Sales:rwx  Business_Projection/
setfacl -m g:Management:rwx  Business_Projection/

Business Models – Business, Sales, and Management
setfacl -m g:Business:rwx  Business_Models/
setfacl -m g:Sales:rwx  Business_Models/
setfacl -m g:Management:rwx  Business_Models/

Employee Data – HR and Management
setfacl -m g:HR:rwx  Employee_Data/
setfacl -m g:Management:rwx  Employee_Data/

Company Vision and Mission Statement – HR and Management
setfacl -m g:HR:rwx  Company_Vision_and_Mission_Statement/
setfacl -m g:Management:rwx  Company_Vision_and_Mission_Statement/

Server Configuration Script – System_Admin, IT_Intern, and Management
setfacl -m g:System_Admin:rwx  Server_Configuration_Script/
setfacl -m g:IT_Intern:rwx  Server_Configuration_Script/
setfacl -m g:Management:rwx  Server_Configuration_Script/

![Screenshot (100)](https://github.com/user-attachments/assets/1aa5c595-8868-4840-8e22-3f058f424dc7)

## Step 6: Set the right Permission using chmod (change mode) command and use getfacl directory name/ to view permission

chmod 770  Finance_Budgets/

![Screenshot (104)](https://github.com/user-attachments/assets/6411f569-609d-45b6-beed-741297c249c9)

chmod 770 Company_Vision_and_Mission_Statement/

![Screenshot (107)](https://github.com/user-attachments/assets/a17030b0-98c4-4a31-95f8-53ca8b47eb10)

chmod 770 Server_Configuration_Scripts/

![Screenshot (106)](https://github.com/user-attachments/assets/0c0e24d0-0121-4779-a20c-730cac2dc472)

chmod 770  Contract_Documents/
![Screenshot (108)](https://github.com/user-attachments/assets/eca31a78-2a3e-4a9a-b2b1-841050b60a23)

chmod 770  Business_Projection/
![Screenshot (109)](https://github.com/user-attachments/assets/f5719f97-75d7-4b01-9488-675963146275)

chmod 770 Business_Models/
![Screenshot (110)](https://github.com/user-attachments/assets/07b95e3c-6c58-45ae-8cac-2942494bfba9)

chmod 770 Employee_Data/

![Screenshot (111)](https://github.com/user-attachments/assets/263b4eaa-dbe1-4e77-b4a9-60b4037f8f0d)


