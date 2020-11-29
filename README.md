#  Refactor Monolith to Microservices
#### Overview
This web application allows users to register, log-in and post images to the feed and process photos using image-filtering microservice. This monolith application is refactored into microservices using stragler pattern. The backend API is decomposed into two independent microservices 'feed' and 'users'.

Therefore, the project consists of:-
1. Frontend client: An ionic client which consumes the RESTful backend
2. Backend user api microservice: A node-express backend service which manages the user profiles
3. Backend feed api microservice: A node-express backend service which manages the image feed

#### Deployment Procedure

