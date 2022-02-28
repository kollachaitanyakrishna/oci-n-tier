# oci-n-tier
Oracle as a cloud provider is ready to provide the different VM shapes and sizes that can fit any 3-tier and n-tier architectures. 

![image](https://user-images.githubusercontent.com/64516009/156035429-c344e989-a18b-4e04-991b-3169ccce23b6.png)

This is a best practice for a client-server application software design pattern. Suggested by different communities to ease software development, deployment and address the scalability problem. 

A 3-tier architecture would logically break an application in three layers as
A)	Presentation tier
B)	Application tier
C)	Database tier

#Presentation tier: 
It is a front-end for a customer to access the application using GUI (graphical user interface) like web browser, applications, mobile interface. To build these interfaces, the most used are 
1)	Web technologies built on HTML, JS, CSS etc…
2)	GUI interfaces build on java, .net etc…


#Business logic should not be part of this layer, The presentation layer communicates with application layer. Hosted on any web servers like IIS, WebLogic, NodeJS etc.… Since this layer is in public facing subnet, securing this layer would help the customer from the most common malware, virus, denial of service attacks etc.

#Application tier:
Every request from presentation layer would communicate with this layer. Business logic and specific set of rules is part of logic layer. Host layer in a distribute servers, any issues in the layer can be deployed without downtime of the presentation and database layers by adding the auto-scale, routing strategy at load balancers. This layer is developed by using different language like java, .net, python, ruby etc.

#Data tier:
A storage layer with RDBMS like oracle, mysql, sql server etc. Best way to implement as master – slave with multiple regions to store the data.

This can be achieved with multiple cloud providers like oracle, aws, azure, gcp. Below is the implementation in different clouds.


