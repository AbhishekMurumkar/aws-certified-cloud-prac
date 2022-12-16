## this is the real reason for using the cloud services and where you can see the real power of the cloud
---
## Scalability -- systam able to handle heavy work loads.

There are 2 types of scalability

1. Vertical Scalability(=scale up/down) -- upgrade the version / capacity of the hardware resource (mostly used in databases)
2. Horizontal Scalability (=elasticity =scale out/in) -- increase the number of instances present as per load we get. This is the case where we get distributed systems (mostly used for web applications). In order to achive we this we will use
   1. **Load Balancer**
   2. **Auto scaling groups**

## Availability

generatlly High availability is achieved when

1. when we have atleast app deplyed in 2 AZ
2. goes in hand with horizontal scaling
3. Autoscaling groups in multiple AZ
---

# <center> Load Balancing
An intermediate server that shares/controls the incoming of traffic and redirects them to proper ec2 instances to complete the request allowing to balance the load given over these instances. This allows us

1. have single DNS for our application
2. handle failres of ec2 instances
3. do health checks on ec2 instances
4. provide SSL for your website
5. high availability across AZ
THis will be publicly exposed over the internet where as the EC2 instances will be hold private in the cloud while using load balancer

![](2022-10-30-13-34-40.png)

# <center> Elatic Load Balancer

* Managed by AWS, means it is responsible of AWS people to keep it running and its updates, maintainance.


AWS offers 3 kind of Load Balancers
1. Application Load balancer -- works on Layer 7 = HTTP/HTTPS
2. Network Load Balancer -- works on Layer 4 = TCP 
   * ## has ultra high performance load balancer which is capable of handling millions of requests per second
   * best suited for gaming servers,  
3. Gateway Load Balancer -- majorly used to redirect traffic to security tools then to the ec2 instances
4. Classical Load Balancer (OLD & will be removed soon) -- works on Layer 4,7

# <center> Auto Scaling Groups

* service mainly used to create or destroy the ec2 instances automatically based on the traffic / workload present, that is 
   * Scale out when there are many requests are preset to match load
   * Scale in when there are idle resources
* Hence in this service, the newly created ec2 instances are registered/de-registered into load balancer automatically
* This can also be used to replace un-healthy instances to a new ones
* This allows us to have huge cost savings option

## Scaling Stragtegies

![](2022-10-30-14-14-46.png)
![](2022-10-30-14-14-57.png)

## Summary
![](2022-10-30-14-16-32.png)