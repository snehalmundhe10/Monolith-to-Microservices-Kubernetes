#  Refactor Monolith to Microservices
### Overview
This web application allows users to register, log-in and post images to the feed and process photos using image-filtering microservice. This monolith application is refactored into microservices using stragler pattern. The backend API is decomposed into two independent microservices 'feed' and 'users'. The bolier plate code consisted of backend api which was refactored into two independent microservices.

Therefore, the project consists of:-
1. Frontend client: An ionic client which consumes the RESTful backend
2. Backend user api microservice: A node-express backend service which manages the user profiles
3. Backend feed api microservice: A node-express backend service which manages the image feed

### Deployment Procedure
### Containorize applications 
Start with creating dockerfiles for each independent application- frontend, backend user api, backend feed api and reverseproxy.
### Build CICD pipeline
1. Set up the github account to integrate TravisCI.
2. Set up the github repository with.travis.yml for build pipeline to be generated.
### Deploy to kubernetes
1. Create Amazon EKS cluster on AWS
2. Create worker nodes in EKS cluster
3. Bind AWS EKS cluster with kubectl using aws eks --region {region} update-kubeconfig --name {clusterr_name}
4. Create the kubernetes resources for backend feed api, backend user api, frontend and reverseproxy by kubectl apply -f  {service & deployment_filename}.yml
 
### Start app as a container on local system
1. Navigate to Deployment folder --> Docker folder
2. Build the images: docker-compose -f docker-compose-build.yaml build --parallel
3. Push the images: docker-compose -f docker-compose-build.yaml push
4. Run the container: docker-compose up

