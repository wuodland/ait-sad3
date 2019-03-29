# AIT Software Architecture Design, Assignment 3

### Team-members and Responsibilities:
* Karan Raj Baruah, 119967 <br/>
Configured docker, server, firewall configuration and implemented serverless architecture.
* Abdulrahman Safi, 119799 <br/>
Implementation of microservices (order product)
* Abhinav Singha, 120278 <br/>
 Implementation of microservices (user)
<br/>


**The third party microservice we used is “Google OAuth” for authentication. **

**Oauth:** <br/>
OAuth is an open-standard authorization protocol or framework that describes how unrelated servers and services can safely allow authenticated access to their assets without actually sharing the initial, related, single logon credential. In authentication parlance, this is known as secure, third-party, user-agent, delegated authorization.
We use it for login in our application

**Describe your own microservice and why you made it**

The microservice we made is sort of an online store where admin is able to list the products for sale and users can add the products to cart and proceed to buy.
We made this as this is a widely used concept and seemed to be a nice idea for a microservice.

**Describe your usage of serverless technology**

We used AWS (EC2 micro instance) for deployment of the docker images. AWS + docker usage means we can scale our system in the future when the number of users rise.
http://18.220.212.251/ is the url where it is running.


**Describe your implementation briefly (best with sample code snippets)** <br/>
We have split the various microservices into separate docker images and have deployed them on the Amazon EC2 instance. There are total of 7 containers with frontent being the main gateway.
<br/>
Following are some of the snippets: <br/>
 ![Link to Diagram](https://i.imgur.com/V3hVurY.jpg)
<br/>
![Link to Diagram](https://i.imgur.com/F1Z00e1.jpg)


**A diagrams/graphs explaining the architecture of the whole app** <br/>

 ![Link to Diagram](https://i.imgur.com/4m6WRFw.jpg)




**Discuss the pros/cons of microservice and serverless technology in your own words** <br/>

**Severless** <br/>

Pros:

- No server management is necessary
- Developers are only charged for the server space they use, reducing cost
- Serverless architectures are inherently scalable
- Quick deployments and updates are possible
- Code can run closer to the end user, decreasing latency
<br/>

Cons:

- Testing and debugging become more challenging
- Serverless computing introduces new security concerns
- Serverless architectures are not built for long-running processes

<br/>


**Microservices**

Pros:
- Increased resilience as all the services are separated and no single point of failure.
- Improved scalability
- The ability to use the right tool for the right task
- Faster time to market

<br/>

Cons:

- Robust monitoring is a must
- You must embrace devops culture
- Testing can be complex
- You need to design with failure in mind

