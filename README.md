# MOSIBIT-CLOUD-COMPUTING
Cloud Computing developmet for Mobile SIBI Translator Mobile App. 

## Deploy ML API 
Requirements:
- Tensorflow 2.2.0
- Numpy 1.20.3 
- Pandas 1.2.4
- Flask 2.0.1

Cloud Computing path responsible for deploying the ML model. All the code and model are provided by Machine Learniing Path. 
![Plan_A_Prediction_Implementation](https://user-images.githubusercontent.com/79360300/121163761-41795200-c879-11eb-893d-82856599a2d4.jpg)


We use 1 Virtual Machine to deployment, here are the spesification:
- Name              : test-deploy-sibi-translator 
- Machine type      : n1-standard-1 
- Image             : Debian-10-buster-v20210512 (10 GB)

Our server is vulnerable because we only have 1 VM to serve the API. We planned to design a load balancer with 3 n1-standard-1 instances. 
