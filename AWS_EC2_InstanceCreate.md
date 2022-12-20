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

 

