# Create GCP Virtual Machine Instance 
  - similar to AWS EC2 Instance

## First, Create a Project
1. To create Project go to `Menu > IAM & Admin > Manage Resources` ![image](https://user-images.githubusercontent.com/40932902/208935255-cfb10bbe-4cfa-43f6-a72f-8befb8a58a80.png)
2. Click on Create Project button ![image](https://user-images.githubusercontent.com/40932902/208935571-49883fce-112e-453b-8420-38b695175e51.png)
3. Give the Project name and click Next ![image](https://user-images.githubusercontent.com/40932902/208936009-18cff531-d352-44d7-87f3-a68236531703.png)
4. Refresh, project will listed project created successfully ![image](https://user-images.githubusercontent.com/40932902/208936224-07e96323-b5c2-4a1c-a846-e90e2a85df3e.png)

## Now, Create VM Instance
1. Go to Menu > Compute Engine > VM Instances ![image](https://user-images.githubusercontent.com/40932902/208936806-e139e143-de76-47a1-b0ac-6a88c14dd285.png)
2. Make sure Project name selecte top then click on Enable API if ask ![image](https://user-images.githubusercontent.com/40932902/208937098-ebe7954e-f5ce-4b04-9471-3e68caef0c20.png)
3. Create VM Instance ![image](https://user-images.githubusercontent.com/40932902/208937527-b2fb82a2-8846-471e-a257-c8123f919102.png)
#### VM creation begin
  1. ![image](https://user-images.githubusercontent.com/40932902/208940608-a4874d04-e4b0-4991-9ebf-1a5c5b892afd.png)
  2. ![image](https://user-images.githubusercontent.com/40932902/208940777-bc915590-e4bf-4342-98d7-fd7d2214df36.png)
  3. ![image](https://user-images.githubusercontent.com/40932902/208940923-29122610-b054-4681-ab42-6582a0f119b8.png)
  4. ![image](https://user-images.githubusercontent.com/40932902/208941075-d5796361-9f76-4a9f-82c2-6296504d533f.png)
  5. ![image](https://user-images.githubusercontent.com/40932902/208941319-e1fb11d6-6ff1-4f0e-b1b9-390e81d11918.png)
  6. ![image](https://user-images.githubusercontent.com/40932902/208941632-a2b6fe75-2827-4adf-9c5f-26fb847c65d7.png)
  7. ![image](https://user-images.githubusercontent.com/40932902/208941835-b3f07004-5dd3-4900-85a9-89f2af12bbbf.png)
  8. ![image](https://user-images.githubusercontent.com/40932902/208942069-14ec5df3-22c3-40d8-9905-2b470535c026.png)
  9. ![image](https://user-images.githubusercontent.com/40932902/208942118-b0b2241b-caf4-44e3-8a10-5e94cb2bf09e.png)

### Connect VM Instance ![image](https://user-images.githubusercontent.com/40932902/208942251-bdca4fbd-b01a-40e4-8560-c7072977d3c3.png)
1. Connect in Browser: Select first option in COnnect option after it will open new tab![image](https://user-images.githubusercontent.com/40932902/208942725-435ccfcb-59ae-46d7-8bfa-536bf204ea65.png)
   - run some basic commands to check ![image](https://user-images.githubusercontent.com/40932902/208943446-cf6260f1-e1f4-4ca7-8b31-1d84412d3825.png)
## Connect with Putty and WinSCP
### To Connect with WinSCP we need to generate SSH private key first
1. To generate SSH key install PuttyGen, download link https://puttygen.com/download.php?val=49
2. Open PuttyGen and click on generate ![image](https://user-images.githubusercontent.com/40932902/208953616-5a85aed9-88e9-4ec1-93bc-63da90ab8ae8.png)
3. While generating the key move mouse cursor anywhere until it get completed ![image](https://user-images.githubusercontent.com/40932902/208953929-0da64d33-7b69-4f00-87c1-3c6d03d643a7.png)
4. Replace Key Comment value with the gmail id of that GCP account and enter passphrase and confirm like 12345, this passphrase required to connect WinSCP![image](https://user-images.githubusercontent.com/40932902/208954902-106791ec-8292-4c0e-99ea-68913f43b596.png)
5. Now, save this key as once Public and once Private by clicking both `Save Public key` and `Save Private Key` (private key will be .ppk) ![image](https://user-images.githubusercontent.com/40932902/208955780-7f10dce6-7532-42f5-b04e-236e3846d378.png)
6. Now, Copy the entire generate key ![image](https://user-images.githubusercontent.com/40932902/208955737-9992c13a-c47f-4558-b0ec-6fc6c4f77866.png)
7. Go to GCP VM instance Page under `VM Instances` click on Edit ![image](https://user-images.githubusercontent.com/40932902/208956212-232cc90e-f4a4-45b1-8555-5be0889fc13e.png)
8. Delete the existing keys and paste copied key and save it ![image](https://user-images.githubusercontent.com/40932902/208957657-bd464579-fc6f-4a77-9ffb-289429891d63.png)
9. After saving 'username as robinhud299' ![image](https://user-images.githubusercontent.com/40932902/208957902-bed6fbef-a388-4f03-806a-8ceeff426301.png)
10. Now, copy the External IP(Public IP), make sure instance is running else external ip will not visible ![image](https://user-images.githubusercontent.com/40932902/208958430-09d6b298-a21e-4f90-9bd9-dac119a5ee8d.png)

## Connect to WinSCP
1. Launch WinSCP and  Enter Hostname as External Ip and Username as `robinhud299` as created above ![image](https://user-images.githubusercontent.com/40932902/208958817-840ddbb7-5180-489c-b925-3ce776d70df9.png)
2. Skip the Password field and click on Advance button then SSH > Authenticate and select the Private_key .ppk file saved earlier using Puttygen.![image](https://user-images.githubusercontent.com/40932902/208959298-779b397b-bbe5-4f40-85ae-7e8cf08fa5f4.png)
3. Click on `Login` and click Yes if ask anything ![image](https://user-images.githubusercontent.com/40932902/208959479-e9764aa9-977c-4f8b-80bd-2714e376d951.png)
4. Now enter the passphrase `12345` same as enter while generating key ![image](https://user-images.githubusercontent.com/40932902/208959713-237bbd6e-2b65-41e9-a4c4-774eb7a73d4e.png)
5. Yaahoooooooooo!!!! Connected... ![image](https://user-images.githubusercontent.com/40932902/208959867-d16d6f5a-b6cd-4adc-9e37-2d2e41b42275.png)

####  Connect Putty if alrady connected with WinSCP then just click on `Open Session in Putty or Ctrl+P`, it will ask passphrase enter the same
![image](https://user-images.githubusercontent.com/40932902/208960318-747be84b-d3a0-4502-8bb9-575600d19a3d.png)

- Try runnung some commands 
- ![image](https://user-images.githubusercontent.com/40932902/208960841-9f656993-bb5c-46ac-85ad-c23475275c1d.png)
- ![image](https://user-images.githubusercontent.com/40932902/208961036-09464c48-dd71-4eb4-b28a-643973c9a5e4.png)
- ![image](https://user-images.githubusercontent.com/40932902/208961340-10628d98-7802-4861-b72d-745954d4f654.png)

## Run First Application on GCP VM Instance
1. Connect to WinSCP
2. Connect to Putty (Ctrl+P in WinSCP)
3. first update sudo by cmd `sudo apt update`
4. check python installation or version  run `python3`
5. install python using `sudo apt install python3.10`
6. install pip using `sudo apt install python-pip`
7. unistall python2.7 `sudo apt purge -y python2.7-minimal`
8. install pip `sudo apt install python3-pip`
9. install packages from requirements.txt `pip3 install -r requirements.txt`
















