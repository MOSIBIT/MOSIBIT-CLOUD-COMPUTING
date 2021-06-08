# MOSIBIT-CLOUD-COMPUTING
Cloud Computing developmet for Mobile SIBI Translator Mobile App. 

## Deployment
Requirements:
- Tensorflow 2.2.0
- Numpy 1.20.3 
- Pandas 1.2.4
- Flask 2.0.1

Cloud Computing path responsible for deploying the ML model. All the code and model are provided by Machine Learning Path. 

![Screenshot 2021-06-06 120655](https://user-images.githubusercontent.com/79360300/121175369-2ca2bb80-c885-11eb-8f3d-b2fa042995b5.jpg)


We use 1 Virtual Machine to deployment, here are the spesification:
- Name              : test-deploy-sibi-translator 
- Machine type      : n1-standard-1 (1 vCPU 3,75 GB RAM)
- Image             : Debian-10-buster-v20210512 (10 GB)
- Network           : default
- Firewall rules    : allw port 80 and 22

Our server is vulnerable because we only have 1 VM to serve the API. We planned to design a load balancer with 3 n1-standard-1 instances. 


## ML API 
![Plan_A_Prediction_Implementation](https://user-images.githubusercontent.com/79360300/121163761-41795200-c879-11eb-893d-82856599a2d4.jpg)
We use Flask as micro web framework. Flask written in Python. We use it because simple, extensible, and flexible. The API can be accessed through http://34.101.121.113:80/ . To perform prediction go to '/predict' route. 

Mobile App will send json file consist of hand coordinate to API. The server will do the machine learning to predict the alphabet. The API will return hand coordinate and aplphabet prediction in json file. 
