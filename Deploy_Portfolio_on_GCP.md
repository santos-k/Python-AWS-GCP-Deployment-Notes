# Deploy Portfolio Application on GCP using Dockerfile
## Requirements:
1. Application Files
    1. `app.py` python main file
    2. `helper.py` another python used in `app.py` main file 
    3. `Dockerfile` file container initialization
    4. `requirements.txt` list of all required packages used in `app.py`
    v. `assests` directory having all other recources used in application
2. GCP Project Setup 
    1. Login in to [GCP Console](https://console.cloud.google.com/), select a project or create new on and copy the `project_id`
        - To create New Project go to `Menu > IAM & Admin > Manage Resources > Create New Project` 
     
        ![image](https://user-images.githubusercontent.com/40932902/209061819-1fde555e-edd0-4298-b9cc-ccce6635287c.png)
        
        - Enter the Project Name and click Create and Click on Select Project after Successful creation 
        
        ![image](https://user-images.githubusercontent.com/40932902/209061972-e2cce137-f788-43b8-bd8b-d994a7901ddd.png)![image](https://user-images.githubusercontent.com/40932902/209062166-48d5441c-2df3-4c41-a3b0-b3b5abab72c8.png)
        
        - Now, Click on GCP Logo to go on Project Home Page and then Copy the Porject_id 
      
        ![image](https://user-images.githubusercontent.com/40932902/209062287-4ba0f00f-20e2-45c5-8c21-536c340d2f24.png)    
3. Upload application code and files to GCP server
    1. Open `Google Coud SDK Shell` 
   
     ![image](https://user-images.githubusercontent.com/40932902/209063663-0da55845-f205-437e-92ba-5b2d95a9b91e.png)
     
    2. Go to the application directory

      ![image](https://user-images.githubusercontent.com/40932902/209063983-8b01ef34-dd7c-4cfc-80bd-be580d766d67.png)
    
    3. Upload code to GCP, run below command, it will upload the file and execute all steps written in Dockerfile
        ```
        gcloud builds submit --tag gcr.io/project_id/project_id --project=project_id
        
        gcloud builds submit --tag gcr.io/santosh-portfolio-372405/santosh-portfolio-372405 --project=santosh-portfolio-372405
        ```
        
        ![image](https://user-images.githubusercontent.com/40932902/209066175-dea7725e-282b-490a-9cb8-660c2690fab4.png)
        ![image](https://user-images.githubusercontent.com/40932902/209066224-8618c8a9-d157-4e54-a828-abfbb230ef61.png)
        
        Performing all steps mentioned in  `Dockerfile` ![image](https://user-images.githubusercontent.com/40932902/209066412-76a5ad36-5464-4a6c-8711-0e4d10e0b278.png)
        ![image](https://user-images.githubusercontent.com/40932902/209066495-acee71f6-b137-4372-bd44-8ea92addbc8b.png)
        
        Successfully project build on GCP now, ready to deploy![image](https://user-images.githubusercontent.com/40932902/209066651-5585b1e7-bce4-432e-8d10-6d32a44bbde5.png)
    
    4. Now, Deploy the project and get the running server link
        ``` 
          gcloud run deploy --image gcr.io/project_id/project_id --platform=managed --project=project_id --allow-unauthenticated
          gcloud run deploy --image gcr.io/santosh-portfolio-372405/santosh-portfolio-372405 --platform=managed --project=santosh-portfolio-372405 --allow-unauthenticated
        ```
        - Run the above command, it will ask for Service name press enter keep it default
        ![image](https://user-images.githubusercontent.com/40932902/209067233-183cdbc9-295e-4e8e-a588-0f473da6adbc.png)
        
        - now, enter y to proceed ![image](https://user-images.githubusercontent.com/40932902/209067354-d8ab31f6-1b25-4ce3-b374-452aa814dd39.png)
       
       - Now, it will ask for region selection enter any region no. ![image](https://user-images.githubusercontent.com/40932902/209067456-53eab446-b8e0-4e1e-a805-20b86e87e679.png)
       ![image](https://user-images.githubusercontent.com/40932902/209067497-443728f8-8321-4cb2-98fa-e2cdd963b571.png)
       
       - Deployment in process 
          ![image](https://user-images.githubusercontent.com/40932902/209067589-a93d3c3b-4b93-4fdc-9ef3-cbd1fcdb9303.png)
       - Successfully deployed, copy this service url or ctrl+click to open in browser https://santosh-portfolio-372405-6xffi4kvea-em.a.run.app/
        ![image](https://user-images.githubusercontent.com/40932902/209068055-c9ad1db5-437b-41b1-84d6-94bbb48f41ab.png)
        ![image](https://user-images.githubusercontent.com/40932902/209068355-664cb009-afca-421e-9913-881ce77249a7.png)


