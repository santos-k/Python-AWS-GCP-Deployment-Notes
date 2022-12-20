# Deploy Python Project on AWS
<!-- ![image](https://user-images.githubusercontent.com/40932902/208615937-e84fbb58-aeb6-4d1b-b8d8-9c3e3a0242e9.png) -->

# Steps
1. Signin to AWS usning rootuser credentials: https://aws.amazon.com/
  after login screen 
 ![image](https://user-images.githubusercontent.com/40932902/208617302-bd7035a5-3f9c-42c5-be0d-bb565bf930fc.png)
2. We will use EC2 Serive `Amazon Elastic Compute Cloud (Amazon EC2) provides scalable computing capacity in the Amazon Web Services (AWS) Cloud. Using Amazon EC2 eliminates your need to invest in hardware up front, so you can develop and deploy applications faster.`
  EC2 is kind of Virtual Machine where we can install any operating system and perform any activity on top of it.
  Other alternatives in AWS such as Lambda, Elastic Beanstalk and there are some separate platform also available in AWS for machine learning projects as well
3. Go to EC2 (Services > EC2 or search EC2 in search bar)
 ![image](https://user-images.githubusercontent.com/40932902/208619053-6ec4a0a6-9791-4ac2-98a8-5f139b7d33d2.png)
 Clikc on Instances and check running instances
 ![image](https://user-images.githubusercontent.com/40932902/208619145-bb8a94f3-a9a7-4efc-8f4b-1a11dd446266.png)
 One already running instance in my account
 ![image](https://user-images.githubusercontent.com/40932902/208619476-82f62c5e-1d81-46fb-a2d3-4bf16b46d725.png)

 ## Create New Instance
 1. Click on Launch Instances
    ![image](https://user-images.githubusercontent.com/40932902/208620140-d868c3bc-1c01-4766-b29f-ac0683b02225.png)
 2. Give Name
    ![image](https://user-images.githubusercontent.com/40932902/208620354-27a85646-0966-4a35-8fc7-e2fc3182d7d9.png)
 3. Select OS, here we can install any OS in our instance, we will use Ubuntu
    ![image](https://user-images.githubusercontent.com/40932902/208620990-838668ef-1a54-4d38-a921-38b2ab9d437d.png)
    ![image](https://user-images.githubusercontent.com/40932902/208621307-f5900b9f-6194-4007-b9fb-9731173a563f.png)
4. Select Instane Type: very important step, if you wan to use for free, then only select `free tires eligible` type else you will have to pay for your service
    ![image](https://user-images.githubusercontent.com/40932902/208626936-a749a83f-92d9-4f1c-9a6e-45163bf0a16a.png)
5. Create a Key Pair for access this instance outside
  ![image](https://user-images.githubusercontent.com/40932902/208627323-5540e931-a039-428d-a517-f0c19620ec0f.png)

  - Click on `Create new Key pair`, give relatable key any name and click `Create key pair` a `.pem` file will be downlaoded keep it safe and private, without this key cannot be loggedin into this instance.
  ![image](https://user-images.githubusercontent.com/40932902/208627580-72f4518b-4a57-49b8-84b1-2f5eecae8e7a.png)
  ![image](https://user-images.githubusercontent.com/40932902/208627646-cfd5ac17-f7e0-434b-a873-994cd9be208f.png)
6. Network Settings: Keep this default
  ![image](https://user-images.githubusercontent.com/40932902/208628553-395df57b-3649-4b0c-b302-c92f085298f9.png)
7. Configure Storage: this is the C drive storage, select as per required, free account only get 30gb per account
    here we selecting 8GB C drive storage.
  ![image](https://user-images.githubusercontent.com/40932902/208629105-6b26a73a-53c7-4b20-beed-d41f02faf26d.png)
  
 8. Done with basic configuration, now click on `Launch Instance`
    ![image](https://user-images.githubusercontent.com/40932902/208629410-3ca2c010-e860-4aa5-adb9-2597a9aa8f1e.png)
 9. Launching Status: 
      ![image](https://user-images.githubusercontent.com/40932902/208629503-7931346f-2242-492c-8944-3934a7e8776c.png)
      ![image](https://user-images.githubusercontent.com/40932902/208629571-4bcfe2f8-994f-4b0c-8a43-dc713e8f1e79.png)
10. Check Created Instance
    Click on Instances, remove filter if any applies, all instaces will display
      ![image](https://user-images.githubusercontent.com/40932902/208629989-e19c36b6-2afc-451b-9fc1-d4fb73fb4a53.png)
  Click on `Instance id` to check the full details
  ![image](https://user-images.githubusercontent.com/40932902/208630402-8e778067-2a8a-4a84-ac1f-db2d71be358e.png)

# Communicate with EC2 Instance 
- We can communicate using any terminal like windows cms, linux terminal, gitbash terminal, putty etc...
### Now, we are ready to communicate our Machine
1. Click on Instance Id ![image](https://user-images.githubusercontent.com/40932902/208632931-58684707-27c7-40bf-86ae-87eb5f6e9003.png)
2. Click on `Connect` ![image](https://user-images.githubusercontent.com/40932902/208633092-725bbc38-c46b-48c1-ba09-9620cb2226e9.png)
3. Go to `SSH Client` and copy the example command ![image](https://user-images.githubusercontent.com/40932902/208633432-1c3019d4-d9e6-40c0-964f-4c5d72e019be.png)
4. Now, go to local system where login key has been downloaded or move that key to any specific folder then open `CMD` at the specific folder
# Connect to instance
## 1. Connect Our Instance using `Windows CMD`(SSH client supported)
   - now open cmd in key folder ![image](https://user-images.githubusercontent.com/40932902/208634718-4b7652bf-b010-409d-8cb8-68e56afa601a.png)
   - now paste the copied command in cmd and press enter ![image](https://user-images.githubusercontent.com/40932902/208635023-25b9bca9-7e3d-4a8b-8f3a-10f484f02672.png)
   - Now, type `yes` and press enter.... bingooo!! we are not connected to our instance![image](https://user-images.githubusercontent.com/40932902/208635244-4b5fe795-a147-48c6-84cf-a0c30d029c06.png)

## 2. We cannot connect our instance using windows cmd if does not support ssh communication, for that we can use below methods
## A. Connect Our Instace using `GitBash`, download and install gitbash for windows
   - open gitbash terminal and change directory where key is present ![image](https://user-images.githubusercontent.com/40932902/208640771-aae7c8ed-3bd0-483c-b63a-47846f527054.png)
   - Paste the same command and press enter ![image](https://user-images.githubusercontent.com/40932902/208641041-df4ef9ef-df4e-4392-bdd4-fc3e7db321b4.png)
connected to instance ![image](https://user-images.githubusercontent.com/40932902/208645509-8eb7e579-be43-4889-b5b1-03aad8538f0e.png)

## B. We can connect using Putty https://www.putty.org/
 
## Let's Run some command to check our AWS Machine (below cmds will work windows as well as linux)
1. Check the OS, `cmd:  cat /etc/os-release`, is that the same as we configured while creating instance ![image](https://user-images.githubusercontent.com/40932902/208636071-f1090df9-2746-43ea-a364-e81db45016a0.png)
2. Let's Check RAM details `cmd: free -m` we have selected 1gb ![image](https://user-images.githubusercontent.com/40932902/208636384-9ab496fe-604c-47cb-a44a-7aa2b7c109a1.png)
3. Check CPU details `cmd: lscpu` selected 1 CPU ![image](https://user-images.githubusercontent.com/40932902/208636641-d049b9b2-0ae0-4506-acae-e23e4ab9a61f.png)
4. Check Storage Capacity `cmd: df -h` ![image](https://user-images.githubusercontent.com/40932902/208637257-1df59fce-a20e-49a6-98c9-878e08164158.png)
![image](https://user-images.githubusercontent.com/40932902/208637675-fb45f667-78e0-4f1b-8076-89a86d36f76e.png)
5. Check Ip details `cmd: ip a` ![image](https://user-images.githubusercontent.com/40932902/208638019-3b27da57-b83e-4261-894e-159c7db103a7.png)
![image](https://user-images.githubusercontent.com/40932902/208638094-44ae9b8b-8445-4032-a423-239892c4786f.png)

#### We establised communication with EC2 instance using terminals, now we need to upload our program files to AWS machine
- To upload external file to AWS machine we need a software called WinSCP https://winscp.net/eng/index.php

## Setup WinSCP
1. Download and install WinSCP
2. Open WinSCP ![image](https://user-images.githubusercontent.com/40932902/208659012-cda2896c-95b0-4618-8563-e3e60f2c901c.png)
3. To connect we need some details `Hostname`, `username` and `password` of our EC2 machine
    - Find `Hostname` of EC2 instance, go to instance page > connect > SSH client![image](https://user-images.githubusercontent.com/40932902/208659764-092b3b82-b1d3-49f2-9f16-0cbbbc32a264.png)
    - to Find `Uername` : Instance > EC2 Instance Connect ![image](https://user-images.githubusercontent.com/40932902/208660193-6025fa47-eb18-47c1-ab38-a1a813093246.png)
    - `Password` we have already `.pem` file as password
 4. Enter the Hostname and Username ![image](https://user-images.githubusercontent.com/40932902/208660655-a66f2e07-7b2d-411a-afd2-3b53877ead4f.png)
 5. To enter the password winscp required `.ppk` format instead of `.pem`, click on `Advanced`![image](https://user-images.githubusercontent.com/40932902/208660894-22ff3901-2b39-4083-abae-e841c11074e8.png)
 6. Select SSH > Authentication and then select private key file `.pem`![image](https://user-images.githubusercontent.com/40932902/208661363-1341d28b-cd68-4e7f-8445-06288112e54f.png)
 7. if `.pem` file not visible while selecting then change the file type to `All File (.)` in file explorer window then select that ![image](https://user-images.githubusercontent.com/40932902/208661696-885e5979-4575-4688-9d43-4cfd81e022c9.png)
 8. It will ask to change file type to putty, click yes and then will ask to save new `.ppk` file, allow that ![image](https://user-images.githubusercontent.com/40932902/208661943-93f1bb2f-4e36-426c-9bec-3ba1bf62e9b2.png)
 ![image](https://user-images.githubusercontent.com/40932902/208662048-a7fb97df-5f45-4a2c-9603-c1ca5734bc24.png)
![image](https://user-images.githubusercontent.com/40932902/208662090-99802416-297a-4aa9-bc95-9a98a16cd5cd.png)
 9. Now, we are ready to connect![image](https://user-images.githubusercontent.com/40932902/208662163-3f252049-f8c8-4852-be22-f59a08fd8c18.png)
 10. Click ok and Click on Login to connect EC2![image](https://user-images.githubusercontent.com/40932902/208662285-16ed31cb-60b4-43c4-941b-9b930e0c5b8c.png)
 ###### Bingooooooooooo!! we are connected now ![image](https://user-images.githubusercontent.com/40932902/208662724-7592a37a-aeaa-4453-a61a-3d73db4608f5.png)
![image](https://user-images.githubusercontent.com/40932902/208663039-7c93a724-7dd9-4899-81b5-d9b86ec26d60.png)

- We don't have any files in our EC2 machine
- using Winscp we can upload any file from our local machine to ec2 by jusy drag and drop
- uploading a python file to EC2, just select the file you want to upload > right click> upload ![image](https://user-images.githubusercontent.com/40932902/208663816-8da86993-cd2c-4265-bb4a-c99f1d383266.png)
- File uploaded to EC2 ![image](https://user-images.githubusercontent.com/40932902/208663925-f33ac20f-6adf-465d-8912-575bc157b814.png)
- Also we can upload file and folders using drag and drop ![image](https://user-images.githubusercontent.com/40932902/208664175-2176a7cb-1e6d-4ab8-a69a-66319b931f1a.png)
- Check all files uisng terminal `cmd: ls` ![image](https://user-images.githubusercontent.com/40932902/208665765-9841282f-fbba-4226-a90e-9b9a0254e62e.png)


### If we have connected with WinSCP then we donn't need to configure Putty, it's automatically configured
  - To launch Putty click on ![image](https://user-images.githubusercontent.com/40932902/208664962-9ae8a2b3-4ed5-4136-99e7-4a2975c9b2d5.png)
  - Connected easly ![image](https://user-images.githubusercontent.com/40932902/208665032-f492b324-856d-44f6-b6f0-9e71bd3ee97f.png)

# Install Python and packages on EC2 using Putty or any other terminals
- Lets check python comes with ubuntu or not, type `python` and press enter ![image](https://user-images.githubusercontent.com/40932902/208665477-4d563ad0-ed67-46b9-ab58-5254c724ade0.png)
- Let's check for `python3`, so python3 is installed in our ubuntu os ![image](https://user-images.githubusercontent.com/40932902/208666089-5541df1d-61da-4317-b963-7b3d89219aa8.png)
- we can install python using `sudo apt install python3` command if python not installed ![image](https://user-images.githubusercontent.com/40932902/208667092-ea5a14d3-bf89-4c6d-b451-9b9e4f94ac26.png)

- update sedu command `sudo apt update`
- install pip for installing python packages using command `sudo apt install python3-pip`
- installing `numpy` using `pip install numpy` ![image](https://user-images.githubusercontent.com/40932902/208668343-c120ffc9-ab81-4c2d-9903-3aed63f6203d.png)
- installing multiple python package using requirements.txt file at once `pip install -r requirements.txt` ![image](https://user-images.githubusercontent.com/40932902/208669115-ed9f3129-5ca1-49a0-8827-f00126443bcf.png)

## Running Flask webapp in EC2:
![image](https://user-images.githubusercontent.com/40932902/208669367-5c25088c-db98-4e82-ac66-26c7c740e2d4.png)






  




