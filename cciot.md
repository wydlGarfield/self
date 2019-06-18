# Cloud Computing

## 1

### Definition
* Cloud Computing is a model for enabling ubiquitous, convenient and on-demand network access to a shared pool of dynamically configurable computing resources (networks, computing power - servers, storage, applications and services) that can be rapidly provisioned and made available to the business client with minimal management effort and service provider interaction 

### Characteristics
* Measured service
* On-demand self-service
* Broad network access
* Resouce pooling
* Rapid elasticity

### *The Service Model*
* IaaS - Infrastructure as a Service
	* Subscriber: Applications, Data, Runtime, Middleware, O/S
	* Service provider: Vitualization, Servers, Storage, Networking	
* PaaS - Platform as a Service
	* Subscriber: Applications, Data
	* Service provider: Runtime, Middleware, O/S, Vitualization, Servers, Storage, Networking
* SaaS - Software as a Service
	* All are service providers

![](https://pic2.zhimg.com/80/v2-448c8a43cf4e5a19673ff97a10a6fddf_hd.jpg)

### *The Deployment Model*
* Private Cloud -- for single Org
* Public Cloud -- for general Public
* Community Cloud -- for Orgs.w/shard internets

### Applications
* healthcare, education, government;
* energy stems manufacturing industry, 
* transportation systems
* radio and mobile communication networks

## Cloud computing comcepts & technologies

### Virtualisation
* Difinition: a physical computng system into multiple virtual resouces
	* creation of flexible substitutes for actual resources

#### Hypervisor: complete job for virtualisation
Type 1: run directly on the system hardware
Type 2: run on a host operating system that provides virtualization service
![](https://pic2.zhimg.com/80/v2-737ff40498d1fea1a4e5c37b7bfec624_hd.jpg)

#### Full Virtualisation
* completely decouples the VM
* VM requires no modification
* VM not aware it is being virtualised
* hypervisor emulates hardware platform by translating requests to physical hardware *requires processing and limited by guest I/O*

#### Para Virtualisation
* VM is modified to enable communication with hypervisor
* PV aims at improving performance and efficiency of VM
* modified to replace non-virtualisable instructions with hyper-calls hypervisor *increases performance of guest I/O*

#### Harware-assisted Virtualization(HAV)
* reduces the involvement of the host system in managing privilege and address space translation issues
* 
* add additional Ring -1
* OS requests trap to hypervisor without binary translation or paravituralisation
* commands are executed directly to HW via the hypervisor

### load balancing
* Definition: the distribution of workloads across multiple servers to meet application workloads
* high *availablity* and *reliablity*
* makes a pool of servers appear as single server

### Scalability
* for multi-tier applications: e-commerce, B2B. Hard to predict traffic patterns
* **Capacity Planning**: determine right size of each tier
* **Approaches**:
	* Scaling Up(Vertical Scaling): upgrading hardware resources
		* e.g.: increase the ability of individual server
	* Scaling Out(Horizontal Scaling): increasing more same type resources
		* e.g.: increase the amount of individual server
	* Demand Forcasts: traditional approach
* ***Scalability*** is the capability of a system, network, or process to handle a growing amount of work, or its potential to be enlarged in order to accommodate that growth

### Elasticity
**Cloud Elasticity**: the degree to which a system, or aparticular cloud layer, autonomously adapts its capacity to workload over time

#### Difference

|**Scalability**|**Elasticity**|
|:---|:---|
|"Increasing" the capacity to meet the "increasing" workload.|"Increasing or reducing" the capacity to meet the "increasing or reducing" workload.|
|In a scaling environment, the available resources may exceed to meet the "future demands". | In the elastic environment, the available resources match the "current demands" as closely as possible.|
|Scalability adapts only to the "workload increase" by "provisioning" the resources in an "incremental" manner.|Elasticity adapts to both the "workload increase" as well as "workload decrease" by "provisioning and deprovisioning" resources in an "autonomic" manner.
|Increasing workload is served with increasing the power of a single computer resource or with increasing the power by a group of computer resources.|Varying workload is served with dynamic variations in the use of computer resources.
|Scalability enables a corporate to meet expected demands for services with "long-term, strategic needs".|Elasticity enables a corporate to meet unexpected changes in the demand for services with "short-term, tactical needs".
|It is "increasing" the capacity to serve an environment where workload is increasing.This scalability could be "Scaling Up" or "Scaling Out".|It is the ability to "scale up or scale down" the capacity to serve at will.
|To use a simile, "scaling up" is an individual increasing her power to meet the increasing demands, and "scaling out" is building a team to meet the increasing demands.|To use a simile, a film actor increasing or reducing her body weight to meet differing needs of the film industry.

### Deployment Lifecycle
Deployment Design:
* Number of tiers
* Number of servers in each tier
* Compute capacities, memory & storage
* Server interconnection
* Load balancing & replication

Performance Measurement:
* Application workload
* Utillization of servers

Deployment Refinement
* Horiziontal scaling(scale out)
* Vertical scaling(scale up)
* Alternative server inter-connections
* Alternative load balancing & replication

### Replication
Definition: creation and maintenance of multiple copies of data in the cloud


### Monitoring
Metrics
Actions
Statistics

### Software Defined networking(SDN)
Limitation of conventional networks
* complex network devices
* management overhead
* limited scalability

SDN: An attempt to create network architectures that are simpler, inexpensive, scalable, agile and easy to manage

SDN elements:
* centralised network controller
* programmable open APIs
* Standard communication interface(**OpenFlow**)

### MapReduce

#### Definition
a parallel data processing model for processing and analysing massive scale data

#### Scenario
Assume 5 files, contains two columns that is city and corresponding temperature

Find the Maximum temperature for each city
##### Map Task
Break down into five map tasks, where each mapper works on one of the five files and the mapper task goes trhough the data and returns the maximum temperature for each city
##### Reduce Task
All five of these output streams would be fed into the reduce task, which combine the input results and output a single value for each city, producing a final result set.

### Identity & Access Management(IDAM)

Authentication & authorisation of users to provide secure access to cloud resources

* can use Role-based access control
	* user who wants access to Cloud resources has to send data to Admin
	* admin assgins permission and access control policies
	* policies are stored in the user roles and database

### Service Level Agreements(SLA)
**Availability**: Percentage of time the service is guaranteed to be available
**Performance**: Response time, Throughput
**Disaster Recovery**: Mean time to recover
**Problem resolution**: Process to identify problems, support options, resolution expectations
**Security and privacy of data**: Mechanisms for security of data in storage and transmission
 
### Billing
a|b
---|---
Virtual machines| CPU, memory, storage, disk I/O, network I/O|
Network|Network I/O, loadbalancers, DNS, firewall, VPN
Storage|Cloud storage, storage volumes, storage gateway
Data services|Data import/export, data encryption, data backup
Security services|IAM
Support|SLA, fault tolerance
Application services| Queuing services
Deployment and management services| Monitoring service

## 2 Cloud Services and Platforms

### Compute Services
* Definition: provide dynamically scalable compute capacity in the Cloud
* can be provisioned **on-demand** as VMs
* APIs are vary (Java, Python, Go)
* Key features
	* Scalability
	* Flexibility
	* Sucurity
	* Cost Effectiveness

### Storage services
* allow storage of any amount of data at any time from anywhere
* data is organised into **buckets** or **containers** -- storage objects, individual pieces of data
* Key Features
	* Scalability
	* Replication
	* Acceess Policies
	* Encryption
	* Consistency

### Database services
* allow storage of any amount of data at any time from anywhere
* Non-relational DBs: fully managed, derliver seamless and scalability
* Key Features
	* Scalability
	* Reliability
	* Performance
	* Security

### Applications services
* Application runtimes and frameworks
* Queuing services
* E-mail service
* Notification services
* Media services

### Content delivery services
Include Content Delivery Networks
### Analyrics services

### Deployment & management services

### Identify Access Management services

## 3 Cloud Application Design

### Design Consideration

#### Scalability

Scalability is major reason why developers are creating Cloud Apps
##### Consideration
* Loose coupling of Components
	* possible to scale each component independently
* Asynchronous communication
	* possible to add capacity by adding additional servers when load uncreases
* Stateless Design
	* stores state outside componetns allowing scaling apps independently
* Database Choice & Design 
	* affest scalability

#### Reliability & Avalability
REliability - th probability that a Cloud App will perform the intended functions under stated conditions for a specified amound of time
Availability - the probability that a Cloud App will perform a specified function under given conditions at a prescribed time
##### Consideration
* No signle point of failure
* Trigger automated actions on failures
* Graceful degradation
	* components remain availale during failure
* Logging
	* diagnosis and prediction of failure
* Replication
	* multiple copies of data

#### Security
* Securing data at rest
* Securing data in motion -- in transmission
* Authentication & authorisation
* ID & access management
* Key management
* Data integrity
* Auditing

#### Maintenance & Upgrade
* Low costs
* Loosely coupled components
* Logging & triggering automated actions

#### Performance

### Reference Architecture

Load Balancing Tier
Application Tier
Database Tier
Storage Tier
???
### Design Methodologies

#### Service-Oriented Architecture(SOA)

##### Simple Object Access Protocol(SOAP)
* Aprotocal specification ofr exchanging structured information in the implementation of web services in computer networks
* Uses XML informatin set for its message format
* Relies on application layer protocals most notabloy HTTP or SMTP

##### Layers
* Business Systems
* Service Components
* Composite Services
* Orchestrated Business Services
* Presentation Services
* Enterprise Service Bus

#### Cloud Component Model
* Loose coupling
	* Better scalability
	* maintainability easier
	* easy to changw and test
##### Component Design
* Define CCM for Application
* Auto-scaling & performance constraints
* Applies both mobile and web
##### Architecture Design
* Define interactions between application components
* loose coupling(REST comm protocol)
* asynchronous communication(msg queues)
* stateless design(storage of session)
##### Deployment Design
* Assign application components to cloud resources
* componments deployed independent of each other
* easy to migrate app from cloud to another



#### Model-View-Controller(MVC)
* seperates data, logic and interface -- improve maintainability

#### RESTful 
##### RESTful web service:
* A collection of resources which are represented by URIs and have a base URI
* Clients sent requests using methods defined by the HTTP protocol
* Can support various types 
##### Constraints
* Client-server: seperation of concerns
* Stateless: Request cannot assume stored context on server; sessions stored on the client
* Cacheable: clients can reuse cacheable data
* Layered system: each layer cannot see beyond layer
* Uniform interface: method of communication between client and server must be uniform 
* Cond on demand: 

#### Non-Relational | No-SQL databases
No-SQL:
* Better horizontal scaling capability
* Improved perforamnce for BigData
* Less rigourous consistency models
* No ACID(atomicty, consistency, isolation, durability) guarantee
* 
Rationale: high scalability, fault tolerance and availability
Popularity


## 4 Cloud Application Development

### Methodology for IaaS model
CCM
* Component Design
* Architecture Design
* Deployment Design

Benifits
* Improved Application Performance
	* loose couple components
	* communicate asychronously
	* scale up or scale out
* Savings in Design, Testing and Mantainance Time
	* standard components -- saving design time
	* loosely couple components -- saving test time(independent test)
* Reduced Application Cost
	* leveraging scale up or scale out
	* focusing only on componets that limit performance
* Reduced Complexity
	* simple design
	* beneficial to scale up than scale out

### Design for PaaS model





# Internet of Things

## Introduction
**Internet of Thing: a system of physical objects that can be *discoverd*, *monitoered*, *controlled*, *interacted with* by electornic devices**

### IoT Characteristics
* Dynamic and self-adapting
* Self-configuring
* Interoperable communication protocols
* Unique identity
* Integrated into information network

### IoT vs. WoT
WoT
* Easier to program
* Faster to integrate data and services
* Simpler to prototye, deploy, and maintain large systems

IoT
* More lightweight
* Optimized for embedded device
* Reduced battery, processing, memory and bandwidth usage
* More bespoke and hard-wired solutions

## Raspberry Pi
### Toggle LED
```python
import RPi.GPIO as GPIO
import time
GPIO.setmode(GPIO.BCM)
GPIO.setup(11, GPIO.OUT)
GPIO.setup(17, GPIO.IN, pull_up_down = GPIO.PUD_DOWN)
GPIO.setup(27, GPIO.IN, pull_up_down = GPIO.PUD_DOWN)

state = 0
while not(GPIO.input(17)):
	if GPIO.input(27):
		GPIO.output(11, 1 - state)
		state = 1 - state
	time.sleep(1)
GPIO.cleanup()
```

### Pulsing LED
```python
import RPi.GPIO as GPIO
import time
GPIO.setmode(GPIO.BCM)
GPIO.setup(10, GPIO.OUT)

p = GPIO.PWM(10, 50)
p.start(0)
for i in range(5):
	for dc in range(0, 101, 5):
		p.ChangeDutyCycle(dc)
		time.sleep(0.1)
	for dc in range(100, -1, -5):
		p.ChangeDutyCycle(dc)
		time.sleep(0.1)
p.stop()
GPIO.cleanup()
```
## Network of Things
### Network Topologies
* Point-to-point network
	* Simplest
	* two devices establish a direct connection
* Star network
	* Several nodes communicate with a single central node
	* A node might note be aware of other nodes in the network
* Mesh network
	* No central nodes
	* Nodes in the network are able to forward messages from one node to another

### Network Classification Model
#### OSI
* **Application**
	* HTTP, DNS, MQTT...
* Presentation
	* TLS, SSL
* Session
	* FTP
* **Transport**
	* TCP, UDP, Zigbee
* **Network**
	* IP(v4,v6), Bluetooth
* Data link
	* Thread stack, MAC
* **Physical**
	* Ethernet, WiFi, IEEE 802.15.4
#### Internet Protocol Suite
* Physical layer
	* Communication technologies for a single segment of the network
	* Interfaces required to transmit informantion
* Network layer
	* Connecting hosts across independent network
* Transport layer
	* Communication of information between two hosts
* Application layer
	* Data exchange between two applications

#### Spatical Considerations
NFC 
PAN
LAN
WAN

#### Comparison of IPv4 and IPv6
* IPv4: 4 groups, 8 bits per group
* IPv6: 8 groups, 16 bits per group

#### Comparison of UDP and TCP
* UDP(User Datagram Protocol)
	* Connectionless protocol
	* No handshake between sender and receiver
	* Delivery is not guaranteed
* TCP(Transmission Control Protocol)
	* Connection-oriented protocol
	* Establishes connection between sender and recipient before message is sent
	* Sends message in chunks
	* Size of packets depens on network congestion

#### Personal Area Protocols
* IEEE 802.15.4
	* Low-power, low-cost, and low-rate wireless protocol ofr communication between devices close to each other
	* Baisi of many IoT personal area protocols
* 6LoWPAN
	* IPv6 over low-power wireless personal area networks
	* Bridges the worlds of IoT and Internet
* ZigBee
	* One of the most popular protocols based on IEEE 802.15.4
	* Supports mesh networking 
	* Spans from the Physical layer to the Application layer
* Thread
* Bluetooth
* EnOcean

#### Web of Things Arichitecture
Compose Layer
Share Layer
Find Layer
Access Layer
Networked things
## Securing Web Things
### Symmetric encryption
* Oldest 
### Asymmetric encryption
* public & private key pair
### Standard Protocols for Encrypting data
* Secure Sockets Layer
	* Best known protocol
	* Has major vulnerabilities
* Transport Layer Security
	* Application layer protocol
	* Secures HTTP communication, WebSocket, MQTT
	* Two main roles
		* Helps the client ensure that the server is who it says it is
		* Guarantees that data sent over the communication channel cannot be read by anyone other than the client and the server involved in the transaction
### Access Control with REST and API Tokens

## AI and IoT
