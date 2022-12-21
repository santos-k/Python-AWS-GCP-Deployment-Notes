# Google Cloud Platform Deployment
### Deploying a simple `Hello World!!` Dash application on GCP

## Let's Setup Dash Application first
   - For this simple project we required 3 files `app.py` (main program file), `Dockerfile` (Docker container file) and `requirements.txt` (python package requirements)
   
  1. app.py 
      ```
      import dash
      import dash_bootstrap_components as dbc
      from dash import html

      app = dash.Dash(__name__, meta_tags=[{'name': 'viewport', 'content': 'width=device-width, initial-scale=1.0'}])
      server = app.server
      app.title = 'Santosh Portfolio'
      app.layout = dbc.Container([
          html.H2("Hello World!!")
          ], fluid=True)


      if __name__ == '__main__':
          app.run_server(host='0.0.0.0', port=8080)
      ```
      
   2. Dockerfile
      ```
      FROM python:3.10

      ENV APP_HOME /app
      WORKDIR $APP_HOME
      COPY . ./

      RUN pip install -r requirements.txt

      EXPOSE 8080

      CMD python app.py
      ```
      
   3. requirements.txt
      ```
      dash
      dash_bootstrap_components
      ```
      
Now, Let's Setup out project at GCP
1. Login to GCP and Create a Project![image](https://user-images.githubusercontent.com/40932902/208905168-9a85cdc1-51c0-4032-a1b2-1aa9f3d032a1.png)

2. Download GCP SDK CLI and install now open it and change directory to the project location ![image](https://user-images.githubusercontent.com/40932902/208906313-954cce4d-0be0-4fe3-9572-685065933d17.png)

3. Build project on GCP, run this commmand to upload application files to GCP
    `gcloud builds submit --tag gcr.io/project_id/project_id --project=project_id`
    ![image](https://user-images.githubusercontent.com/40932902/208906632-0bc32aa2-62a0-408b-8dd9-300860bb3b22.png)

4. If success message get end of the command means succesfully files uploaded to GCP ![image](https://user-images.githubusercontent.com/40932902/208906826-7f3059ff-a4a6-45e5-be70-f2efac2a6d8c.png)

5. Now, deploy using this command 
    `gcloud run deploy --image gcr.io/project_id/project_id --platform=managed --project=project_id --allow-unauthenticated`![image](https://user-images.githubusercontent.com/40932902/208909288-85042323-cb2e-47ae-a389-70403af7fbe6.png)
    
    - ask for Service name press enter to keep it default and then type y if ask for y/n ![image](https://user-images.githubusercontent.com/40932902/208909308-0f44d7b0-4798-43e5-967d-9e1df290faa3.png)
    
    - enter region no on that server application will deploy ![image](https://user-images.githubusercontent.com/40932902/208909323-da85fa4f-f620-49ef-95bc-b8b8a2428506.png)
    - after execution it will deploy and give deployed url link copy that and open in browser (or Ctrl+right Click) ![image](https://user-images.githubusercontent.com/40932902/208910335-f3369ac0-b77a-4124-89b8-76e6dab21c56.png)
    - Hurrree............ successfully deployed!!!! ![image](https://user-images.githubusercontent.com/40932902/208910600-cac7ae4f-61e2-4a74-89b2-d1faa6548e9e.png)








