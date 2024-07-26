# AWS Projects

## Observability points for AWS VPC

In software engineering, especially in the context of modern distributed computing and microservices, 
the concept of observability has become essential. Observability refers to the ability to gain actionable insights 
into the internal states of distributed systems and microservices, as well as the communication between their components, 
through the collection and analysis of data. This capability is now a crucial part of the daily practice of software engineers.

In AWS cloud computing, before client workloads are exposed to the internet, a trusted network boundary called a 
Virtual Private Cloud (VPC) is required. Amazon VPC provides AWS clients with control over their 
virtual networking environment, including resource placement, connectivity, and security. 
Observability in AWS begins with the VPC, and ends with the resources that a software workload requires to function.

Network traffic within a trusted boundary, such as a Virtual Private Cloud (VPC), is called East-West traffic. 
With outbound workload traffic is referred to as Egress flow, while inbound workload traffic is known as Ingress flow. 
Enabling observability for an AWS VPC requires collecting actionable data from; 

* Ingress.<br> 
* Egress.<br>
* East-West traffic.<br>


#### VPC Flow Logs:

##### What it is: 
VPC Flow Logs capture information about the IP traffic going to and from network interfaces in your VPC.

##### Uses: 
Diagnose connectivity issues, monitor network traffic, and troubleshoot security group and network ACL rules.

##### Metrics: 
Source/destination IP, source/destination port, protocol, action (accept/reject), and log status.

#### AWS CloudTrail:

##### What it is: 
CloudTrail records API calls made within your AWS account, including those to VPC.
##### Uses: 
Track changes to VPC configurations, audit access and actions, and ensure compliance.
##### Metrics: 
Details of API calls, including the caller identity, time, source IP, request parameters, and response elements.

#### Amazon CloudWatch:

##### What it is: 
CloudWatch collects monitoring and operational data in the form of logs, metrics, and events.
##### Uses: 
Monitor VPC components, set alarms, and visualize logs and metrics.
##### Metrics: 
Network-related metrics such as BytesIn/BytesOut, PacketsIn/PacketsOut for NAT Gateways, Transit Gateway, and other network components.

#### AWS Config:

##### What it is: 
AWS Config tracks the configuration changes of your AWS resources.
##### Uses: 
Monitor configuration changes, maintain resource configurations, and audit resource compliance.
##### Metrics: 
Configuration history and compliance status of VPC resources like subnets, route tables, and security groups.

#### AWS Trusted Advisor:

##### What it is: 
Trusted Advisor provides real-time guidance to help you provision your resources following AWS best practices.
##### Uses: 
Optimize VPC security, fault tolerance, and performance.
##### Metrics: 
Recommendations on security group settings, exposed ports, and redundant routes.

#### AWS Network Firewall Logging:

##### What it is: 
Logs traffic that passes through AWS Network Firewall.
##### Uses: 
Monitor and troubleshoot firewall rules, gain insights into allowed and blocked traffic.
##### Metrics: 
Logs for alert, flow, and stateful rule groups indicating allowed/denied traffic and matches on rules.

#### AWS Elastic Load Balancer (ELB) Access Logs:

##### What it is: 

Capture detailed information about requests sent to your load balancer.
##### Uses: 
Analyze traffic patterns troubleshoot issues, and audit requests.
##### Metrics: 
Details like request timeclient IP, request path, and server responses.

##### Amazon Route 53 Resolver Query Logs:

##### What it is: 
Log DNS queries that Route 53 Resolver receives.
##### Uses: 
Troubleshoot DNS issues, monitor DNS query patterns, and enhance security.
##### Metrics: 
Details of DNS queries including query name, response, and the resolver that processed the query.
