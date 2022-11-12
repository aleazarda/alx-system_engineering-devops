## You must be able to explain some specifics about this infrastructure:
  1. For every additional element, why you are adding it
      for security purpose and monitering.
  2. What are firewalls for
      The firewalls are for protecting the network (web servers, anyway) from unwanted and unauthorized users by acting as an intermediary 
      between the internal network and the external network and blocking the incoming traffic matching the aforementioned criteria.
  3. Why is the traffic served over HTTPS
      for encryption the message. The SSL certificate is for encrypting the traffic between the web servers and the external network to prevent 
      man-in-the-middle attacks (MITM) and network sniffers from sniffing the traffic which could expose valuable information. 
      The SSL certs ensure privacy, integrity, and identification.
  4. What monitoring is used for
      for controlling purpose. The monitoring clients are for monitoring the servers and the external network. They analyse the performance
      and operations of the servers, measure the overall health, and alert the administrators if the servers are not performing as expected. 
      The monitoring tool observes the servers and provides key metrics about the servers' operations to the administrators. 
      It automatically tests the accessibility of the servers, measures response time, and alerts for errors such as corrupt/missing files, 
      security vulnerabilities/violations, and many other issues.
  5. How the monitoring tool is collecting data
      by loge file
  6. Explain what to do if you want to monitor your web server QPS
      by telenet 
## You must be able to explain what the issues are with this infrastructure:
  1. Why terminating SSL at the load balancer level is an issue
      Terminating SSL at the load balancer level would leave the traffic between the load balancer and the web servers unencrypted.
  2. Why having only one MySQL server capable of accepting writes is an issue
      Having one MySQL server is an issue because it is not scalable and can act as a single point of failure for the web infrastructure.
  3. Why having servers with all the same components (database, web server and application server) might be a problem
      Having servers with all the same components would make the components contend for resources on the server like CPU, Memory, I/O, etc., 
      which can lead to poor performance and also make it difficult to locate the source of the problem. A setup such as this is not easily scalable.
