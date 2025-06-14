# MicroServicesNew Update
This application follows the microservice architecture to implement an order and inventory system. It simulates the function
of an online shopping application, although it is a light weight mini version. It uses Http Client as the protocol 
for communication between services. It also includes service discovery, api gateway and circuit breaking 
functionalities using Spring-Cloud-Starter-Netflix-Eureka, Spring-Cloud-Starter-Gateway and resilience4j.

## Features
- Product Service
> It contains functions for creating, updating, removing and getting all products from database.
- Order Service
> contains the function for making the order of a product. It first verifies the availability of the product
> by making an asynchronous call to the inventory service using web client.
- Inventory Service
> It contains the isInStock method that takes in an inventory code as a parameter and checks if the requested product is in stock.

### Tech Stack
- Spring boot
- java
- Service discover
- Spring-Cloud-Starter-Gateway
> For channelling all api endpoints through a single api gateway
- Spring-Cloud-Starter-Netflix-Eureka
> For discovering live and running services
- Resilience4j
> Controls what should happen when the service being called is down
> Controls what should happen when the service being called is responding slowly due to database issues or poor network.
> Controls when and how many times the application should retry sending or retrieving a request if there is no response.
> Sets time out limits for api calls
- HttpClient
> http client is a protocol that allows services to talk to each other.
> but unlike the web Client protocol, http client does not support asynchronous non-blocking, which makes communication between
> services slower because subsequent requests need to wait for the completion of the previous request.
- microservice
> Microservices is a design architecture that is more of splitting the application responsibility into various problems.
> Each problem is then tackled separately in a single service. These services are called microservices. They can then 
> talk to each other to pass necessary information among themselves to fulfil a purpose. Microservice architecture
> allows various implementation strategies to increases scalability and handle robustness in heavy application.