
# here you will see a cloud project i did where the example request from management was to deploy a PoC web application to see if the software can be modernized from a monolithic to a micro-services architecture runtime tool. The runtime tool choice for most is docker and that is what i used here for this project. 

# the proccess starts in vs code where use a python web application for the test deployment. Look under the app/ directory to find the dockerfile where i have coded in python to make the docker config file.

# as we wanted to use this proccess in a serverless envirorment after i finished the config file i ran the rast of the operations via google cloud shell. I made a zip file of the /app directory folder and after imported into google cloud shell. after unzipping folder and moving into the app directory i created a test container with the following command: docker container run --name apptest01 -p 5000:5000 app:1.0

# after creating the container from the image locally in google cloud shell, the next step for me was to push my changes to the container registery google cloud service.

# once bringing the image and containers to the container registery, the next step was to deploy to cloud run for our python application to be accessible via google cloud.

# After configuration of container image my web application is now accessible via cloud and the was in a matter of seconds to get this done. 

# Web applicastion can use a microservice architecture and using docker as our runtimetool.

# Link of success for my container registery -  https://app-ssxqaotyqa-uc.a.run.app