# AWS ElasticbeanStalk
## Steps to deploy:
1. Login to [AWS Console](https://us-east-1.console.aws.amazon.com/elasticbeanstalk/home?region=us-east-1#/gettingStarted)
2. Search `Elastic BeanStalk` and open it
    
    ![image](https://user-images.githubusercontent.com/40932902/213845614-077deeff-8ea8-4fc7-8b6f-233a02528517.png)

3. Create Application 

    ![image](https://user-images.githubusercontent.com/40932902/213845646-edd2cb45-f539-4a75-9ef1-aee7eab4ecfd.png)

4. Enter basic app details
    ![image](https://user-images.githubusercontent.com/40932902/213845665-e9f30bc2-04e5-4159-8f39-d9d73d2dfcd4.png)
    ![image](https://user-images.githubusercontent.com/40932902/213845679-c3abbb80-2993-43d1-b490-c024b5edaa91.png)
    ![image](https://user-images.githubusercontent.com/40932902/213845697-91bb924b-7cde-44fd-8c28-e7fec36b2e7e.png)
    ![image](https://user-images.githubusercontent.com/40932902/213845713-9ad05331-9734-416c-9070-495b5be26b3d.png)

## Prepare Project File
- All files should be in a .zip file
- App.zip
  -  .ebextentions/
      - app.config
          ```
          option_settings:
            "aws:elasticbeanstalk:container:python":
                WSGIPath: app:app
          ```
  - requirements.txt
  - app.py
  - static/
  - templates/

![image](https://user-images.githubusercontent.com/40932902/213845758-f9cee614-0188-4dda-823a-8ab19b86f688.png)
![image](https://user-images.githubusercontent.com/40932902/213845772-074f0192-bf27-4377-95c5-22beef8d8682.png)
![image](https://user-images.githubusercontent.com/40932902/213845778-1732393d-9ed3-4d53-8c5c-6b9f59918926.png)
![image](https://user-images.githubusercontent.com/40932902/213845790-293eda91-4174-4156-bd77-8c267316a7ec.png)
![image](https://user-images.githubusercontent.com/40932902/213845896-df4b3af2-039c-4884-bdad-1fda94a4604b.png)
![image](https://user-images.githubusercontent.com/40932902/213845959-a177842a-add7-4b52-b368-4d4c2a085cac.png)
# Something went wrong
![image](https://user-images.githubusercontent.com/40932902/213846658-240c387b-e1a7-497e-a20d-5083bd0ced0c.png)
