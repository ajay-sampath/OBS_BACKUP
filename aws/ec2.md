the root device of ec2  is  elastic block store

#AMI amazon machine image

#aws #ec2 



instance type 
1. General Purpose
2. Compute-optimized Instances
3. Memory-optimized Instances
4. Storage optimized Instances
5. Accelerated Computing Instance
6. Micro Instance



![[Pasted image 20231230232402.png]]



- ### Images
    

Amazon Machine Image provides the required information to launch an EC2 instance, which may include EBS (elasic block store) storage snapshots , operating systems such as linux, windows, etc. and application servers like JBoss, Weblogic.

A single AMI can construct many instances, duplicated in one or more AWS regions, and can be deregistered when no longer required. Users can use pre-existing AMIs offered by AWS or create their own, which are simple to share or sell.

- ### EBS
    

Amazon Elastic Block Storage abbreviated as (EBS) only provides elastic storage at block levels, which is used for EC2 instances. It offers quick access and persistent data storage using snapshots (which are stored in S3) of EC2.

Some of the volume types provided by EBS are Optimised HDD, Cold HDD, General Purpose SSD, and provisioned SSD.

- ### Networking and Security
    

Networking and security are the main components of EC2 by various techniques such as fundamental pairs, security groups, placement groups, network interfaces, IAM, and VPC, as discussed in the article "What is AWS."

- ### Load Balancing
    

The load balancer scales in accordance with the volume of traffic and distributes incoming traffic among different EC2 instances in various zones.

- ### Auto Scaling
    

Auto-scaling is implemented using launch configurations and auto-scaling groups. Users can create a template where they can specify AMI, instance type, key pair, and other related required attributes.

- ### Monitoring
    

Monitoring of EC2 instances is done by CloudWatch, Status Check, and Events. CloudWatch automatically sends alarms and makes changes according to the defined rules. Status Check is used to identify the status of various software and hardware-related problems.

- ### Region and Availability Zones
    

Amazon operates at various levels of development and highly available data centers. Although rare, failures can occur that affect the availability of the DB instances in the exact location. If all DB instances are made available in a single site, and maybe some failure happens, then none of them will be available later.

That's why AWS EC2 instances are hosted in multiple locations with the concept of availability zones and regions. A single region may have several regions. AWS EC2 places instances across various locations.

## Features of Amazon EC2

- ### Reliability:
    

Amazon EC2 allows you to run instances in many **locations**. Regions and Availability Zones constitute Amazon EC2 locations. You can protect your applications from a single location failure by creating instances in distinct Availability Zones.

Amazon EC2 provides a highly dependable environment in which instances may be **swiftly replaced**. The Amazon EC2 Service Level Agreement assures 99.99 percent availability for each Amazon EC2 Region.

- ### Scalability:
    

Amazon EC2 allows you to adjust your Amazon EC2 capacity up or down according to your demands. To add or delete EC2 instances, you can use the dynamic and predictive scaling controls provided by **EC2 Auto Scaling**.

Predictive scaling use machine learning to allocate instances based on predicted demand, whereas dynamic scaling allows you to increase computation depending on defined metrics. Scaling Amazon **EC2** instances helps to maintain performance while lowering expenses.

- ### Cost Optimization:
    

You only pay for what you use with per-second billing. It deduct the cost of wasted minutes and seconds from the bill, allowing you to concentrate on improving your apps rather than **optimising** use to the hour.

- ### Global infrastructure:
    

Amazon EC2 allows you to run instances in many locations. Regions and Availability Zones constitute Amazon **EC2 locations**. You can protect your applications from a single location failure by creating instances in distinct Availability Zones.

- ### Compatibility:
    

Amazon EC2 integrates seamlessly with Amazon services such as Amazon S3, Amazon RDS, Amazon DynamoDB, and Amazon SQS. It offers a **full computation**, query processing, and storage solution over a wide range of applications.

- ### Operating Systems:
    

Amazon Machine Images (AMIs) are preloaded with an number of operating systems, including Microsoft Windows and Linux distributions like Amazon Linux 2, Ubuntu, Red Hat Enterprise **Linux**, **CentOS**, **SUSE**, and **Debian**.

## Benefits of Amazon EC2

- ### Elastic web-scale computing
    

It takes minimal time for customers to scale up or down their instance capacity. Thousands of parallel computations can be initiated simultaneously on a **server instance**. As these services are controlled by **web APIs**, the customer requires no self-intervention to handle the cases.

- ### Completely controlled
    

Customers have complete control of the instances and can interact with each one because of their **root access** to each one. It can start retaining data according to its requirements and can restart also.

- ### Flexible cloud hosting service
    

Numerous instance types, operating systems, and software packages are available. You can choose the memory, CPU, instance storage, and boot partition size that's best for your preferred operating system using Amazon **EC2**.

- ### Compatible with other AWS web services
    

To offer a comprehensive solution for computation, query processing, and storage across various applications, Amazon **EC2** operates with Amazon S3, Amazon RDS, and Amazon SQS.

- ### Reliable
    

Replacement instances can be quickly and reliably commissioned in a highly dependable environment. The service operates inside Amazon's reliable data centers and network infrastructure.

- ### Secure
    

For your compute resources, Amazon EC2 and Amazon VPC combine to offer security and reliable networking capabilities. Your compute instances are situated in a Virtual Private Cloud (VPC) with your chosen IP range.

- ### Groups and networks for security
    

You can manage network access to and from your instances to limit inbound and outgoing traffic. Your EC2 resources can be set up as Dedicated Instances (dedicated Instances are Amazon EC2 Instances that operate on hardware reserved for a single customer). To use sophisticated networking features like private subnets and outbound connections, you must first configure a VPC and run instances in it.

- ### Inexpensive
    

You receive the financial advantages of Amazon's scaling through Amazon EC2. You pay for the amount of computing power that you use.

- ### Easy to start
    

By visiting the Amazon Web Services Management Console and selecting prepackaged software from Amazon Machine Images, you may quickly get started with Amazon EC2 (AMIs). Through the EC2 console, you may quickly install this software on EC2.

## EC2 vs. S3

EC2 and S3 are very different ideas, where EC2 is primarily used for computing and S3 for primary storage.

### EC2:

A remote computer running Windows or Linux or any other operating system that you may use to install any software you want, including a Web server that runs PHP code and a database server, is called an "EC2 instance."

### S3:

Amazon S3 is a storage facility frequently used to store enormous binary files. Additionally, Amazon offers RDS for relational databases and DynamoDB for NoSQL databases, etc.


### Accelerated Computing

Compared to software running on CPUs, accelerated computing instances use hardware accelerators, or co-processors, to perform tasks like floating point number calculations, graphics processing, or data pattern matching. Depending on the instance size, accelerated instances have "p" and "g" instances with their own NVIDIA cards with varying amounts of GPU.

- The older P instances are simpler to use and have the processing power needed for data science, data analysis, and rendering even though P2 is a "general" purpose instance.
    
- With its NVIDIA Tesla V100, the most recent P3 instance has more power. Similar to the P2, this is an excellent option for data analysis. It will also work great for autonomous vehicles and speech recognition.
    
- The best choice for 3D rendering, video encoding, or application streaming, G3 instances are ideal for building your remote graphics station.
    

**Use Cases:**

High-performance computing, computational fluid dynamics, computational finance, seismic analysis, speech recognition, self-driving cars, and drug discovery are examples of these technologies.

### Storage Optimized

Instances optimized for storage are made for workloads that demand frequent, sequential read and write access to enormous amounts of data stored locally. They are made to offer tens of thousands of low-latency, random I/O operations per second to applications (IOPS). These instances are in three groups: H, I, and D, which are a fantastic choice for databases that must frequently write to the disk.

- For distributed file systems or centralized log processing, H instances are the best choice.
    
- Excellent database option is I instances, particularly for NoSQL or data warehouses.
    
- D instances are similar to H ones but perform better for massively parallel processing data warehousing and distributed computing, such as Hadoop and MapReduce.
    

**Use Cases:**

These instances increase the number of transactions handled per second for I/O-intensive and business-critical workloads with medium-sized data sets that can benefit NoSQL and relational databases (MySQL, MariaDB, and PostgreSQL) with high network speed and computational performance (TPS).

Additionally, they are a perfect fit for workloads like data analytics and search engine workloads requiring quick access to medium-sized data sets on local storage.


