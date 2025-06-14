# MicroServicesNew
This application follows the microservice architecture to implement an order and inventory system. It simulates the function
of an online shopping application, although it is a light weight mini version. It uses Web Client as the protocol for 
communication between services.

## Features
- Product Service
> It contains functions for creating, updating, removing and getting all products from database.
- Order Service
> contains the function for making the order of a product. It first verifies the availability of the product
> by making an asynchronous call to the inventory service using web client.
- Inventory Service
> It contains the isInStock method that takes in an inventory code as a parameter and checks if the requested product is in stock.

### Tech Stack
-Spring boot
- java
- web client
> Web client is a protocol that allows applications to talk to each other just like the httpClient protocol.
> but unlike the httpClient protocol, webclient has asynchronous non-blocking, which makes communication between
> services faster because subsequent requests do not need to wait for the completion of the previous request.
- microservices
> Microservices is a design architecture that is more of splitting the application responsibility into various problems.
> Each problem is then tackled separately in a single service. These services are called microservices. They can then 
> talk to each other to pass necessary information among themselves to fulfil a purpose. Microservice architecture
> allows various implementation strategies to increases scalability and handle robustness in heavy application.