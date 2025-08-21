# Azure-application-gateway

Summary: Deploying Azure Application Gateway for Load Balancing
In this project, I configured Azure Application Gateway to securely route traffic to a web application. The steps include:

Creating a Virtual Network (VNet) with two subnets:
One for the Application Gateway.
One for the Application (VMs hosting the website).
Deploying a Virtual Machine (VM) in the application subnet.
Connecting to the VM via RDP and installing the IIS server to host a dummy website.
Configuring the Application Gateway to route traffic to the IIS server.
Retrieving the Public IP of the Application Gateway to access the hosted website.
This setup enables secure, scalable, and efficient web traffic management using Azure's Layer 7 load balancing. 🚀

Step - 1
i. Create a virtual Network
<img width="1366" height="628" alt="Capture1" src="https://github.com/user-attachments/assets/ab5acc1e-5bde-43c6-8800-5938b18e0a23" />

ii. I have reserved 64 Ip address for the virtual machine and 64 for the application gateway
<img width="1366" height="624" alt="Capture3" src="https://github.com/user-attachments/assets/1a121f60-b9a3-45f3-aefe-3506d372c716" />


iii. Once the virtual Network is done , Lets create a VM , make sure you selected this ports.
<img width="1366" height="616" alt="Capture2" src="https://github.com/user-attachments/assets/5c457233-28ed-4381-816a-b50d7d097b3d" />


iv. Deploy the VM in subnet that you created
<img width="1366" height="626" alt="Capture4" src="https://github.com/user-attachments/assets/30534ec0-8d2d-499a-ac0d-2af9c918eceb" />

Step- 2
i. Connect your VM with the RDP
<img width="894" height="900" alt="5" src="https://github.com/user-attachments/assets/484e1942-ab75-4fbb-87e4-e2a724b01fa2" />


ii. Go into server manager , then click on add roles and features
<img width="1366" height="700" alt="Capture5" src="https://github.com/user-attachments/assets/46215675-fcd3-42e6-ad6f-4aa4cca0c449" />


iii. Install Web Server IIS
<img width="799" height="565" alt="Capture6" src="https://github.com/user-attachments/assets/9504e3c5-3fb2-4254-a7e4-a409f81d8a1a" />


Step - 3
i. Create Application Gateway, select your virtual network then click on Manage subnet configuration
<img width="1366" height="552" alt="Capture7" src="https://github.com/user-attachments/assets/94b16420-a055-4bbc-bab3-c78177f15cff" />
<img width="1366" height="623" alt="Capture8" src="https://github.com/user-attachments/assets/98573d2d-a9c1-4429-aa2f-3c83748c7016" />

ii. Click on + subnet , give the name and the left 64 ip address will be asign to this application gateway
<img width="1366" height="626" alt="Capture9" src="https://github.com/user-attachments/assets/46c3b861-31c6-4ce0-a9ff-7c48fdf697bd" />

iii. Now you can see your subnet is added
<img width="1366" height="624" alt="Capture10" src="https://github.com/user-attachments/assets/112cad0e-f170-4091-b547-7544065a705e" />

iv. Once the basic is configure lets configure the frontends, Just give the public ip name
<img width="1366" height="393" alt="Capture11" src="https://github.com/user-attachments/assets/4c1b4b94-1338-4e41-9393-de61390d4b7f" />

v. In backend , click on Add backend pool then configure as per shown in the image
<img width="1366" height="619" alt="Capture12" src="https://github.com/user-attachments/assets/6ca93b9f-e7d9-42c7-8ebf-aca3735a49f2" />

vi. host a demo webiste on Web server IIS
<img width="1050" height="539" alt="Capture13" src="https://github.com/user-attachments/assets/2ea49dda-fd52-43e4-b8a3-ac862f71c173" />

vii. Lets configure the configuration part
<img width="1366" height="629" alt="Capture14" src="https://github.com/user-attachments/assets/5e7a08a9-b91d-4f6a-9faa-a20cf248dafd" />
<img width="1366" height="626" alt="Capture16" src="https://github.com/user-attachments/assets/05623dba-e103-4a14-980c-7374c81977c1" />
<img width="1366" height="624" alt="Capture15" src="https://github.com/user-attachments/assets/32f716cf-c2aa-473d-bb80-54ae8a4f2376" />
<img width="1366" height="628" alt="Capture17" src="https://github.com/user-attachments/assets/739ff808-3d6c-46b6-b8b1-1a4fdd630566" />
<img width="1366" height="732" alt="Capture18" src="https://github.com/user-attachments/assets/79218d93-3ea7-4e00-ab12-46fee4aa144c" />

















