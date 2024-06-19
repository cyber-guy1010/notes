# AWS Certified Solutions Architect – Associate Notes

# Services Summary

## AWS Fundamentals
## Availability Zones and Regions
- [Availability Zone (AZ)](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.RegionsAndAvailabilityZones.html#Concepts.RegionsAndAvailabilityZones.AvailabilityZones) 1 or more discrete data centers (each with redundant power, networking, and connectivity) houses in separate facilities.
- `Region` physical location consisting of 2 or more availability zones
- [Local Zone](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.RegionsAndAvailabilityZones.html#Concepts.RegionsAndAvailabilityZones.LocalZones) is an extension of an AWS Region that is geographically close to your users.
- [Edge Location](https://wa.aws.amazon.com/wellarchitected/2020-07-02T19-33-23/wat.concept.edge-location.en.html) are endpoints for AWS CloudFront that are used for caching content for faster delivery to users at any location.
- [Well-Architected Framework](https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html) helps you understand the pros and cons of decisions you make while building systems on AWS
- `Well-Architected tool` provides a consistent process for measuring cloud architectures
- [Free Tier](https://aws.amazon.com/free/) When you create an AWS account, you’re automatically signed up for the free tier for 12 months.

## Account Security
- `Identity and Access Management (IAM)` allows you to manage users and their level of access to the AWS console
- `Security Token Service (STS)`service for requesting temporary, limited-privilege credentials for AWS Identity and Access Management users or for users that you authenticate (federated users).

## Networking
- [Elastic IP address](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/elastic-ip-addresses-eip.html) static IPv4 address designed for dynamic cloud computing.
- [Virtual Private Cloud (VPC)](https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html) logically isolated part of AWS cloud where you can define your own network
- `Classless Inter-Domain Routing (CIDR)` defines an IP address range for a network or a subnet
- `Route tables` specifies the allowed routes for outbound traffic leaving the subnet
- `Gateway` connects your VPC to another network
- `Internet Gateway` allows communication between resources in your VPC and the internet
- `NAT Gateway` enables instances in a private subnet to connect to the internet or other AWS services while preventing the internet from initiating a connection with those instances
- [NAT instance](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_NAT_Instance.html) provides network address translation (NAT) using a NAT AMI instance
- `VPC Endpoints` enables you to privately connect your VPC to supported AWS services and VPC endpoint services
- `Gateway Endpoints`  gateway that you specify as a target for a route in your route table.
- `Interface Endpoints` elastic network interface with a private IP address from the IP address range of your subnet
- `VPC Peering` allows you to connect 1 VPC with another via a direct network route using private IP addresses
- `Transit Gateway` hub that controls how traffic is routed among all the connected networks
- [VPC Flow Logs](https://docs.aws.amazon.com/vpc/latest/userguide/flow-logs.html) capture IP traffic flow information for the network interfaces associated with your resources. You can create multiple flow logs to send traffic to different destinations.
- [Network Access Analyser](https://docs.aws.amazon.com/vpc/latest/network-access-analyzer/what-is-network-access-analyzer.html) feature that identifies unintended network access to your resources on AWS
- `Security Groups` virtual firewall that controls inbound and outbound traffic into AWS resources 
- [Network Access Control List (NACL)](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-network-acls.html) optional firewall at the subnet boundary
- `PrivateLink` provides private connectivity between virtual private clouds (VPCs), supported AWS services, and your on-premises networks without exposing your traffic to the public internet.
- `Site-to-Site VPN` creates a secure connection between your data center or branch office and your AWS cloud resources.
- `Accelerated Site-to-Site VPN` option provides even greater performance by working with AWS Global Accelerator.
- `Direct Connect` makes it easy to establish a dedicated network connection from on-prem to AWS
- `AWS VPN` VPN services that allow you connect your on-premises networks and remote workers to the cloud
- `Client VPN` fully managed elastic VPN service that automatically scales up or down based on user demand.   
- `AWS Managed VPN` lets you reuse existing VPN equipment and processes and also use existing internet connections.
- `VPN CloudHub` can be used to connect multiple remote sites together
- `Wavelength` embeds AWS compute and storage services within 5G networks
- `Route 53` A service by AWS that allows you to route domain names using DNS
- `IoT Core` provides the cloud services that connect your IoT devices to other devices and AWS cloud services


## Compute
- `Elastic Compute Cloud (EC2)` service that provides secure, resizable compute capacity in the cloud.
- `VMWare Cloud on AWS` managed service that combines compute, network and storage capabilities in a fully supported, ready-to-run service from the creators of the software, VMware and the leading public cloud provider, AWS. 
- `Outposts` brings AWS data center to on-prem
- `Batch` managed service to run batch computing workloads within AWS

## Storage
- `Simple Storage Service (S3)` object storage in the cloud
- `S3 Access Points` simplify managing data access at scale for shared datasets in S3. 
- `S3 Lifecycle management` define rules to automatically transition objects to cheaper storage classes or delete after a set period of time
- [S3 Batch Operations](https://docs.aws.amazon.com/AmazonS3/latest/userguide/batch-ops.html) S3 data management feature that lets you manage billions of objects at scale with just a few clicks in the Amazon S3 Management Console or a single API request. 
- [S3 Event Notifications](https://docs.aws.amazon.com/AmazonS3/latest/userguide/EventNotifications.html) receive notifications when certain events happen in your S3 bucket
- [S3 Select](https://docs.aws.amazon.com/AmazonS3/latest/userguide/selecting-content-from-objects.html) use SQL statements to filter the contents of an Amazon S3 object and retrieve only the subset of data that you need
- `Elastic Block Storage (EBS)` block-level storage volumes that you can attach to EC2 instances
- `Elastic File System (EFS)` managed Network File System that can be mounted on many EC2 instances at once
- `FSx` is a fully managed third-party file system solution.
- `FSx for Windows` fully managed native Microsoft Windows File system
- `FSx for Lustre` fully managed file system optimised for compute-intensive workloads
- `FSx for NetApp ONTAP` shared file storage solution that provides high-performance SSD storage with sub-millisecond latency and is widely accessible from Linux, Windows, and macOS compute instances running on AWS or on-premises.
- `FSx for OpenZFS` file storage service that delivers up to 1 million IOPS with latencies of hundreds of microseconds.
- `Amazon Machine Images (AMI)` provides the information required to launch an instance
- `Data Lifecycle Manager` service used to automate the creation, retention, and deletion of EBS snapshots and EBS-backed AMIs
- `Backup` managed service that allows you to consolidate backups across multiple AWS services
- [WorkDocs](https://docs.aws.amazon.com/managedservices/latest/userguide/workdocs.html) is a fully-managed, secure content creation, storage, and collaboration service.
- [WorkSpaces](https://aws.amazon.com/workspaces/) Fully managed, secure, reliable virtual desktop solutions for every workload


## Databases
- `Relational Database Service (RDS)` collection of managed services that makes it simple to set up, operate, and scale databases in the cloud
- `RDS Proxy` fully managed database proxy for RDS that makes applications more scalable, more resilient to database failures, and more secure.
- `Aurora` MySQL and PostgreSQL compatible relational database engine that combines speed and availability with simplicity and cost-effectiveness of open-source databases
- `Aurora Serverless` serverless DB cluster that automatically starts, shuts down and scales capacity
- `Aurora Global Database` allows a single Aurora database to span multiple AWS regions
- `DynamoDB` managed serverless noSQL database
- `DynamoDB Accelerator (DAX)` caching system specifically for DynamoDB
- `DynamoDB Global Tables` managed multi-master, multi-region replication
- `DocumentDB` allows you to run MongoDB on the AWS cloud
- `Keyspaces` allows you to run Apache Cassandra database service
- `Neptune` allows you to run a graph database service
- `Quantum Ledger Database (QLDB)` allows you to run a ledger database service
- `Timestream` allows you to run a time-series database service
- `ElastiCache` managed version of Memcached and Redis caching technologies

## Monitoring & Scaling
- `Vertical Scaling` resizing an individual instance
- `Horizontal Scaling` creating many different smaller instances rather than a single large one
- `Auto Scaling`monitors your applications and automatically adjusts capacity to maintain steady, predictable performance at the lowest possible cost. 
- `Elastic Load Balancing (ELB)` automatically distribute incoming application traffic across multiple instances
- `Health Checks` periodically send requests to load balancers registered instances to test their status
- `Application Load Balancer (ALB)` intelligent load balancer
- `Network Load Balancer` performance load balancer
- `Gateway Load Balancer` for inline Virtual Appliance Load balancing
- `Classic Load Balancer` Legacy/test/dev load balancer
- `CloudWatch` monitoring and observability platform that was designed to give us insight into our AWS architecture
- `CloudWatch Dashboard` Customizable home pages in the CloudWatch console that you can use to monitor your resources in a single view, even those spread across different regions.
- `CloudWatch Container Insights` collects, aggregates, and summarizes metrics and logs from your containerized applications and microservices.
- `EventBridge (CloudWatch Events)` serverless event bus that allows you to pass events from a source to an endpoint
- `CloudWatch Alarms` watches a single metric over a specified time period, and performs one or more specified actions, based on the value of the metric relative to a threshold over time.
- `Managed Grafana` fully managed service that allows secure data visualisation for instantly querying, correlating, and visualising your operational metrics, logs, and traces from different sources
- `Managed Prometheus` serverless, Prometheus-compatible service used for securely monitoring container metrics at scale

## Automation
- `CloudFormation` allows you to provision resources quickly and consistently
- `CloudFormation registry` helps you discover and provision private and public extensions such as resources, modules, and hooks in your AWS CloudFormation templates.
– `Solutions Library` stores solutions that AWS and AWS Partners have built for a broad range of industry and technology use cases.
- `Cloud Development Kit (AWS CDK)` open-source software development framework to model and provision your application resources by using common programming languages. 
- `Elastic Beanstalk` all in one service for deploying and scaling web applications and services
- [Systems Manager](https://tutorialsdojo.com/aws-systems-manager/) Allows you to centralize operational data from multiple AWS services and automate tasks across your AWS resources
- [Lightsail](https://docs.aws.amazon.com/lightsail/) Easy way to build websites or web applications
- `CodeWhisperer` analyses your comments and code as you write them in your integrated development environment (IDE). 

## Containers
- `Microservices` where software is composed of small independent services that communicate over well-defined APIs.
- `Elastic Container Registry (ECR)` managed container image registry
- `Elastic Container Service (ECS)` open-source container orchestration service that offers a more managed model for deploying your containers.
- `Elastic Kubernetes Services (EKS)` managed kubernetes container orchestration service
- `Fargate` fully managed serverless compute engine tailored for docker containers

## Serverless
- `Lambda` serverless compute service that lets you run code without provisioning or managing the underlying servers
- [Serverless Application Repository](https://aws.amazon.com/serverless/serverlessrepo/) allows users to find, deploy, and publish serverless applications
- [Serverless Application Model (SAM)](https://tutorialsdojo.com/aws-serverless-application-model-sam/) open-source framework for building serverless applications.

## Edge Services
- `CloudFront` Content Distribution Network (CDN) that allows us to spread out our resources all over the globe
- [CloudFront Origin Shield](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/origin-shield.html) centralized caching layer that sits in front of your origin 
- [Edge Functions](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/edge-functions.html) code that you write and attach to your CloudFront distribution
- `CloudFront Functions` write lightweight functions in JavaScript for high-scale, latency-sensitive CDN customizations. 
- [Lambda@Edge](https://docs.aws.amazon.com/lambda/latest/dg/lambda-edge.html) extension of AWS Lambda that lets you deploy Python and Node.js functions at Amazon CloudFront edge locations.
- `Global Accelerator` networking service that sends your users traffic through AWS global network infrastructure via accelerators

## Backup and Recovery
- `Recovery Point Objective (RPO)` what point in time do you want data recovered to
- `Recovery Time Objective (RTO)` how fast do you want to failover
- `Backup and restore` restore system from a backup  
- `Pilot Light` live data replication to a database in another Region
- `Warm standby` scaled-down version of production system in another Region
- `Active/Active failover/ Multi-site` two active sites both active and traffic split between them
- [Elastic Disaster Recovery (DRS)](https://docs.aws.amazon.com/drs/latest/userguide/what-is-drs.html) provides continuous block-level replication, recovery orchestration, and automated server conversion capabilities

## Security
- `CloudTrail` records AWS management console and API calls
- [CloudTrail Lake](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-lake.html) lets you run SQL-based queries on your events. 
- `Shield` free DDoS protection for Elastic Load Balancers, CloudFront, and Route53
- `Shield Advanced` enhanced protection for Elastic Load Balancers, CloudFront, and Route53 against larger and more sophisticated DDoS
- `Web Application Firewall (WAF)` lets you monitor the HTTP and HTTPS requests that are forwarded to CloudFront or an Application Load Balancer
- `Firewall Manager` security management service that allows you to centrally manage firewall rules across accounts and applications.
- `GuardDuty` threat detection service that uses ML to monitor for malicious behaviour
- `Macie` used to discover sensitive data in S3
- `Inspector` automated security assessment service
- `Key Management Service (KMS)` managed service that allows you to create and control encryption keys
- `CloudHSM` cloud-based Hardware Security Module
- `Secrets Manager` securely stores, encrypts and rotates secrets
- `Parameter Store` capability of Systems Manager that provides secure, hierarchical storage for configuration data management
- `Presigned-URLs` can be used to share an S3 object with others
- `Presigned Cookies` can be used to share S3 objects with others
- `Certificate Manager (ACM)` allows you to create, manage, and deploy public and private SSL certificates
- `Audit Manager` allows you to automatically audit AWS usage
- `Artifact` single source to get compliance related information
- `Cognito` authentication, authorisation and user management service for web and mobile apps
- `Cognito User Pools` directories of users that provide registration or sign-in options for users
- `Cognito Identity Pools/ Federated Identities` grant temporary credentials that grant users access to specific AWS resources, whether the users are anonymous or are signed in.
- `Cognito Sync` is an AWS service and client library that makes it possible to sync application-related user data across devices
- `Detective` analyse, investigate and identify root causes of potential issues or suspicious activities
- `Network Firewall` managed service that allows you to deploy physical firewall protection across VPCs
- `Security Hub` single place to view security alerts from AWS security services

## Application Services
- `Tight Coupling` one instance talking directly to another instance
- `Loose Coupling` instances are directly aware of other instances as all communication is done through an intermediary (load balancer, SQS etc.)
- `Simple Queue Service (SQS)` fully managed message queueing service that enables you to decouple and scale microservices, distributed systems, and serverless applications.
- `SQS Dead-Letter queues (DLQ)` targets for messages that cannot be processed successfully
- `First-In-First-Out (FIFO)` guarantees that the first message in will be the first message out of the queue
- `Simple Notification Service (SNS)` fully managed message service for both applications-to-application (A2A) and application-to-person (A2P) communication
- `API Gateway` fully managed service that makes it easy for developers to create, publish, maintain, monitor, and secure APIs at any scale.
- `Amazon MQ` message broker service that allows for easier migration of existing applications to the AWS cloud
- `Step Functions` serverless orchestration service to combine AWS services for business applications
- `AppFlow` fully managed service for exchanging data between SaaS apps and AWS services
- [Simple Workflow Service (SWF)](https://docs.aws.amazon.com/amazonswf/latest/developerguide/swf-welcome.html) provides a way to build, run, and scale background jobs that have parallel or sequential steps.
- [Simple Email Service (SES)](https://docs.aws.amazon.com/ses/latest/dg/Welcome.html) is an email platform that provides an easy, cost-effective way for you to send and receive email using your own email addresses and domains.

## Developer Tools
- `X-Ray` collects application data for viewing, filtering and gaining insights

## Big Data
- `Redshift` fully managed, petabyte-scale data warehouse service in the cloud
- `Redshift Spectrum` efficiently query and retrieve data from S3 without having to load the data into Redshift tables
- `RedShift Streaming Ingestion` Allows you to consume and process data directly from a streaming source to a Redshift cluster using SQL.
- `Redshift ML` Allows you to train and deploy machine learning models using the data stored in your Amazon Redshift cluster through a simple CREATE MODEL SQL statement.
- `Redshift Data Sharing` Redshift Data Sharing is a secure way to share live data across Redshift clusters within an AWS account, without the need to copy or move data.
- `Redshift Serverless` lets you access and analyze data without the usual configurations of a provisioned data warehouse
- `Elastic MapReduce (EMR)` simplifies running big data frameworks to help with Extract, Transform, Load (ETL) processing
- `EMR Notebooks` provide a managed environment, based on Jupyter Notebooks, to help users prepare and visualize data, collaborate with peers, build applications, and perform interactive analysis using EMR clusters.
- `Kinesis` allows you to ingest, process, and analyse real-time streaming data
- `Kinesis Data Streams` real-time streaming for ingesting data
- `Kinesis Data Firehose` managed service to load streaming data into data stores and analytics tools
- `Amazon Managed Service for Apache Flink/ Kinesis Data Analytics` transform and analyze streaming data in real time
- `Athena` interactive query service that makes it easy to analyze data in S3 using SQL
- `Glue` serverless data integration service that makes it easy to discover, prepare and combine data.
- `Lake Formation` managed service that makes it easy to set up, secure, and manage your data lakes
- `Quicksight` fully managed business intelligence (BI) data visualisation service
- `Data Exchange` service that helps AWS easily share and manage data entitlements from other organizations at scale.
- [Data Pipeline](https://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/what-is-datapipeline.html) managed Extract, Transform, Load (ETL) service for automating movement and transforming data
- `Amazon Managed Streaming for Apache Kafka (Amazon MSK)` fully managed service for running data streaming applications that use Apache Kafka
- `MSK Serverless` cluster type that offers serverless cluster management
- `OpenSearch` managed service that allows you to run search and analytics engines
- [ParallelCluster](https://tutorialsdojo.com/aws-parallelcluster/) open source cluster management tool for deploying and managing High Performance Computing (HPC) clusters
- [CloudSearch](https://tutorialsdojo.com/amazon-cloudsearch/) managed service in the AWS Cloud that makes it easy to set up, manage, and scale a search solution for your website or application.

## Governance
- `Organisations` free governance tool that allows you to create and managed multiple AWS accounts
- Account Types
- `Service Control Policies (SCPs)` JSON policies that get applied to OUs or accounts to restrict actions that are allowed or denied
- `Resource Access Manager (RAM)` free services that allows you to share AWS resources with other accounts inside or outside your organisation
- `Config` fully managed service that provides you with an resource inventory, configuration history, and configuration change notifications to enable security and governance.
- `Directory Service` fully managed version of Active Directory
- [Billing and Cost Management](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/billing-what-is.html) provides a suite of features to help you set up your billing, retrieve and pay invoices, and analyze, organize, plan, and optimize your costs.
- `Cost Explorer` tracks and analyses your AWS usage.
- `Budgets` manage budgets for your account.
- `Cost and Usage Reports (CUR)` provides information about your use of AWS resources and estimated costs for that usage.
- [Cost Allocation Tags](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html) tags that track and organize your resource costs on your cost allocation report, to make it easier for you to categorize and track your AWS costs. 
- `Compute Optimizer` service that analyses config and utilisation metrics of AWS resources
- `Trusted Advisor` fully managed best-practice auditing tool
- `Control Tower` service to set up and govern multi-account environment
- `Licence Manager` service that handles software licence management
- `Health/ Personal Health Dashboard` provides visibility of resource performance and availability of services and accounts
- `Service Catalog` used by organisations to create and manage catalogs of approved IT services
- `Proton` service that creates and manages infrastructure and deployment tooling for users, serverless and container-based applications
- [OpsWorks](https://tutorialsdojo.com/aws-opsworks/) configuration management service that helps you configure and operate applications in a cloud enterprise 

## Migration
- `Snow Family` set of secure appliance that provide petabyte-scale data collection and processing solutions for migration to/from AWS services
- `Snowcone` smallest device in the snow family
- `Snowball edge` jack of all trades
- `Snowmobile` heavy lifter, physical truck
- `Storage Gateway` service that gives your applications seamless and secure integration between on-premises environments and AWS storage.
- `File Gateway` caching of local files
- `Volume Gateway` backs up drives to the cloud
- `Tape Gateway` replaces physical tapes
- `DataSync` data transfer service that facilitates moving data between on-premises storage and Amazon EFS, Amazon FSx, and Amazon S3
- `Transfer Family` allows you to move files out of S3 or EFS
- `Migration Hub` single place to track progress of application migration to AWS
- `Server Migration Service` used to move on-prem servers to AWS
- `Database Migration Service` used to move databases to AWS databases services
- `Schema Conversion Tool (SCT)` used to covert on-prem databases to AWS databases
- `Application Discovery Service` helps plan migrations to AWS via collection of usage and config data from on-prem servers
- `Application Migration Service (MGN)` lift-and-shift service for expediting application migration to AWS

## Front-End Web and Mobile
- `Amplify` suite of tools for front-end and mobile development
- `Amplify Hosting` service that provides hosting for web apps
- `Amplify Studio` visual interface that allows developers to easily build and deploy web and mobile apps
- `Device Farm` application testing service for testing and interacting with Android, iOS and web apps
- `Pinpoint` service that allows you to engage with customers through messaging channels
- [AppSync](https://tutorialsdojo.com/aws-appsync/) scalable GraphQL interface for application developers

## Machine Learning
- `Comprehend` uses NLP to help understand meaning and sentiment of text
- `Kendra` allows you to create intelligent search service powered by ML
- `Textract` allows you to process handwriting, text, tables and more
- `Forecast` time-series forecasting service
- `Fraud Detector` service built to detect fraud in your data
- `Polly` turns text to lifelike speech
- `Transcribe` converts audio and video files to text
- `Lex` allows you to build conversational interfaces (bot) in your applications
- `Rekognition` computer vision service that allows you to automate the recognition of pictures and videos
- `SageMaker` service that allows you to build and deploy machine learning models in the AWS cloud
- `Translate` service that translates text into other languages
- Highly accurate and continuously improving
- [Bedrock](https://tutorialsdojo.com/amazon-bedrock/) managed service that allows you to build and scale generative AI applications. 
- [Personalise](https://tutorialsdojo.com/amazon-personalize/) fully managed machine learning service for building recommendation systems.
- [Deeplens](https://tutorialsdojo.com/aws-deeplens/) deep learning-enabled camera for developers

## Media
- `Elastic Transcoder` covert/transcode media files from source format into versions optimised for various devices
- `Kinesis Video Streams` service to stream media content from a large number of devices to AWS 

# Module 1: AWS Fundamentals
## Availability Zones and Regions
- [AWS Global Infrastructure Map](https://aws.amazon.com/about-aws/global-infrastructure/)
- [Availability Zone (AZ)](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.RegionsAndAvailabilityZones.html#Concepts.RegionsAndAvailabilityZones.AvailabilityZones) 1 or more discrete data centers (each with redundant power, networking, and connectivity) houses in separate facilities.
    - a data center or multiple data centers located close together
    - Example: `us-east-1a`
    - Designed for fault isolation
    - If one AZ goes down, then can switch to another in an AZ
        - Need to set up replication to AZ, some services do this automatically
    - Availability zones are physically separated by a meaningful distance but all are within 100km (60 miles) of each other
- `Region` physical location consisting of 2 or more availability zones
    - Example: `us-east-2`
    - Latency varies by region based on where you are based
    - Cost and service availability varies by region
        - `us-east-1` is one of the primary regions, it was the first region and is where AWS roles out many new services first
    - Each AWS Region has 2 or more, isolated locations known as Availability Zones
- [Local Zone](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.RegionsAndAvailabilityZones.html#Concepts.RegionsAndAvailabilityZones.LocalZones) is an extension of an AWS Region that is geographically close to your users.
    - Local data processing
    - Example: `us-west-2-lax-1a`
    - for highly demanding applications that require single-digit millisecond latency to end users
    - [Map of local zones](https://aws.amazon.com/about-aws/global-infrastructure/localzones/locations/)
- [Edge Location](https://wa.aws.amazon.com/wellarchitected/2020-07-02T19-33-23/wat.concept.edge-location.en.html) are endpoints for AWS CloudFront that are used for caching content for faster delivery to users at any location.
    - To deliver content to end users with lower latency
    - Used by CloudFront
    - There can be multiple edge locations nearby (same city)
    - `Regional edge caches` are used when you have content that is not accessed frequently enough to remain in an edge location. 
        - used by default with CloudFront
        - absorb this content and provide an alternative to the need to retrieve that content from the origin server.
    - Many more edge locations than regions
## Well-Architected Framework
- `Solutions architects (SAs)` are responsible for managing an organization’s cloud computing architecture
    - Plan, Research, Build
- [AWS Whitepapers and Guides](https://aws.amazon.com/whitepapers/?whitepapers-main) 
- [Well-Architected Framework](https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html) helps you understand the pros and cons of decisions you make while building systems on AWS
- earn architectural best practices for designing and operating secure, reliable, efficient, cost-effective, and sustainable workloads in the AWS Cloud.
- General Design Principles
    - Stop guessing your capacity needs
    - Test systems at production scale
    - Automate with architectural experimentation in mind
    - Consider evolutionary architectures
    - Drive architectures using data
    - Improve through game days
- `Reviews` should be applied at key milestones in the product lifecycle, early on in the design phase to avoid one-way doors that are difficult to change, and then before the go-live date. 
### Well-Architected Pillars
- `Operational Excellence` Running and monitoring systems to deliver business values, and continually improving processes and procedures.
    - Design Principles:
        - Perform operations as code
        - Make frequent, small, reversible changes
        - Refine operations procedures frequently
        - Anticipate failure
        - Learn from all operational failures
        - Use managed services
        - Implement observability for actionable insights
    - Best Practices:
        - Teams must have a shared understanding
        - Understand your workloads and their expected behaviors
        - Operate understand your workload's interactions and output
        - Implement observability in your workload
        - Evaluate the operational readiness of your workload
        - Learn, share, and continuously improve
- `Performance Efficiency` Using IT and computing resources efficiently
    - Design Principles
        - Democratize advanced technologies
        - Go global in minutes
        - Use serverless architectures
        - Experiment more often
        - Consider mechanical sympathy
    - Best Practices
        - Reduce latency
        - Architecture selection: use multiple solutions and allow different features to improve performance
        - Compute and hardware: vary based on application design
        - Data management: varies based on the kind of data type
        - Networking and content delivery: varies based on latency, throughput requirements, jitter, and bandwidth
        - Process and culture: foster performance efficiency of cloud workloads
- `Security` Apply Security at all layers
    - Design Principles
        - Implement a strong identity foundation
        - Maintain traceability
        - Apply security at all layers
        - Automate security best practices
        - Protect data in transit and at rest
        - Keep people away from 
        - Prepare for security events
    - Best Practices:
        - Enforce principle of least privilege
        - Use MFA
        - Security: apply overarching best practices to every area of security
        - Identity and access management:  only authorized and authenticated users and components are able to access your resources in the way you intend
        - Detection: use detective controls to identify a potential security threat or incident
        - Infrastructure protection: control methodologies, such as defence in depth, necessary to meet best practices and organizational or regulatory obligations
            - Use a VPC
        - Data protection: foundational practices should be in place
            - categorize organizational data based on levels of sensitivity
            - encryption
        - Incident response: routinely practice incident response
        - Application security: understand the security properties of your build and release infrastructure, and use automation to identify security issues. 
- `Cost Optimisation` Avoiding unnecessary costs
    - Design Principles
        - Implement Cloud Financial Management
        - Adopt a consumption model
        - Measure overall efficiency
        - Stop spending money on undifferentiated heavy lifting
        - Analyze and attribute expenditure
    - Best Practices
        - Practice Cloud Financial Management
        - Expenditure and usage awareness, stop guessing
        - Use Cost-effective resources
        - Manage demand and supply resources: only for what you need
        - Optimize over time: review your existing architectural decisions to verify they continue to be the most cost effective
- `Reliability` Ensuring a workload performs its intended function correctly and consistently when it's expected to
    - Design Principles
        - Automatically recover from failure
        - Test recovery procedures
        - Scale horizontally to increase aggregate workload availability
        - Stop guessing capacity
        - Manage change in automation
    - Best Practices
        - Foundational requirements that influence reliability should be in place
        - Design upfront design decisions for both software and infrastructure
        - Anticipate and accommodate changes
        - Expect that failures will occur, recover from failure
- `Sustainability` Minimising environmental impacts of running cloud workloads
    - Design Principles
        - Understand your impact
        - Establish sustainability goals
        - Maximize utilization
        - Anticipate and adopt new, more efficient hardware and software offerings
        - Use managed services
        - Reduce the downstream impact of your cloud workloads
    - Best Practices
        - Choose Regions for your workloads based on both business requirements and sustainability goals.
        - Align service levels to customer needs
        - Maintaining consistent high utilization of deployed resources to minimize the resources consumed.
        - Implement data management practices to reduce the provisioned storage required to support your workload
        - Minimize the amount of hardware needed to provision and deploy, and select the most efficient hardware and services for your individual workload.
        - Reduce your sustainability impact by making changes to your development, test, and deployment practices.
### Well-Architected tool
- `Well-Architected tool` provides a consistent process for measuring cloud architectures
- Assists with documentation 
- Guides for making workloads more reliable efficient, and cost effective
- Asks questions, analyses applications and makes suggestions
- `Workload` collection of resources and code that delivers business value
    - Examples: customer-facing application or a backend process.
- `Lenses` provide a way for you to consistently measure your architectures against best practices and identify areas for improvement
    - 5 lenses can be added at a time to a workload, with a maximum of 20 lenses applied to one workload
    - workload can have one or more lenses applied 
    - Can choose Lenses from a Catalog or make custom lenses
## AWS Accounts
- `AWS Management Console` web interface to manage services
- `AWS Account` basic container and security boundary for all the AWS resources you create
    - Can have up to 5000 users in 1 account
- `Root User` unrestricted account access and is associated with the person who created the AWS account.
    - Should not be used for day-to-day interactions with AWS
    - creates other types of users, such as IAM users and users in AWS IAM Identity Center, and assigns them access credentials.
    - Full admin access to AWS
    - Important to secure this account
    - Should enable MFA for the root account
        - Do this via IAM > Security Credentials > Assign MFA Device
    - Create an admin group for your admins, and assign the appropriate permissions to this group
        - Create user accounts for your admins
        - Add users to the admin group
- `IAM User` Identity within your AWS account that has specific custom permissions
    - Each user has their own credentials.
    - They are authorized to perform specific AWS actions based on permissions.
    - Best practice is to require MFA for IAM users
    - `Programmatic access` IAM user might need to make API calls, use the AWS CLI, or use the AWS SDKs. In that case
        - create an access key (access key ID and a secret access key) for that user
### AWS CLI
- `Command Line Interface (CLI)` unified tool to manage your AWS services
- Secret Access Key: can be used to access EC2 instances
    - generated during creation of EC2 instance
    - Can be regenerated
    - Don't share between developers
- Use roles where possible to allow access
    - Allow access without the use of access key IDs and secret access keys
    - Can easily attach/detach roles without having to stop EC2 instances
- Can be accessed on local machine (OpenSSH or PuTTy) or via AWS web interface
- Least privilege principle should be used when using the CLI
- Use groups to assign user CLI access
### CloudShell 
- [CloudShell](https://tutorialsdojo.com/aws-cloudshell/) is a browser-based, pre-authenticated shell that you can launch directly from the AWS Management Console.
## Amazon Resource Name (ARN)
- `Amazon Resource Name (ARN)` a name unique to each resource
    - Can be assigned to users
    - Syntax: `arn:partition:service:region:account_id/resource`
    - Example: `arn:aws:iam::12345:user/ryan`
    - Some values are omitted but colons are kept
    - Can have resource wildcards
        - Example: `arn:aws:ec2:us-east-1:12345:instance/*`
## Shared Responsibility Model
- [Shared Responsibility Model](https://aws.amazon.com/compliance/shared-responsibility-model/)
- If you can do something in the AWS Management Console, otherwise AWS is likely responsible
- Customer/You: Responsible for security `IN` the cloud
    - Platform, Applications, IAM
    - OS, Network, Firewall
    - Client-side data encryption & Data Integrity
    - Server-side encryption (File system or data)
    - Networking Traffic Protection (Encryption, Integrity, Identity)
- AWS: Responsible for security `OF` the cloud
    - Compute, Storage, Database, Networking
    - Hardware/ Global Infrastructure
    - Regions, AZs, Edge Locations
- `Inherited Controls` Controls which a customer fully inherits from AWS.
    - Physical and Environmental controls
- `Shared Controls` Controls which apply to both the infrastructure layer and customer layers, but in completely separate contexts or perspectives. 
    - AWS provides the requirements for the infrastructure and the customer must provide their own control implementation within their use of AWS services.
    - Examples: Patch management, Configuration Management, Awareness & Training
- `Customer Specific` Controls which are solely the responsibility of the customer based on the application they are deploying within AWS services
    - Service and Communications Protection or Zone Security which may require a customer to route or zone data within specific security environments.
![Shared Responsibility Model](/images/Shared_Responsibility_Model.jpg)
## Free Tier
- [Free Tier](https://aws.amazon.com/free/) When you create an AWS account, you’re automatically signed up for the free tier for 12 months.
- You can use a number of AWS services for free, as long as you haven’t surpassed the allocated usage limit.
- To help you stay within the limits, you can track your free tier usage and set a billing alarm with AWS Budgets to notify you if you start incurring charges.
## Tags and Resource Groups
- `Tags` key-value pairs that can be added to AWS resources to help identify, organise and search for resources
    - Up to user created tags 50 per resource
    - Tags are case sensitive
- `Resource Groups` groupings of instances based on service and tags
    - Can be used in cloudwatch to easily view stats for a particular group
## Service Quotas and Throttling
- `pay-as-you-go model` pay for what you use
- [Service quotas/limits](https://docs.aws.amazon.com/general/latest/gr/aws_service_limits.html) your AWS account has default quotas for each AWS service. 
    - Each quota is Region-specific, unless otherwise noted. 
    - You can request increases for some quotas, but not all quotas can be increased.
    - Can be requested via Console, CLI or support cases
- `Throttling limits` are applied across all accounts and clients in a region. 
    - These limit settings exist to prevent your API—and your account—from being overwhelmed by too many requests. 
    - These limits are set by AWS and can't be changed by a customer.

# Module 2: Account Security
## Identity and Access Management (IAM)
- `Identity and Access Management (IAM)` allows you to manage users and their level of access to the AWS console
- Create user and grant permissions
- Create groups and roles
- Control access to AWS resources
- `IAM is Universal` Does not work at a regional level but at a `global` level
    - can't have IAM specific to a region
- `IAM Identity Center/ Single Sign-On` service for managing human user access to AWS resources
    - `workforce identities` assign your workforce users consistent access to multiple AWS accounts and applications
## IAM as a Certificate Manager
- Can be [used as a certificate manager](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_server-certs.html) in regions where ACM is not supported
- To upload a server certificate to IAM, you must provide the certificate and its matching private key
## IAM database authentication
- `IAM database authentication` works with MariaDB, MySQL, and PostgreSQL. With this authentication method, you 
    - uses an authentication token, don't need to use a password when you connect to a DB instance
## IAM Policy Documents 
- `policy` is attached to an identity or resource to define its permissions.
- `Defence in depth` is a strategy that is focused on creating multiple layers of security
- `Policy Documents` list of statements used to assign permissions
- JSON format
- Policy documents are assigned to groups, users, and roles
    - Typically not assigned directly to a user as this becomes difficult to manager
    - User should be assigned to group and policy document assigned to group
- AWS provides ready made policies
- `Identity Policy` policy assigned to users or groups
- `Inline Policy` policy assigned to one user or one group
- `Resource-based Policy` policy assigned to services or instances
    - checked when someone tries to access the resource
    - Requires a principal
    - [endpoint policy](https://docs.aws.amazon.com/vpc/latest/privatelink/vpc-endpoints-access.html#default-endpoint-policy) is a resource-based policy that you attach to a VPC endpoint to control which AWS principals can use the endpoint to access an AWS service.
        - `default endpoint policy` grants full access to the endpoint.
- `Explicit Deny` policy that denies all access.
    - An explicit deny will always override an allow
    - `Explicit Allow` policy that allows all access.
- `Permissions boundaries` policy defines the maximum permissions that the identity-based policies can grant to an entity, but does not grant permissions
- `Session policies` limit the permissions that the role or user's identity-based policies grant to the session.
- `Version` policy language version that you want to use.
- `Statement` matches an AWS API request
    - can include more than one statement in a policy
- `Sid` Include an optional statement ID to differentiate between your statements.
    - Optional
- `Effect, Action, Resource (EAR)`
    - `Effect` either Allow or Deny
    - `Action` a list of actions that the policy allows or denies.
    - `Resource` for IAM permissions policy, you must specify a list of resources to which the actions apply
        - If you do not include this element, then the resource to which the action applies is the resource to which the policy is attached.
        - Cannot be included at same time as Principal
    - `Principal` entity that can request an action or operation on an AWS resource 
        - Can be a IAM user, IAM role, AWS Service, Identity Provider or Federated user
        - Required for resource-based policy, you must indicate the account, user, role, or federated user to which you would like to allow or deny access
        - Cannot be included at same time as Resource
    - `Condition` Specify the circumstances under which the policy grants permission.
        - Optional
- Example: `AdministratorAccess` AWS-managed policy, allow the action of everything on every resource
    ```json
    {
        "Version": "2012-10-17",
        "Statement": [
            {
            "Effect":"Allow",
            "Action":"*",
            "Resource":"*",
            }
        ]
    }
    ```
- Example:
    ```json
        {
        "Version": "2012-10-17",
        "Statement": [
            {
            "Sid": "FirstStatement",
            "Effect": "Allow",
            "Action": ["iam:ChangePassword"],
            "Resource": "*"
            },
            {
            "Sid": "SecondStatement",
            "Effect": "Allow",
            "Action": "s3:ListAllMyBuckets",
            "Resource": "*"
            },
            {
            "Sid": "ThirdStatement",
            "Effect": "Allow",
            "Action": [
                "s3:List*",
                "s3:Get*"
            ],
            "Resource": [
                "arn:aws:s3:::confidential-data",
                "arn:aws:s3:::confidential-data/*"
            ],
            "Condition": {"Bool": {"aws:MultiFactorAuthPresent": "true"}}
            }
        ]
        }
    ```
- Example: Resource-based policy
    ```json
    {
        "Version": "2012-10-17", "Statement": [
        {
        "Sid": "AccountBAccess", 
        "Effect": "Allow", 
        "Principal": {"AWS": "444455556666"}, 
        "Action": "s3:PutObject", 
        "Resource": [ "arn:aws:s3:::DOC-EXAMPLE-BUCKET/folder123/*"] 
        } 
        ] 
    } 
    ```
## Permission Boundary
- `permissions boundary` is an advanced feature for using a managed policy to set the maximum permissions that an identity-based policy can grant to an IAM entity. 
- List of allow permissions
- Do not provide permissions on their own
- act as a filter.
- allowed to perform only the actions that are allowed by both its identity-based policies and its permissions boundaries.
- SCPs provide permission boundaries for Organisations
## Users, Groups and Roles
- `Users` a physical person
    - Best practice for users to inherit their permissions from groups
    - Never share user accounts between people
    - Users can be in multiple groups
- `Groups` collection of IAM users
    - can specify permissions for multiple users, which makes it easier to manage the permissions
- `Roles` identity within IAM that has specific permissions
    - User can `assume a role`
        - Permissions are only valid while operating under the assumed role.
        - Role credentials are specific for users
        - Users only have to login once, can assume different roles once signed in
        - `Maximum Session Duration` defines how long a user can stay in a role before automatically removing them
    - Don't have user permission when in a role
    - AWS Services can assume a role
    - Internal usage within AWS, allows different parts of AWS to access each other
    - Commonly used to allow user access to EC2 or Lambda
    - Allow you to avoid hard coding credentials
    - Can easily update policies attached to a role
    - federate a directory service
    - `Lambda execution role` grants a lambda function permission to access AWS services and resources.
- `Principle of least privilege` only assign a user the minimum privileges to do their job
- To allow users to log in with their Active Directory accounts
    - [Set up SAML 2.0-Based Federation by using a Microsoft Active Directory Federation Service (AD FS)](https://aws.amazon.com/blogs/security/aws-federated-authentication-with-active-directory-federation-services-ad-fs/)
- [Web Identity](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/WIF.html) users can sign in to an identity provider and then obtain temporary security credentials from AWS Security Token Service (AWS STS).
    - Login with Amazon, Facebook, Google
    - Users can assume a role
- IAM is used to create and manage Users, Groups and Roles
- Account settings
    - Can specify password policy
    - Always setup password rotations
- New users have no permissions when first created
- Access key ID and secret key: is required to access the Command Line Interface
    - Cannot be used to log into AWS online
    - Not the same as usernames and passwords
    - Can only view these once
- `Identity Providers` allows us to connect to SAML (Active directory) or OpenID Connect
    - Can connect to corporate Single Sign On (SSO)
    - Allows for IAM federation
## Setting up Cross-Account Role access
- `Cross-Account role access` ability to set up temporary access you can easily control.
- Prevents having to duplicate IAM accounts
- `Temporary Credentials` need for long-term access keys or IAM users
    - Can be revoked as needed
- How to set this up
    1. Create a new IAM role with a policy that has the least amount of privileges required
    2. Update the trust policy to allow role assumption from the Auditor Account IAM role
    3. Provide the ARN of the Role to the audit team. They need to grant permissions to assume the role ARN provided to them
    4. Test the other account has access
## Security Token Service
- `Security Token Service (STS)`service for requesting temporary, limited-privilege credentials for AWS Identity and Access Management users or for users that you authenticate (federated users).
- Used as part of a role-based access control strategy
- Global Service


# Module 3/10: Networking
## Network Topology Best Practices
- Use highly available network connectivity for your workload public endpoints
    - DNS, use Route 53
    - Use Route 53 health checks and configure DNS failover
    - Serverless, use API Gateway along with AWS Lambda
    - Simple API, use CloudFront 
    - Geographic split, use Global Accelerator
    - Stop DDoS, use Shield
- Provision redundant connectivity between private networks in the cloud and on-premises environments
    - Use multiple Direct Connect connections or VPN tunnels
- Ensure IP subnet allocation accounts for expansion and availability
    - Make VPCs as large as possible, largest VPC possible (/16) results in over 65,000 IP addresses
    - Allow IP address space for more than one VPC per Region.
    - Within a VPC, allow space for multiple subnets so that you can cover multiple Availability Zones.
    - The initial VPC CIDR block allocated to your VPC cannot be changed or deleted, but you can add additional non-overlapping CIDR blocks to the VPC. This however may fragment your address ranges.
- Prefer hub-and-spoke topologies over many-to-many mesh
    - Transit Gateway provides a hub-and-spoke model
    - Easier to maintain
- Enforce non-overlapping private IP address ranges in all private address spaces where they are connected
    - Capture your current subnet usage. 
    - Use service API operations `DescribeSubnets` to collect subnets per VPC in each Region. 
    - migrate to a new range of addresses or use Network and Port Translation (NAT) appliances from AWS Marketplace if you need to connect the overlapping ranges. 
## Data Transfer Charges
- [Data Transfer Charges](https://aws.amazon.com/blogs/architecture/overview-of-data-transfer-costs-for-common-architectures/) vary depending on the services used and the source AWS Region
- `Within an AZ` within the same Availability Zone is free
- `Between an AZ` charge varies by service, some are free
    - EC2 instances in different AZs (same region) incur inbound/outbound charges
        - EC2 to RDS in another AZ incur inbound/outbound charges
    - RDS instances in different AZs (same region) do not incur inbound/outbound charges
    - Use resources from the local Availability Zone whenever possible.
- `Within an AWS Region` charged for both inbound and outbound traffic
    - If the internet gateway is used to access the public endpoint of the AWS services in the same Region, there are no data transfer charges
    - If a NAT gateway is used to access the same services, there is a data processing charge (per gigabyte (GB)) for data that passes through the gateway.
- `Between AWS Regions` charge is determined by the data transferred out from the source Region, no charge for the data transferred into the destination Region
    - charge depends on the source and destination Region
    - Avoid cross-Region data transfer unless your business case requires it.
- `Out to the internet` no charge for inbound data transfer across all services in all Regions. Charged per service, with rates specific to the originating Region.
    - Avoid routing traffic over the internet when connecting to AWS services, use VPC endpoints
    - Sending data to on-premises networks, use Direct Connect
## Networking Basics
### Public and Private IP Addresses
- `Public IP addresses` accessible from the internet.
    - Public IP addresses obscure the private IP addresses, which are only reachable within the network
- `Private IP` Used for communication within your private network. 
    - not reachable over the internet.
### Elastic IP address
- [Elastic IP address](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/elastic-ip-addresses-eip.html) static IPv4 address designed for dynamic cloud computing.
- associated with any instance or network interface for any VPC in your account
- Only supported for IPv4
- allocated to your AWS account, and is yours until you release it
- you can mask the failure of an instance or software by rapidly remapping the address to another instance in your account
- use in a DNS record for your domain, so that your domain points to your instance.
- can be associated with a single instance or network interface at a time
- You're limited to 5 Elastic IP addresses per region
    - To help conserve them, you can use a NAT device
    - use an Elastic IP address primarily to be able to remap the address to another instance in the case of instance failure.
## Virtual Private Cloud (VPC)
- [Virtual Private Cloud (VPC)](https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html) logically isolated part of AWS cloud where you can define your own network
- private cloud hosted within a public cloud
- virtual data center in the cloud
- Spans a single region, covers all AZs in a region
- Gives control over internet gateways, route tables, network access control lists, subnets, security groups
    - Allows launching of instances to subnet of your choosing
- can't change the primary CIDR for a VPC, so you must create a new one to connect it to your internal network.
- What is created when you created a VPC?
    - Route tables
    - ACL
    - Security groups
- `Default VPC` Your AWS account includes a default VPC in each AWS Region
    - Provisioned at account creation
    - Preconfigured for immediate use
    - Span all Availability Zones within the Region
    - Owned and controlled by the customer
    - Use primarily for testing
    - Creates internet gateway, route tables and public subnets
        - Subnets will be public by default
### Connect a VPC to the internet
To enable access to or from the Internet for instances in a VPC subnet, you must do the following:
1. Attach an Internet Gateway to your VPC
2. Ensure that your subnet’s route table points to the Internet Gateway.
3. Ensure that instances in your subnet have a globally unique IP address (public IPv4 address, Elastic IP address, or IPv6 address).
4. Ensure that your network access control and security group rules allow the relevant traffic to flow to and from your instance
### Subnets
- `Classless Inter-Domain Routing (CIDR)` defines an IP address range for a network or a subnet
    - `Mask` defines which portion of the IP address is dedicated to network identification and which can be used for host IP addresses
        - Block sizes must be between /16 and /28 netmask
    - Example: subnet mask of /16 reserves the first 16 bits, or two octets, for network identification. The remaining 16 bits are used for host identification.
- [Subnets](https://docs.aws.amazon.com/vpc/latest/userguide/configure-subnets.html) range of IP addresses in your VPC
- subset of the VPC CIDR block
    - CIDR blocks cannot overlap
- resides in a single Availability Zone
    - When you add subnets to your VPC to host your application, create them in multiple Availability Zone for better availability
- Every subnet you create is associated with the main route table for the VPC.
- Can have multiple subnets
- First 4 IPs and last IP are reserved (for networking and by AWS)
- Can contain both IPv4 and IPv6 addresses
- Use Security Groups and NACLs to secure subnets
- Each subnet must be associated with
    - a route table, automatically associated with the main route table for the VPC
    - a network ACL, automatically associated with the default network ACL for the VPC
- Subnet types
    - `Public subnet` direct route to an internet
        - Requires route table, Internet gateway and public IPs to access the internet
    - `Private subnet` no direct route to an internet, require a NAT device to access the public internet.
        - Still has access to Route53 DNS
        - put web-tier instances inside private subnets behind a load balancer placed in a public subnet
    - `VPN-only subnet` route to a Site-to-Site VPN connection through a virtual private gateway, no route to an internet gateway.
    - `Isolated subnet` no routes to destinations outside its VPC
### Route Tables
- `Route tables` specifies the allowed routes for outbound traffic leaving the subnet
- subnet can be associated with only one route table at a time
- can associate multiple subnets with the same route table
- Should keep public and private IPs in separate Route Tables where possible
- Associate a Route table to an internet gateway to create public IPs
- `Implicit Route Table/ Main route table` contains only a single route permits communication for all the resources within the VPC.
    - Created by default by the VPC
- Example: Send all other traffic 0.0.0.0/0 to Internet Gateway to connect to the internet
### Gateways
- `Gateway` connects your VPC to another network
- `Internet Gateway` allows communication between resources in your VPC and the internet
    - provide a target in your subnet route tables for internet-routable traffic.
    - protects IP addresses on your network by performing network address translation (NAT)
    - `Egress-only Internet gateway` allows outbound communication to the internet but prevents the internet from initiating connections.
        - IPv6 only 
        - stateful
        - cannot associate a security group with an egress-only Internet gateway.
        - can use a network ACL to control the traffic to and from the subnet for which the egress-only Internet gateway routes traffic.
- Needs to be attached to a VPC
- VPCs can only have 1 internet gateway
- `NAT Gateway` enables instances in a private subnet to connect to the internet or other AWS services while preventing the internet from initiating a connection with those instances
    - uses an Elastic IP address as the source IP address for traffic from the private subnet
    - Must be created in a public subnet
    - Used to connect private subnets to the internet via an internet gateway
        - Private Subnet -> NAT Gateway -> Internet Gateway
    - Highly available
    - Managed by AWS
    - Redundant inside the AZ, only ever need 1
    - 5-45 Gbps
    - No need to patch
    - Not associated with security groups
    - Automatically assigned public IP address
- [NAT instance](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_NAT_Instance.html) provides network address translation (NAT) using a NAT AMI instance
    - Managed by you
    - Used allow resources in a private subnet to communicate with destinations outside the VPC
    - must have internet access, so it must be in a public subnet
    - recommended that you use NAT gateways because they provide better availability and bandwidth and require less effort on your part to administer.
### VPC Endpoints
- `VPC Endpoints` enables you to privately connect your VPC to supported AWS services and VPC endpoint services
- Avoids using the public internet via a Internet Gateway or NAT Device
- Traffic between VPC and other service do not leave AWS network
- Instances in your VPC do not require public IPs
- without using an internet gateway, NAT device, VPN connection or AWS Direct Connect connection.
- redundant, horizontally scaled, highly available VPC components
- Helps remove imposed availability risks or bandwidth constraints on network traffic
- Should be used for large data transfer or large number of requests rather than using NAT gateway
- `Gateway Endpoints`  gateway that you specify as a target for a route in your route table.
    - Inside VPC, similar to NAT gateway
    - Choose this for public facing services such as S3 and dynamo DB
        - S3 must be in same region, otherwise use Interface Endpoint
    - target for traffic that is destined for a supported AWS service
    - no additional charge for using gateway endpoints apart from standard charges for data transfer and resource usage still apply.
    - IPv4 only
    - must enable DNS resolution in your VPC
- `Interface Endpoints` elastic network interface with a private IP address from the IP address range of your subnet
    - On edge of VPC
    - Use for all other services (apart from S3 and DynamoDB) and 3rd party services
        - All services supported by PrivateLink 
        - Use for S3 in another region
    - traffic is directed to the new endpoint without changes to any route tables in your VPC
    - Entrypoint for traffic headed to a supported service
    - pay an hourly rate for every provisioned Interface endpoint.
    - IPv4 only
### VPC Peering
- `VPC Peering` allows you to connect 1 VPC with another via a direct network route using private IP addresses
- Instances behave if they were on the same private network
- Intra-Region, inter-Region support and Cross-account support
- No `transitive peering`, cannot talk to other VPCs through an intermediary VPC
- You can peer between regions
- Can't have overlapping CIDR ranges
- Have to accept peering request
    - Allows different owners of VPCs to accept separately
- highly available connections, no single point of failure
-  Use private IP addresses to direct traffic, traffic remains in the private IP space
- Uses 
    - Connect to a shared services VPC
    - Connect small number (less than 5) VPCs
### Transit Gateway
- `Transit Gateway` hub that controls how traffic is routed among all the connected networks
- Traffic stays on AWS not the internet
- can use to interconnect your VPCs and on-premises networks, and it scales elastically, based on traffic.
    - Works with Direct Connect and Site-to-Site VPNs
- Acts as a cloud router, each new connection is made only once
- Services can talk to each other through a transit gateway
    - Allows `transitive peering` between many VPCs
- Can connect up to 5000 VPCs
- Supports IPv4 and IPv6
    - Operates at Level 3, packets are sent to a specific next-hop attachment based on their destination IP addresses.
- Works on `regional` basis 
    - Use gateway `peering attachments` to connect to a transit gateway in same/another region
- Can be run across multiple AWS accounts using RAM (Resource Access Manager)
- Use route tables to limit how VPCs talk to each other
- Supports IP Multicast (not supported by any other AWS service)
- `attachment` is a source and a destination of packets
    - Can be VPC, VPN connection, Direct Connect gateway, Transit Gateway Connect, Transit Gateway peering connection
    - associated with exactly one route table
- `Blackhole route` can be used to stop certain VPCs from communicating with each other
- [Transit Gateway Inter-Region peering](https://aws.amazon.com/blogs/networking-and-content-delivery/building-a-global-network-using-aws-transit-gateway-inter-region-peering/) allows VPCs attached to an AWS Transit Gateway hosted in one Region can exchange traffic with resources deployed in other Regions
### VPC Flow Logs
- [VPC Flow Logs](https://docs.aws.amazon.com/vpc/latest/userguide/flow-logs.html) capture IP traffic flow information for the network interfaces associated with your resources. You can create multiple flow logs to send traffic to different destinations.
- Network activity, IP traffic information to and from VPC network interfaces
- can be configured at VPC, subnet or network interface level
- can be published to CloudWatch Logs, S3, or Data Firehose
- Uses
    - Diagnose overly restrictive security group rules.
    - Monitor the traffic that is reaching your instance. 
    - Determine the direction of the traffic to and from the network interfaces.
### Network Access Analyser
- [Network Access Analyser](https://docs.aws.amazon.com/vpc/latest/network-access-analyzer/what-is-network-access-analyzer.html) feature that identifies unintended network access to your resources on AWS
- Can help Demonstrate compliance
- can help you verify
    - Network segmentation
    - Internet accessibility
    - Trusted network paths
    - Trusted network access
## Network Security
### Security Groups
- `Security Groups` virtual firewall that controls inbound and outbound traffic into AWS resources 
- `All rules evaluated` before deciding whether to allow traffic
    - ALLOW rules only
- `Stateful` responses to allowed inbound traffic are allowed to flow out regardless of outbound rules
- `Default Security group` all inbound traffic is blocked and all outbound traffic is allowed
    - You can't delete this group, however, you can change the group's rules.
- `Custom Security group` all inbound traffic is blocked and all outbound traffic is allowed
- no additional charge for using network ACL
- Need to open up HTTP/HTTPS ports for web servers to work
- After you launch an instance into a VPC, you can change the security groups that are associated with the instance. 
    - You can change the security groups for an instance when the instance is in the running or stopped state.
    - Changes take effect immediately
- Used to control traffic to EC2 instances
    - virtual firewalls for your EC2 instance
    - can assign up to five security groups to an EC2 instance.
    - Can have multiple EC2 instances within a security group
    - Can be configured during setup of EC2 instance

### Security Group Chaining
- `Security group chaining` Inbound and outbound rules allow traffic flow from the top tier to the bottom tier.
- groups act as firewalls to prevent a subnet-wide security breach.
### Network Access Control Lists
- [Network Access Control List (NACL)](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-network-acls.html) optional firewall at the subnet boundary
- `Rules processed in order` when deciding whether to allow traffic, `executed immediately` when a matching rule is found.
    - Rules have a priority starting with lowest numbered
- `Stateless` responses to allowed inbound traffic are subject to the rules for outbound traffic (and vice versa)
    - Corresponding rules for both inbound and outbound traffic required
- `Default NACL` allows all outbound and inbound traffic
    - Comes with VPC by default
    - If you don't explicitly associate a subnet with a network ACL, the subnet is automatically associated with the default NACL
    - You can add and remove rules from a default NACL, but you can't delete the default NACL itself.
    - Each network ACL also includes a rule whose rule number is an asterisk (*), you can't modify or remove this rule.
- `Custom NACL` by default each custom network ACL denies all inbound and outbound traffic until you add rules
- no additional charge for using network ACL
- Network ACL can be associated with multiple subnets but a subnet can only have 1 Network ACL at a time
- `Rule` there are inbound and outbound rules, each can either allow or deny traffic
    - `Rule number` priority starting with lowest numbered
    - `Type` The type of traffic; for example, SSH. You can also specify all traffic or a custom range.
    - `Protocol` You can specify any protocol that has a standard protocol number. For more information, see Protocol Numbers
    - `Port range` The listening port or port range for the traffic. For example, 80 for HTTP traffic.
    - `Source` [Inbound rules only] The source of the traffic (CIDR range).
    - `Destination` [Outbound rules only] The destination for the traffic (CIDR range).
    - `Allow/Deny` Whether to allow or deny the specified traffic.
- Use Network ACL not Security Groups to block IP addresses
## PrivateLink
- `PrivateLink` provides private connectivity between virtual private clouds (VPCs), supported AWS services, and your on-premises networks without exposing your traffic to the public internet.
- Best way to expose a service VPC to customer VPCs
- Doesn't require VPC peering, no route tables, NAT gateways, internet gateways
- Requires an Network Load Balancer on the service VPC and an ENI on the customer VPC
## Hybrid Networking
- Options to connect our on-premises network to the AWS Cloud?
### Site-to-Site VPN
- `Site-to-Site VPN` creates a secure connection between your data center or branch office and your AWS cloud resources.
- Goes over internet
- Part of AWS VPN Service
- Simple to setup
- Encrypted by default
- offers two VPN tunnels that go between a virtual private gateway (or a transit gateway) on the AWS side, and a customer gateway on the on-premises side. 
    - `virtual private gateway` is the VPN concentrator on the AWS side of the AWS Site-to-Site VPN connection.
    - `customer gateway` is a resource that you create in AWS
-  choose either static routing or dynamic routing based on the features of your customer gateway device. 
    - dynamic routing option uses Border Gateway Protocol (BGP) to automatically discover routes
- Cost:
    - charged a per-hour connection fee for your use
    - Generally lower cost than Direct Connect#
    - Pay only when connect is active
- `Accelerated Site-to-Site VPN` option provides even greater performance by working with AWS Global Accelerator.
### Direct Connect
- `Direct Connect` makes it easy to establish a dedicated network connection from on-prem to AWS
- Does not go over the internet, dedicated internet connection
    - `virtual interfaces` created directly to Amazon VPC, public AWS services (S3) bypassing internet service providers (ISPs) in your network path
- links your internal network to a Direct Connect location over a standard Ethernet fibre-optic cable
- Cost
    - Higher cost than Site-to-Site VPN
    - Charged based on Capacity, port hours and Data Transfer Out
    - Pay when connect is inactive
- Higher effort to setup
    - Need predictable network performance
    - network is collocated with an existing Direct Connect location
    - working with a Direct Connect Partner
    - working with an independent service provider to connect to Direct Connect.
- not encrypted by default.
    - use the transit encryption options
- Fast, secure and reliable connection, large throughput
- Can help reduce network costs, reduce bandwidth
- `Dedicated Connection` physical ethernet connection associated with a single customer
    - Can be requested through AWS Direct Connect console, CLI or API
- `Hosted Connection` a physical ethernet connection provided by an ISP (AWS Direct Connect Partner)
- `Letter of Authorization and Connecting Facility Assignment (LOA-CFA)` is required to begin the process of creating the cross-connect in the data center
- `Data transfer out (DTO)` refers to the cumulative network traffic that is sent through AWS Direct Connect to destinations outside AWS.
## AWS VPN
- `AWS VPN` VPN services that allow you connect your on-premises networks and remote workers to the cloud
- `Client VPN` fully managed elastic VPN service that automatically scales up or down based on user demand.   
    - don’t need to install and manage hardware or software-based solutions, or try to estimate how many remote users to support at one time.
- `AWS Managed VPN` lets you reuse existing VPN equipment and processes and also use existing internet connections.
    - It is an AWS-managed high availability VPN service.
    - It supports static routes or dynamic Border Gateway Protocol (BGP) peering and routing policies.
## VPN CloudHub
- `VPN CloudHub` can be used to connect multiple remote sites together
- Hub-and-spoke model
- Operated over public internet but all traffic is encrypted
- Low cost and easy to manage
## Wavelength
- `Wavelength` embeds AWS compute and storage services within 5G networks
- Mobile edge computing infrastructure
- Helps deploying and scaling ulta-low-latency applications
- Smart cars
## Route 53
- `Route 53` A service by AWS that allows you to route domain names using DNS
- Can register or transfer domain names
- connects user requests to infrastructure running in AWS, such as EC2 instances, ELB, S3
- can configure an CloudWatch alarm to check on the state of your endpoints. 
    - Combine your DNS with health check metrics to monitor and route traffic to healthy endpoints
- `hosted zone` is a container for records
    - Records contain information about how you want to route traffic for a specific domain
    - `Public hosted zones` contain records that specify how you want to route traffic on the internet
        - Route to internet-facing resources
        - Resolve from the internet
    - `Private hosted zones` contain records that specify how you want to route traffic in your VPC
        - Route to VPC resources
        - Resolve from inside the VPC 
- `Zone Apex` top node of a DNS namespace
- Manage and create DNS records
    - `SOA` start of authority record, start of DNS records
    - `CNAME` records, map one domain to another
        - Always choose an alias record over a CNAME
        - Not allowed for Zone Apex
    - `NS` Name Server records, where is DNS info stored
    - `A` Records, maps domain name back to IP address
        - Used to route traffic to a resource
    - `AAAA` records match a domain name to an IPv6 address
        - exactly like DNS A records, except that they store a domain's IPv6 address instead of its IPv4 address.
- Can buy domains through AWS
    - Can take up to 3 days to register
- DNS operates on route 53
- Improves availability between region using Routing Policies
- Routing Policies (7 total)
    - `Simple Routing` one record with multiple IP addresses
        - If you specify multiple values in a record, Route 53 returns all values to the user in a random order
    - `Weighted Routing` allows you to split traffic based on different weights assigned
        - Example: 10% to us-east-1 and 90% to eu-west-1
        - `Health checks` if a record set fails a health check it will be removed from route 53 until it passes
            - TCP, HTTP, HTTPS, and SSL protocols can be used
            - Set on individual record sets
            - Can check status of other health checks
            - Can check status of a CloudWatch alarm
        - Can send SNS notification to alert you about failed health checks
    - `Failover Routing` used when you want to crate an active/passive failover to a secondary instance
        - Example: primary site in eu-west-2 and secondary site in ap-southeast-2
        - Route 53 will monitor the health of your primary site using a health check
    - `Geolocation Routing` choose where traffic will be sent based on the geographic location of users
        - Good for compliance (GDPR)
        - Helps with localisation (languages)
    - `Geo-proximity Routing (Traffic Flow Only)` builds a routing system using a combination of geo-proximity, latency, and availability to route traffic.
        - Must use Route 53 traffic flow
        - `Bias` shrinks the size of a geographic region from which traffic is routed to a resource
            - Optional choose to route more traffic or less to a given resource by specifying a value
    - `Latency-Based Routing` route based on lowest network latency for your end user
        - Region that gives them fastest response time
    - `Multi-value Answer Routing` configures Route 53 to return multiple values in response to DNS queries
        - Simple routing with health checks, only returns healthy resources
        - Returns only the values for healthy resources
- `Zonal shift` capability in Route 53 Application Recovery Controller that shifts a load balancer resource away from an impaired Availability Zone with a single action. 
    - Only supported on Application Load Balancers and Network Load Balancers with cross-zone load balancing turned off
## IoT Core 
- `IoT Core` provides the cloud services that connect your IoT devices to other devices and AWS cloud services
    - device software that can help you integrate your IoT devices into AWS IoT-based solutions


# Module 4: Compute
## Elastic Compute Cloud (EC2)
- `Elastic Compute Cloud (EC2)` service that provides secure, resizable compute capacity in the cloud.
- VM hosted in AWS
- Operate at a regional level
- [Instance types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html) determine the hardware of the host computer used for your instance
### EC2 Pricing Options
- `On-demand` pay by the hour or second, depending on the type of instance you run
    - unpredictable usage that is not suitable for Spot
    - Low cost and flexible
    - No up-front payment
    - Short-term
    - Good for workloads that cannot be interrupted
    - Good for testing and development
- `Reserved` reserved capacity for 1 to 3 years
    - Predictable usage
    - Specific capacity requirements
    - Can pay up front
    - [Billed](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/concepts-reserved-instances-application.html) for every clock-hour during the term that you select, regardless of whether an instance is running
        - When you run out of Reserved capacity, switches to on-demand
    - `Standard Reserved Instances`
        - up to 72% off
    - `Convertible Reserved Instances` can change to a different Reserved Instance of equal or greater value
        - up to 54% off
    - `Scheduled Reserved Instances` launched within time window you define
    - `Reserved Instance Marketplace` supports the sale of third-party and AWS customers' unused Standard Reserved Instances
- `Spot` Purchase unused capacity
    - Up to 90% discount on hourly charge
    - Good for applications with flexible start and end times
        - Stateless, fault-tolerant, flexible applications
    - Big Data, Containers, CI/CD, HPC
    - Don't use work applications that need to be always available, database
    - Cheapest option
    - Maximum Spot Price: you define a price where BELOW this price you will pay for an instance
        - When it goes above this prices running instances are stopped or terminated (you have 2 mins to choose)
        - Price varies between region
    - `Spot Block` used to stop spot instances from terminating
    - `Spot Fleet` collection of spot instances
        - Attempts to launch On-Demand instances to meet specified target capacity
        - Spot Fleet Strategies
            - `capacityOptimised` spot instances come from pool with optimal capacity for the number of instances launching
            - `diversified` spot instances are diversified across all pools
            - lowestPrice: spot instances come from pool with lowest price
            - `InstancePoolsToUseCount` spot instances are distributed across the number of spot instance pools specified.
                - Used in combination with lowestPrice
    - `Launch Pools` define instance type, OS, AZ for spot instances
        - Can have multiple pools
- `Dedicated` A physical EC2 server dedicated for your use
    - Most expensive option
    - Good for compliance, cannot share physical components with other customers
    - Some licencing that requires Dedicated hosts
        - Allows you to use existing per-socket, per-core, or per-VM software licences
        - Such as Windows Server, Microsoft SQL server, SUSE Linux Enterprise Server
    - Can be purchased on demand (hourly)
    - Up to 70% off if reserved early
### Bootstrap scripts
- `Bootstrap Script/ User Data` script that runs when the instance first runs
    - User data field is used when setting up an EC2 instance to store bootstrap script
    - By default, user data runs one time and one time only.
- `EC2 Metadata` information about an EC2 instance
    - `http://169.254.169.254/latest/meta-data/` url where information about an instance sits 
        - instance ID, public keys, and public IP address
    - Public/private IP
    - Hostname
    - Security groups
    - Bootstrap scripts can be used to access metadata
### EC2 Networking
- `Elastic Network Interface (ENI)` basic day-to-day networking, added by default
    - Private/public IPv4 
    - Many IPv6 addresses
    - MAC Address
    - 1+ security groups
    - Low-budget, high availability solution
    - Dual-homed workloads
    - Allows use of network and security appliances in your VPC
    - Allows creation of a management network
- `Enhanced Networking (EN)` single root I/O virtualisation to provide high performance
    - Networks between 10-100 Gbps
    - Lower CPU usage
    - High bandwidth, high packets per second, lower latencies
    - `Elastic Network Adapter (ENA)` Supports speeds of up to 100 Gbps
        - Always choose this over VF, faster and more modern
    - `Intel 82599 Virtual Function (VF) Interface` supports speeds of up to 10 Gbps
        - Typically used in older instances
- `Elastic Fabric Adapter (EFA)` accelerates High Performance Computing (HPC) and machine learning (ML) applications
    - Lower and more consistent latency, higher throughput
    - not supported on Windows instances
    - `OS-Bypass` feature that can be used by EFA to bypass OS and achieve lower latency
        - Only supported in Linux
### EC2 Placement Groups
- Only certain types of instances can be launched in a placement group
- You cant merge placement groups
    - Have to stop instances to move them into another placement group
    - Can move using AWS CLI, AWS SDK but not via Console
- `Cluster Placement Groups` groups instances within a single AZ
    - Good for applications that communicate with each other
    - Low network latency, high network throughput
    - Should always have same type of instances within cluster placement group
- `Spread Placement Groups` groups instances on distinct underlying hardware
    - Can span multiple AZs
    - Good for small number of critical instances that should be kept separate
    - Used for individual critical instances
- `Partition Placement Groups` groups partitions (groups of instances) onto distinct underlying racks
    - Can span multiple AZs
    - Each group is divided into logical groups called partitions
    - Each rack has own network and power source
    - Isolates impact of hardware failure
    - Used for multiple critical instances such as HDFS, HBase, Cassandra
### EC2 Hibernation
- [Hibernation](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Hibernate.html) features that suspends an EC2 instance to disk. 
- Saves the contents from the RAM to the EBS root volume.
- Not possible to enable or disable hibernation for an instance after it has been launched
- Allows instance to boot much faster
- When resumed
    - EBS root volume is restored
    - RAM contents are reloaded, must be less than 150GB RAM
    - The processes that were previously running on the instance are resumed
    - Previously attached data volumes are reattached and the instance retains its instance ID
- Only some instance families are supported
- Can't be hibernated for more than 60 days
### Launch Templates
- `Launch Templates` specifies all the needed settings required to build an EC2 instance
    - Can configure once and deploy many times
        - Can configure
            - AMI
            - EC2 Instance size
            - Security groups
            - Networking Information, typically done via auto scaling group instead
    - Capable of auto scaling for all EC2 features
    - Supports versioning
    - More granular settings
    - Use this over Launch Configurations
- `Launch Configurations` predecessor to Launch Templates
    - Only Capable of auto scaling for certain EC2 features
    - Immutable, no versions
    - Limited settings
        - No networking information
    - Don't use
### EC2 Quotas
- [EC2 Quotas](https://docs.aws.amazon.com/general/latest/gr/ec2-service.html)
- Limited to running On-Demand Instances per your vCPU-based On-Demand Instance limit, 
- 20 Reserved Instances per month
- requesting Spot Instances per your dynamic Spot limit per region
## VMware cloud on AWS
- `VMWare Cloud on AWS` managed service that combines compute, network and storage capabilities in a fully supported, ready-to-run service from the creators of the software, VMware and the leading public cloud provider, AWS. 
- `Hybrid Cloud` connect to on-prem cloud to the AWS public cloud
- `Cloud Migration` migrate existing cloud environment to AWS
- `Disaster Recovery` allows inexpensive disaster recovery on AWS
- `Leverage AWS` use AWS service to update applications or crate new ones
- `vCenter` hosts that run on dedicated AWS hardware
    - Each can run 100s of VMware instances
    - Clusters have 2-16 hosts
## Outposts
- `Outposts` brings AWS data center to on-prem
- Allows AWS services on-prem
- Use for applications that must remain on-prem
    - generate near real-time responses to end-user applications.
    - communicate with other on-premises systems or control on-site equipment.
- Can extend any VPC in the Region to your Outpost by adding an Outpost subnet.
    - linked to a specific Availability Zone
    - can support multiple VPCs that can have one or more Outpost subnets
- `Outpost Racks` rack of servers
    - Large deployments, up to 96 42U–standard racks
    - Pool compute and storage capacity between multiple Outposts racks
    - Get more service option
    - can choose from a variety of Outposts configurations. 
        - Each configuration provides a mix of EC2 instance types and EBS volumes.
    - Installed by AWS
    - Supports EC2, ECS, SageMaker Edge Manager, IoT Greengrass, EKS, Elasticache, EMR, RDS, ALBs, Route 53, S3
- `Outpost servers` small individual servers
    - Small deployments, 1U Graviton-based processor or 2U Intel Xeon Scalable processor
        - Good for physical space constraints
    - Not all services available in Outposts racks are supported in Outposts servers.
    - Installed by you
    - Supports EC2, ECS, SageMaker Edge Manager, IoT Greengrass
- [local gateway](https://docs.aws.amazon.com/outposts/latest/userguide/outposts-local-gateways.html) enables connectivity between your Outpost subnets and your on-premises network
    - If internet connected (Direct Connect) can communicate with regional services or regional workloads
## Batch
- `Batch` managed service to run batch computing workloads within AWS
- Manages install, configuration and scaling
- Components:
    - `Job` unit of work submitted to batch
    - `Job Definitions` specify how jobs should be run
    - `Job Queues` jobs are submitted to specific queues
    - `Compute Environment` compute resources used to run jobs 
        - `Fargate` use for majority of workloads
            - Fast start times (<30s)
            - For jobs requiring less than 16 CPUs, no GPUs, <120GB
        - `EC2` use when need control over instance selection
            - For jobs that require
                - GPUs
                - Elastic Fabric Adapter
                - Custom AMIs
                - High levels of concurrency
                - Require access to Linux Parameters
- AWS Batch vs Lambda
    - Lambda has 15 minute execution limit, batch does not
    - Lambda has limited disk space and EFS requires VPC-enabled Lambda function (not ideal)
    - Lambda is fully serverless
    - Batch uses docker, any runtime can be used


# Module 5: Storage
## Storage Summary
![AWS Storage Options](/images/aws_storage_options.png)
- `Block Storage` Raw storage, data organized as an array of unrelated blocks.
- `File Storage` Unrelated data blocks managed by a file (serving) system. Native file system places data on disk.
- `Object Storage` Stores virtual containers that encapsulate the data, data attributes, metadata, and object IDs.
## Simple Storage Service (S3)
- `Simple Storage Service (S3)` object storage in the cloud
- scalable, allows you to store and retrieve any amount of data from anywhere in the world at a low cost
- simple, easy to use with a simple web interface
- S3 is a global service (like IAM)
- Safe place to store files
    - Data is spread across multiple devices and data centers
    - Availability (99.95% - 99.99% depending on tiers)
    - Durability (99.999999999%, 11 nines durability)
- Key, value store
    - Key = name of object (filename)
    - Value = data
    - Version ID = when versioning is enabled on S3
    - Metadata = data about the data (content-type, last-modified)
        - Retention period
- Upload any file type
    - Stores static files
    - Examples: photos, videos, code, documents, text files
    - Cannot be used to run an OS or database
- Unlimited storage, no limit on number of objects
- Objects can be up to 5TB in size
    - Single PUT limit 5GB
    - S3 console 160GB for a single object
    - Multipart upload allows larger objects
- `S3 Buckets` where files are stored, similar to a folder
    - Universal namespace, each S3 bucket name is globally unique
    - Example bucket name: https://bucket-name.s3.Region.amazonaws.com/key-name
    - When a file is uploaded, you will receive a 200 code if successful
- `Strong read-after write consistency` as soon as a write is performed any read requests receive the latest version of the object
- S3 can be used to host static webpage but not dynamic or those with database connections
    - The bucket name must always be the same as the domain name.
- S3 scales automatically 
- [Server access logging](https://docs.aws.amazon.com/AmazonS3/latest/userguide/ServerLogs.html) provides detailed records for the requests that are made to a buckets
    - Saves logs to S3
### S3 Cost Factors
- `Storage` – Per-gigabyte cost to hold your objects. You pay for storing objects in your S3 buckets. The rate that you’re charged depends on your objects' size, how long you stored the objects during the month, and the storage class. You incur per-request ingest charges when using PUT, COPY, or lifecycle rules to move data into any S3 storage class.
- `Requests and retrievals` number of API calls: PUT and GET requests.
    - costs are based on the request type, and are charged on the quantity of requests. 
    - When you use the Amazon S3 console to browse your storage, you incur charges for GET, LIST, and other requests that are made to facilitate browsing.
- `Data transfer` Usually no transfer fee for data-in from the internet and, depending on the requester location and medium of data transfer, different charges for data-out.
- `Management and analytics` pay for the storage management features and analytics that are activated on your account’s buckets.
- `S3 Replication and S3 Versioning` can have a big impact on your AWS bill.
- `Requester Pays` option for buckets where requester instead of the bucket owner pays the cost of the request and the data download from the bucket.
    - bucket owner always pays the cost of storing data. 
### Securing S3
- `Server-Side Encryption` enabled by default using SSE-S3 keys
    - `Server-side encryption with S3-managed keys (SSE-S3)` S3 managed keys, AES 256
        -  each object is encrypted with a unique key
        - encrypts the key itself with a primary key that it regularly rotates
    - ` Server-side encryption with KMS keys (SSE-KMS)` AWS management service-managed keys
        - Separate permissions for the use of a KMS key that provides added protection against unauthorized access of your objects in Amazon S3. 
        - provides you an audit trail that shows when your KMS key was used, and by whom
    - `Dual-layer server-side encryption with KMS keys (DSSE-KMS)` applies two individual layers of object-level encryption instead of one layer. 
        - Each layer of encryption uses a separate cryptographic implementation library with individual data encryption keys.
    - `Server-side Encryption with Customer-Provided Keys (SSE-C)` customer provided keys
        - S3 manages the encryption as it writes to disks and decryption when you access your objects
- `Client-Side Encryption` encrypt files before uploading them to S3
- `Encryption in transit` SSL/TLS, HTTPS
- Enforcing encryption
    - Bucket policy can deny PUT requests that don't include `x-amz-server-side-encryption`
- `Access Control Lists (ACLs)` defines which AWS accounts or groups are granted access 
    - Can be attached to individual objects in a bucket
- `Bucket Policies` defines what actions are allowed or denied
    - Type of Resource-based policy
    - Principal is user/service, resource is the bucket
    - Bucket wide
    - Can be used to make all items in bucket public
    - Controls access to a bucket without managing permissions in IAM
- Buckets are private by default, have to allow access on both bucket and objects to make public
### S3 Endpoints
- `S3 Access Points` simplify managing data access at scale for shared datasets in S3. 
- named network endpoints that you can use to perform S3 object operations, such as GetObject and PutObject.
- attached to buckets. 
- distinct permissions and network controls that S3 applies for any request that is made through that access point.
- Example: finance employee assumes the finance team IAM role and sends a GetObject request to your finance access point. With the access point policy, the finance role can get objects in doc-example-bucket with the prefixes /finance and /tax
### S3 Storage Classes
![S3 Storage Classes](/images/s3_storage_classes_table.png)
- S3 offers a range of storage classes designed for different use cases
- For all classes
    - Durability (99.999999999%, 11 nines durability)
- `S3 Standard` default storage class for S3
    - Latency: Milliseconds
    - Availability: 99.99%
    - Availability Zones: 3
    - Minimum storage duration: None
    - Cost: Highest
    - Uses:
        - Examples: Websites, content distribution, gaming applications, big data
- `S3 Standard-Infrequent Access (S3 Standard-IA/ S3-IA)` Infrequently accessed data that needs millisecond access
    - Latency: Milliseconds
    - Availability: 99.99%
    - Availability Zones: 3
    - Minimum storage duration: 30 days
    - Uses
        - Example: long-term storage, backups
- `S3 One Zone-Infrequent Access` Re-creatable infrequently accessed data
    - Latency: Milliseconds
    - Availability: 99.5%
    - Availability Zones: 1
    - Minimum storage duration: 30 days
    - Costs: 20% less than S3 Standard-IA
    - Uses:
        - non-critical data backups
- `S3 Express One Zone` High performance storage for your most frequently accessed data
    - Latency: single-digit Milliseconds
    - Availability: 99.95%
    - Availability Zones: 1
    - Minimum storage duration: 1 hour
    - access speeds up to 10x faster and with request costs 50 percent lower
    - Commonly used with other AWS services to support analytics and artificial intelligence and machine learning (AI/ML) workloads
        - EMR
        - SageMaker
        - Athena
- `S3 Intelligent Tiering` Automatic cost savings for data with unknown or changing access patterns
    - Latency: Milliseconds
    - Availability: 99.99%
    - Availability Zones: 3
    - automatic storage cost savings when data access patterns change, without performance impact or operational overhead
        - Automatically moves data to the most cost-effective access tier when access patterns change
    - no retrieval charges 
- `S3 Glacier` way of archiving data long term
    - Pay for each access
    - Used only for archiving data
    - `Glacier Instant Retrieval` long-lived data that is accessed a few times per year with instant retrievals
        - Latency: Milliseconds
        - Availability: 99.9%
        - Availability Zones: 3
        - Minimum storage duration: 90 days
        - Uses
            - Critical data accessed infrequently
    - `Glacier Flexible Retrieval` Backup and archive data that is rarely accessed and low cost
        - Latency: Minutes to 12 hours
        - Availability: 99.99%
        - Availability Zones: 3
        - Minimum storage duration: 90 days
        - Cost: Low Cost
        - Uses
            - Backup or disaster recovery
    - `Glacier Deep Archive` Archive data that is very rarely accessed and very low cost
        - Latency: 12 to 48 hours
        - Availability: 99.99%
        - Availability Zones: 3
        - Minimum storage duration: 180 days
        - Cost: Very Low Cost
### S3 Lifecycle management
- `Lifecycle management` define rules to automatically transition objects to cheaper storage classes or delete after a set period of time
- Can move different versions to different storage tiers
- Lifecycle policies can't work backwards, can move back from less-frequently accessed storage classes (Glacier to Standard-IA)
### Glacier Archive Retrieval Options
- [Retrieving from Glacier](https://docs.aws.amazon.com/amazonglacier/latest/dev/downloading-an-archive-two-steps.html) is `Asynchronous operation` you first initiate a job, and then download the output after the job is completed.
- `Bulk retrievals` lowest-cost option, which you can use to retrieve large amounts, even petabytes, of data inexpensively in a day. 
    - completed within 5–12 hours.
- `Standard retrieval` access within several hours
- `Expedited retrievals` allow you to quickly access your data when occasional urgent requests for a subset of archives are required. 
    - For all but the largest archives (250 MB+)
    - available within 1–5 minutes. 
    - `Provisioned Capacity` ensures that retrieval capacity for Expedited retrievals is available when you need it
        - Each unit of capacity provides that at least three expedited retrievals can be performed every five minutes and provides up to 150 MB/s of retrieval throughput. 
### S3 Versioning
- All versions are stored in S3
- Good for backups
- Cannot be disabled, can only be suspended
    - Even if an object is deleted it is still there
- Lifecycle rules can be integrated
- Can enable MFA to delete objects
- Previous versions are not made public by default
### S3 Batch Operations
- [Batch Operations](https://docs.aws.amazon.com/AmazonS3/latest/userguide/batch-ops.html) S3 data management feature that lets you manage billions of objects at scale with just a few clicks in the Amazon S3 Management Console or a single API request. 
- Uses 
    - Transcoding video files 
    - Encrypting objects 
    - used storage metadata to create batches of objects that we could move to S3 Glacier
    - set object tags
    - Set access control lists (ACLs)
- CSV Object Lists – If you need to process a subset of the objects in a bucket and cannot use a common prefix to identify them, you can create a CSV file and use it to drive your job
### S3 Object Lock and Glacier Lock
- `S3 Object Lock` used to store objects using write once, read many (WORM) model
    - Prevents objects from being deleted or modified for a fixed amount of time or indefinitely 
    - Used to meet regulatory requirements or add extra protection
    - `Governance Mode` users can't overwrite or delete an object version or alter it's locker settings unless they have special permissions
        - Protects against alteration by most users
        - Can grant some users permission to alter retention settings
    - `Compliance Mode` nobody can overwrite or deleted by any users, including root user
        - Only applies for duration of retention period
    - `Legal Hold` prevents an object version from being overwritten or deleted
        - Similar to a retention period but no set time period
        - It's there until removed
- [S3 Glacier Vault Lock](https://docs.aws.amazon.com/amazonglacier/latest/dev/vault-lock.html) easily deploy and enforce compliance controls for individual S3 Glacier vaults
    - Once locked the policy can no longer change
    - WORM model
    - Used for compliance
### S3 Performance
- `S3 Prefixes` folders inside out buckets
    - Example: mybucketname/folder1/subfolder1/myfile.jpg 
        - Prefix is /folder1/subfolder1/
    - 5,500 reads per prefix
    - Can get better performance by spreading your reads across different prefixes
- If using SSE-KMS your objects must keep within the KMS limits
    - Region specific
    - Uploading/download counts as a request
    - SSE-S3 has no limit so should be used to fix this issue
- `Multipart uploads` parallel uploads for large files
    - required for files over 5GB
    - Changes in code are required to be able to upload files using S3 multipart upload.
- [Transfer Acceleration](https://docs.aws.amazon.com/AmazonS3/latest/userguide/transfer-acceleration.html) bucket-level feature that enables fast, easy, and secure transfers of files over long distances between your client and an S3 bucket. 
    - uses edge locations to facilitate fast data transfer
    - Allows transfer gigabytes to terabytes of data on a regular basis across continents. 
    - Used when You are unable to utilize all of your available bandwidth over the Internet when uploading to Amazon S3.
- `S3 Byte-range Fetches` parallel downloads of partial parts of a file
    - If a download fails it's only within that byte-range
### S3 Replication and Backups
- [S3 Replication](https://docs.aws.amazon.com/AmazonS3/latest/userguide/replication.html) automatic, asynchronous copying of objects across S3 buckets.
- Must be enabled on both source and destination buckets
- Replication requires versioning to be enabled for both buckets
- Objects in an existing bucker are not replicated automatically
- Delete markers are not replicated by default
- Need to specify an IAM role that S3 can assume to replicate objects on your behalf
- destination buckets can be in different AWS Regions or within the same Region as the source bucket.
- `Same-Region Replication (SRR)` is used to copy objects across Amazon S3 buckets in the same AWS Region
    - Aggregate logs into a single bucket 
    - Configure live replication between production and test accounts
    - Abide by data sovereignty laws
- `Cross-Region Replication (CRR)` is used to copy objects across Amazon S3 buckets in different AWS Regions
    - Meet compliance requirements
    - Minimize latency
    - Increase operational efficiency
- `two-way replication (bi-directional replication)`
    - Build shared datasets across multiple AWS Regions
    - Keep data synchronized across Regions during failover
    - Make your application highly available
- `S3 Batch Replication` replicates existing objects to different buckets as an on-demand option
    - replicate objects that were added to the bucket before Same-Region Replication or Cross-Region Replication were configured.
    - Replicate objects that previously failed to replicate
### S3 Event Notifications
- [S3 Event Notifications](https://docs.aws.amazon.com/AmazonS3/latest/userguide/EventNotifications.html) receive notifications when certain events happen in your S3 bucket
- Send event notification messages to SNS, SQS, Lambda, EventBridge
- can publish notifications for the following events:
    - New object created events
    - Object removal events
    - Restore object events
    - Reduced Redundancy Storage (RRS) object lost events
    - Replication events
    - S3 Lifecycle expiration events
    - S3 Lifecycle transition events
    - S3 Intelligent-Tiering automatic archival events
    - Object tagging events
    - Object ACL PUT events
### S3 Select
- [S3 Select](https://docs.aws.amazon.com/AmazonS3/latest/userguide/selecting-content-from-objects.html) use SQL statements to filter the contents of an Amazon S3 object and retrieve only the subset of data that you need
- works on objects stored in CSV, JSON, or Apache Parquet format
- works with objects that are compressed with GZIP or BZIP2 
- works with Server-side encrypted objects
## Elastic Block Storage (EBS)
- `Input Output Per Second (IOPS)` number of reads and write operations per second, ability to action reads and writes quickly
    - Important for quick transactions
- `Throughput` number of bits read or written per second 
    - Important for large datasets
- `Elastic Block Storage (EBS)` block-level storage volumes that you can attach to EC2 instances
- Can be attached to multiple EC2 instances
- Virtual hard disk in the cloud
- Production/Mission-critical workloads
- High availability, automatic replication within a single AZ
- Scalable, can dynamically increase size with no downtime
- support live configuration changes while in production which means that you can modify the volume type, volume size, and IOPS capacity without service interruptions. 
- [EBS Multi-Attach](https://tutorialsdojo.com/amazon-ebs-multi-attach/) allows EC2 instances to share a single EBS volume for up to 16 instances and provide higher availability of your applications for Linux workloads. 
    - Each instance to which the volume is attached has full read and write permissions to the volume.
    - supported exclusively on Provisioned IOPS SSD (io1 or io2) volumes.
    - Only available in a few regions
- `DeleteOnTermination` attribute for each attached EBS volume determines whether to preserve or delete the volume
- Default, set to True for the root volume and False for all other volume types.
- `Magnetic HDD` workloads with smaller datasets where data is accessed infrequently or when performance consistency isn't of primary importance
    - 100 IOPS on average
- `General Purpose SSD (GP2)` good for applications that are not latency sensitive
    - boot volumes or development
    - 3 IOPS per GiB up to 16k IOPS
    - Up to 3k IOPS for volumes smaller than 1TB
- `General Purpose SSD (GP3)` good for applications that require high performance at a low cost
    - MySQL, Cassandra, Virtual desktops and Hadoop
    - 4x faster than gp2
    - 3k IOPS regardless of size
    - Can scale up to 16k IOPS for a fee
- `Provisioned IOPS SSD (io1)` high performance and most expensive option
    - Designed for I/O intensive applications, large databases and latency sensitive workloads
- `Provisioned IOPS SSD (io2)` latest generation, higher durability and more IOPS
    - Same price as io1
    - Up to 64K IOPS
- `Provisioned IOPS SSD (io2 Block Express)` highest-performance SSD volume designed for business-critical latency-sensitive transactional workloads.
    - Highest iops
- `Throughput Optimised HDD (st1)` low cost HDD volume
    - Frequently accessed, throughput-intensive workloads
    - Big data, data warehouse, ETL, log processing
    - Cannot be a boot volume
    - 500 IOPS limit
- `Cold HDD (SC1)` Lowest cost option
    - Good for infrequently accessed data and where performance is not a factor
    - sequential I/O operations
    - Throughput rather than IOPS
### EBS Volumes and snapshots
- `Volume` virtual hard disks
    - Need at leats 1 volume per EC2 instance
    - Volumes are stored on EBS
    - Always in the same AZ as the attached EC2
    - Can switch volume type whilst an EC2 is running
- `Snapshots` copy of the virtual disk at a point in time
    - Save incremental changes only, data changed since last snapshot
    - Stop instance to get a consistent snapshot
    - Encrypted by default
    - Migrating/backups of a snapshot
        - share snapshots inside a region
        - need to be copied to another region first
    - Snapshots are stored on S3
### EBS Encryption
- `Not Encrypted by default`, encryption can be applied to your volume with a data key using industry-standard AES-256 data encryption
    - Data at rest inside the volume
    - All data moving between the volume and the instance
    - All snapshots created from the volume
    - All volumes created from those snapshots
- When you encrypt on volume, the following is encrypted
    - Data inside the volume 
    - All data moving between an instance and volume 
    - All snapshots
    - All volumes created from snapshots
- How to encrypt
    - Create a snapshot of the unencrypted volume
    - Create a copy of the snapshot and select the encrypt option
    - Create an AMI for the encrypted snapshot
    - Use that AMI to launch new encrypted instances
## Elastic File System (EFS)
- `Elastic File System (EFS)` managed Network File System that can be mounted on many EC2 instances at once
- Works with EC2 instances in multiple AZs within a region
- POSIX-compliant
- Supports Network File System version 4 (NFSv4)
- Highly available and scalable
    - Replicated across 3 AZs 
- Expensive, pay per use
- Good for web servers, content management systems
- Scales automatically up to petabytes
- 1000s concurrent connections
- Read-after-write consistency
- Can chose Performance Characteristics
    - `General Purpose` web servers, CMS
    - `Max I/O` big data, media processing
- [Storage Classes](https://aws.amazon.com/efs/storage-classes/):
    - `Standard` for frequently accessed files
        - Latency: Sub-millisecond
        - `Standard One Zone` Stored within a single AZ
    - `Infrequent Access` for infrequently accessed files
        - Latency: Tens of milliseconds
        - `Infrequent Access One Zone` Stored within a single AZ
    - `EFS Archive` cost-optimized for data that is accessed only a few times
        - Latency: Tens of milliseconds
        - Minimum Storage Duration: 90 days
## FSx
- `FSx` is a fully managed third-party file system solution.
- uses SSD storage to provide fast performance with low latency.
- Supports identity-based authentication over the Server Message Block (SMB) protocol through Microsoft Active Directory.
- Automatically encrypts your data at-rest using AWS KMS and in-transit using SMB Kerberos session keys. 
- `FSx for Windows` fully managed native Microsoft Windows File system
    - Allows easy migration from Windows, Share Point, IIS
    - Supports Active Directory Users
    - `Robocopy` is a command-line file transfer utility for Microsoft Windows.
- `FSx for Lustre` fully managed file system optimised for compute-intensive workloads
    - High performance computing
    - Good for massive data sets that need 100s GBs throughput, millions of IOPS and sub-millisecond latencies
    - Can store data directly on S3
- `FSx for NetApp ONTAP` shared file storage solution that provides high-performance SSD storage with sub-millisecond latency and is widely accessible from Linux, Windows, and macOS compute instances running on AWS or on-premises.
    - Supports multi-protocol access to data using NFS, SMB, and iSCSI.
    - `NetApp SnapMirror` replicates snapshot copies onto the same system, same or different cluster, or to the cloud
        - Use for replication
- `FSx for OpenZFS` file storage service that delivers up to 1 million IOPS with latencies of hundreds of microseconds.
    - Graviton family of processors
    - accessible through the NFS protocol 
## Amazon Machine Images (AMI)
- `Amazon Machine Images (AMI)` provides the information required to launch an instance
- can include block device mapping that specifies the volumes to attach to the Amazon EC2 instance when it is launched.
- `Quick Start Amazon Machine Image (AMI)` used to create any instance type.
- Options include
    - Region
    - OS
    - Architecture
    - Launch permissions
    - Storage for the root device
- Need to copy AMI to another region before it can be used
    - Create a mapping in the CloudFormation template. Define the unique AMI value per region.
- `Custom AMIs` preconfigured with your operating system of choice, plus the appropriate pieces of the application stack.
    - configure and identify your own AMIs so that they can launch as part of your recovery procedure.
- Either backed by 
    - `EBS` volume created from EBS snapshot
        - Consistent and permanent
    - `Instance Store` temporary block-level storage for your instance.
        - located on disks that are physically attached to the host computer.
        - ideal for temporary storage of information that changes frequently
        - created from a template stored in Amazon S3
        - Doesn’t support snapshots
        - random IOPS
        - Ephemeral storage: cannot be stopped, not saved if the instance is terminated or the host fails
            - Persists during reboot
        - data in the instance store is lost under any of the following circumstances:
            - The underlying disk drive fails
            - The instance stops
            - The instance terminates
- `Data Lifecycle Manager` service used to automate the creation, retention, and deletion of EBS snapshots and EBS-backed AMIs
## Backup
- `Backup` managed service that allows you to consolidate backups across multiple AWS services
- Storage: EC2, EBS, EFS, FSx for Lustre, FSx for Windows, AWS storage gateway
- Databases: RDS, DynamoDB, Aurora
- Can be used with AWS organisations
- Central management across AWS services
- Stores periodic backups incrementally.
- Lifecycle policies allow deletion of backups
- Compliance
- works with AWS Organizations
    - centrally deploys data protection policies to configure, manage, and govern your backup activity
- Can create backups across regions and accounts
- IAM role required for Backup to access resources
- `Backup plan` policy expression that determines when and how you want your AWS resources backed up.
    - Schedule 
    - Lifecycle 
    - Vault 
    - Tags for the backups
- `Backup vault` container to store and organize your backups.
    - `Backup Vault Lock` allows you to enforce retention periods and prevent early deletions.
- Policy-based and tag-based Backup access policies
    - `Tags` all AWS resources with that tag will be backed up using this plan
    - `Resource IDs` can use Resource IDs for specific resources, such as a specific DynamoDB table or Amazon EBS volume.
- Automated backup scheduling
- Good for compliance
    - Monitoring and logs of centralized backup activity
    - Encrypted backups
    - Backup access policies
- Costs
    - Automated management of backup retention
    - No added cost for orchestration
    - Amount of backup storage you use.
    - Amount of backup data that has been transferred between AWS Regions.
    - Amount of backup data you restore.    
    - Number of backup evaluations.
- Monitoring
    - works with CloudWatch, EventBridge, CloudTrail, and SNS to monitor workloads
## WorkDocs
- [WorkDocs](https://docs.aws.amazon.com/managedservices/latest/userguide/workdocs.html) is a fully-managed, secure content creation, storage, and collaboration service.
## WorkSpaces
- [WorkSpaces](https://aws.amazon.com/workspaces/) Fully managed, secure, reliable virtual desktop solutions for every workload
- Windows, Amazon Linux, or Ubuntu Linux 


# Module 6: Databases
## Relational Database Service (RDS)
- `Relational Database Service (RDS)` collection of managed services that makes it simple to set up, operate, and scale databases in the cloud
- Automatically provisions and maintains a synchronous standby replica in a different AZ
- Can be spread across multiple AZ's
    - Exact copy in another AZ
    - Amazon Aurora is Multi-AZ by default, others aren't
    - Can only connect to primary database, secondary DB is there in case of failure
- Has failover capability
    - One to two minutes
    - CNAME is switched from the primary db instance to the secondary
- Can stop an Amazon RDS database instance for up to seven days at a time
- Used for online transaction processing (OLTP), real-time transactions
- Not suitable for Online Analytical Processing (OLAP)
    - Not suitable for analysing large amount of data
    - Use data warehouse, Redshift
- Available Database Engines
    - SQL Server
    - Oracle
    - MySQL
    - PostgreSQL
    - MariaDB
    - Amazon Aurora
- `Read Replicas` read-only copy of your primary DB
    - Improves performance, takes load of primary DB
    - Not for disaster recovery
    - Requires automatic backups
    - Can be in same AZ or cross-region
    - Can promote a read replica to a primary DB
    - Good for serverless architectures that have a large number of open connections 
    - allows applications to pool and share connections established with the database, improving database efficiency and application scalability.
- can choose to use on-demand DB instances or reserved DB instances
### RDS Backups
- [Automated backups](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_WorkingWithAutomatedBackups.html) storage volume snapshot of your DB instance or Multi-AZ DB cluster during the backup window of your DB instance
- maximum backup retention period for automated backup is only 35 days
    - Create an AWS Backup plan to take daily snapshots with a longer retention period
- Your DB instance must be in the available state for automated backups to occur. 
- don't occur while a DB snapshot copy is running in the same AWS Region for the same database
- `Point-in-time Restores` restore your DB instance to any specific time during the backup retention period
- Save a `manual database (DB) snapshot` or a DB cluster snapshot in a separate Region.
    - Share a manual snapshot with up to 20 other AWS accounts
### RDS Instance Storage
- [RDS instance storage](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_Storage.html) EBS provides durable, block-level storage volumes that you can attach to a running instance. 
- Storage Types
    - General Purpose (SSD)
    - Provisioned IOPS (PIOPS)
    - Magnetic
### RDS Proxy
- `RDS Proxy` fully managed database proxy for RDS that makes applications more scalable, more resilient to database failures, and more secure.
-  allow your applications to pool and share database connections to improve their ability to scale
- automatically connecting to a standby DB instance while preserving application connections.
- handle unpredictable surges in database traffic.
- queues or throttles application connections that can't be served immediately from the connection pool
- reduce the overhead to process credentials and establish a secure connection for each new connection
### RDS Multi-AZ
- [Multi-AZ DB instance](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.MultiAZSingleStandby.html) deployment has the following characteristics:
    - single standby DB instance.
    - automatically provisions and maintains a synchronous standby replica in a different Availability Zone. 
    - The primary DB instance is synchronously replicated across AZs to a standby replica to provide data redundancy and minimize latency spikes during system backups
    - In the event of a failure, RDS automatically switches to a standby replica
        - 60–120 seconds to complete
- [Multi-AZ DB cluster](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/multi-az-db-clusters-concepts.html) semisynchronous, high availability deployment mode of Amazon RDS with two readable replica DB instances
    - writer DB instance and two reader DB instances in three separate Availability Zones in the same AWS Region
    - high availability, increased capacity for read workloads, and lower write latency when compared to Multi-AZ DB instance deployments.
    - failover in typically under 35 seconds 
### RDS Auto Scaling
- `RDS Auto Scaling` automatically scales storage capacity in response to growing database workloads, with zero downtime.
- Continuously monitors actual storage consumption, and scales capacity up automatically when actual utilization approaches provisioned storage capacity. 
- works with new and existing database instances.
### RDS on Outposts
- [RDS on AWS Outposts](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/rds-on-outposts.html) extends databases to AWS Outposts environments
- Uses the same hardware as in public Regions
## Aurora
- `Aurora` MySQL and PostgreSQL compatible relational database engine that combines speed and availability with simplicity and cost-effectiveness of open-source databases
- higher availability and better durability than RDS
    - 2 copies of stored in each AZ, minimum of 3 AZ's, 6 copies minimum
- Can share aurora snapshots with other AWS accounts
- ACID compliant 
- helps to reduce your database costs by reducing unnecessary I/O operations, while ensuring that your database resources remain reliable and available
- Better performance than RDS
    - 5x performance than MySQL
    - 3x performance than PostgreSQL
- Minimum 10GB size, then scales in 10GB increments up to 128TB
- Backups always enabled, do not impact performance
- [Endpoints](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.Overview.Endpoints.html) can be used to map connections to appropriate instances or instance groups
    - `Cluster endpoints/writer endpoints` connects to the current primary DB instance for that DB cluster
    - `Reader endpoint` provides load-balancing support for read-only connections to the DB cluster
    - `Custom endpoints` connections to a set of DB instances that you choose
    - `Instance endpoint` connects to a specific DB instance within an Aurora cluster
- `Aurora Backups` automatically backs up and retains restore data for the length of the backup retention period
    - maximum backup retention period for automated backup is only 35 days.
        - Use Backup plan to take daily snapshots with a longer retention period
### Aurora DB Clusters
- `Aurora DB cluster` consists of one or more DB instances and a cluster volume that manages the data for those DB instances. 
- The instances perform the compute functions of the database while the cluster volume stores the actual data.
- instance types:
    - `Primary instance` Supports read and write operations and performs all the data modifications to the cluster volume. 
        - One per cluster
    - `Aurora replica` Supports read operations only. 
        - can have up to 15 Aurora replicas in addition to the primary instance. 
        - Multiple Aurora replicas distribute the read workload.
        - You can increase availability by locating Aurora replicas in separate Availability Zones. 
        - You can have a read replica in the same Region as the primary instance.
        - Automated failover only available with this type
    - `MySQL Replicas` 5 read replicas
    - `PostgreSQL Replicas` 5 read replicas
- `Aurora cluster volume`virtual database storage volume that spans multiple Availability Zones. 
    - Each Availability Zone has a copy of the DB cluster data. 
    - Storage in the cluster volume is replicated across hundreds of storage nodes. 
    - Aurora presents the cluster volume as a single, logical volume to the primary instance and to Aurora replicas in the DB cluster. 
    - Write operations to the cluster volume are often available to Aurora replicas in less than 100 milliseconds.
### Aurora Serverless
- `Aurora Serverless` serverless DB cluster that automatically starts, shuts down and scales capacity
- Automatic capacity adjustment based on application demands
- Simple cost-effective option for infrequent and unpredictable workloads
    - Per-second billing based on resources consumed by DB clusters 
- valuable for multi-tenant databases, distributed databases, development and test systems, and other environments with highly variable and unpredictable workloads
- `Aurora Capacity Units (ACU)` measurement on how your clusters scale
    - can specify a lower and upper capacity limit
    - higher the current capacity, the faster it can scale up
    - each ACU is 2GB memory, matching CPU and networking
    - Set a min and max ACU, can be zero
    - Allocated quickly by warm pools
- 2 copies of stored in each AZ, minimum of 3 AZ's, 6 copies minimum
- Uses
    - Capacity planning
    - Mixed-use apps
    - Dev and test
    - Variable workloads
    - Multi-tennant apps
    - New apps
### Aurora Global Database
- `Aurora Global Database` allows a single Aurora database to span multiple AWS regions
- Replicates data with no impact on performance
- Designed for globally distributed applications
- low latency global reads 
- disaster recovery from region-wide outages. 
- RPO of 1 second and RTO of less than 1 minute
### Aurora Auto scaling
- `Aurora Auto scaling` dynamically adjusts number of replicas in a DB Cluster
- works with CloudWatch to automatically add and remove Replicas in response to changes in performance metrics that you specify
- `Instance scaling` scale your Aurora DB cluster by modifying the DB instance class for each DB instance in the DB cluster.
- `Read scaling` as your read traffic increases, you can create additional Aurora Replicas and connect to them directly to distribute the read load for your DB cluster.
## DynamoDB
- `DynamoDB` managed serverless noSQL database
- stores data in tables
    - When creating a table, you must specify a table name and a partition key
        - Use partition keys with high-cardinality attributes, which have a large number of distinct values for each item.
- Primary Keys
    - `Simple primary key` composed of just one attribute, which is designated as the partition key. If you use only the partition key, no two items can have the same value.
    - `Composite primary key` composed of both a partition key and a sort key. In this case, the partition key value for multiple items can be the same, but their sort key values must be different
        - `high cardinality` attributes have distinct values for each item
            - useful for creating efficient partition keys
            - `Low cardinality` attributes are typically not suitable for partition keys
- Availability
    - Replicated across 3 AZs
- Consistency
    - `Eventual consistent reads by default` consistency reached within 1 second
    - `Strongly consistent reads (opt-in)` returns a result that reflects all writes
- Pay-per-request pricing
    - No minimum capacity
    - Use for new product launches
- `DynamoDB Streams` first-in first out, time ordered sequence of item level 
- `DynamoDB Transactions`
    - Use for financial transactions, managing orders, game engines, coordination between services
    - 3 options for reads:
        - eventual consistency
        - strong consistency
        - transactional
    - 2 Options for writes
        - standard
        - Transactional
    - Provides ACID across 1 or more tables within a single AWS account and region
    - `Atomic, Consistent, Isolated, Durable (ACID)` all or nothing
        - `Atomic` all changes performed to DB must be performed successfully or not at all
        - `Consistent` data must be in a consistent state before and after the transaction
        - `Isolated` no other process can change the data while the transaction is running
        - `Durable` the changes made by a transaction must persist
changes in a table
    - Data is broken up into shards
    - Every shard is stored for 24 hours 
    - Can be combined with Lambda for stored procedure functionality
- `Time To Live (TTL)` cost-effective method for deleting items that are no longer relevant.
- Use cases
    - Player profile page
    - Online shopping cart
### DynamoDB Auto scaling
- `DynamoDB auto scaling` is enabled for that table by default
    - dynamically adjusts provisioned throughput capacity on your behalf, in response to actual traffic patterns.
    - Should apply auto scaling uniformly to all global secondary indexes
    - doesn’t prevent you from manually modifying provisioned throughput settings
- `scaling policy` specifies whether you want to scale read capacity or write capacity (or both), and the minimum and maximum provisioned capacity unit settings for the table or index.
    - `target utilization` the percentage of consumed provisioned throughput at a point in time.
### DynamoDB Accelerator (DAX)
- `DynamoDB Accelerator (DAX)` caching system specifically for DynamoDB
- Used to No-SQL databases such as DynamoDB
- In memory cache, millisecond to microsecond response times
- Lives inside the VPC you specify
- Can configure node size, count for cluster TTL for data, maintenance windows
### DynamoDB Global Tables
- `DynamoDB Global Tables` managed multi-master, multi-region replication
- Multi-region redundancy for disaster recovery or high availability
- Under 1 second replication across regions
- Requires DynamoDB streams enabled
- fast and localized read and write performance for massively scaled global applications.
- can only have one replica table per Region, and every replica has the same table name and the same primary key schema.
### DynamoDB Backups
- `DynamoDB Backups` full backups at anytime with no performance impact
- Retained until deleted
- Same region as source table
- Use AWS Backup to automatically copy the on-demand DynamoDB backups to another AWS account for disaster recovery
### DynamoDB Point-in-time recovery
- [Point-in-time recovery](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/PointInTimeRecovery.html) protects against accidental writes or deletes
    - Restore to any point within from last 5 minutes to last 35 days
    - Not enabled by default
### DynamoDB Security
- Default, DynamoDB manages keys for you 
    - No additional charge
    - Provides encryption at rest
- Optionally, store in KMS or Customer-managed
    - Additional charge
## DocumentDB
- `DocumentDB` allows you to run MongoDB on the AWS cloud
    - managed document database that scales with your workloads
    - Backups automatically
    - Don't need to manage MongoDB cluster
## Keyspaces
- `Keyspaces` allows you to run Apache Cassandra database service
    - managed database that scales with your workloads
    - Backups automatically
## Neptune
- `Neptune` allows you to run a graph database service
- managed database that scales with your workloads
- Connections between identities, Knowledge graph, fraud patterns, security graphs
- Provide milliseconds latency when querying the graph.
- supports graph query languages like Apache TinkerPop Gremlin and W3C’s SPARQL.
- replicated six ways across three availability zones
- Automated backups are always enabled.
- does not support cross-region replicas
- Encryption of an existing Neptune instance is not supported
- `Neptune Streams` generate a complete sequence of change-log entries that record every change made to your graph data as it happens
## Quantum Ledger Database (QLDB)
- `Quantum Ledger Database (QLDB)` allows you to run a ledger database service
    - Ledger database is a immutable, transparent, cryptographically verifiable transaction log owned by one authority
    - Cannot update a record, update adds a new record
    - Used for crypto, shipping companies, financial transactions, centralise records
    - managed database
## Timestream
- `Timestream` allows you to run a time-series database service
    - managed database
    - Time series data: data points that are logged over a series of time
    - Temperature readings, IoT sensors, analytics, DevOps applications
    - 1,000 times faster than a traditional relational databases
## ElastiCache
- `ElastiCache` managed version of Memcached and Redis caching technologies
- internal caching system that site in front of databases
- `Memcached` simple database caching solution
    - Not a database by itself
    - No failover
    - No backups
    - Multi-threaded performance
    - Uses:
        - web
        - mobile apps
        - gaming
        - ad tech
        - ecommerce. 
- `Redis` caching solution and standalone database
    - `Redis AUTH` used for better security, requires password 
    - Failover support
    - Multi-AZ support
    - Backups
    - Advanced data types
    - Sorting and ranking datasets 
    - Publish and subscribe capability 
    - Backup and restore
    - Uses
        - real-time applications in gaming, ad tech, e-commerce, healthcare, financial services, and Internet of Things 
### Caching Strategies
- [Caching Strategies](https://docs.aws.amazon.com/AmazonElastiCache/latest/mem-ug/Strategies.html)
    - `Lazy Loading` loads data into the cache only when necessary
        - In the case of a cache miss, the information that is `retrieved from the database` can be subsequently written to the cache. 
        - loads data that the application needs into the cache
        - can result in high cache-miss-to-cache-hit ratios in some use cases
    - `Write through` adds data or updates data in the cache whenever data is `written to the database`
        - results in fewer cache misses, improved performance
        - requires additional storage for data that the applications might not need.
- `Time to live (TTL)` is an integer value that specifies the number of seconds until the key expires.
    - doesn't guarantee that a value isn't stale, keeps data from getting too stale and requires that values in the cache are occasionally refreshed from the database.

# Module 7: Monitoring & Scaling
## Scaling
- `Vertical Scaling` resizing an individual instance
    - Only works to a certain point
- `Horizontal Scaling` creating many different smaller instances rather than a single large one
    - High availability
- Questions to ask
    1. Is it highly available?
        - Pick answers that include high availability unless specific focus on cost
    2. Is horizontal or vertical scaling more appropriate?
        - Focus on horizontal scaling as it scales more easily and is more highly available
        - Vertical scaling is useful for instance specific issues, network throughput etc.
    3. Is the scaling cost effective?
        - Balance, don't overkill the solution
    4. Would switching database solve the issue?
        - Would no-SQL/DynamoDB work better?
- Get ahead of the workload where possible, use predictive scaling rather than reactive where possible
    - Spin up predictive ahead of time for rush rather than playing catchup
- Bake AMIs to reduce build times, put everything in an AMI rather than use user data
- Spread Auto scaling over multiple AZs
- `Steady state groups` allow us to create a situation where a single failure can recover
    - Min, max, desired are set to 1
    - Useful when their can't be more than a single instance at a time
- Load Balancers are essential
    - Enable health checks from load balancers otherwise instance won't be replaced when they fail health checks
## Auto Scaling
- `Auto Scaling`monitors your applications and automatically adjusts capacity to maintain steady, predictable performance at the lowest possible cost. 
- Required components 
    - `Launch templates`
    - `Auto scaling policy`
    - `Auto scaling groups` groups of instances
        - Can be across AZs
- lets you build scaling plans for
    - EC2 instances and Spot Fleets
    - ECS tasks
    - DynamoDB tables and indexes
    - Aurora
- Registers new instances with load balancers, when specified
- Cloudwatch alarms can be used to tell us when to add more resources
### Auto Scaling Policies
- CloudWatch & Health Checks are primarily used to alert Auto Scaling that you need more resources
- Scaling Policies:
    - `Step Scaling` applies stepped adjustments to vary the scaling depending on the size of the alarm breach
        - Example:
            - Scaling out
                - Add 10 when memory is between 60-80%
                - Add 5 when memory is between 80-100%
            - Scaling in
                - Terminate 10 when memory is between 40-20%
                - Terminate 15 when memory is between 20-0%
    - `Simple Scaling` relies on metrics for scaling needs
        - Example: Add 1 instance if CPU utilisation metric > 80%
    - `Target Tracking` uses a scaling metric and value that your ASG should maintain at all times
        - Example: maintain ASGAverageCPUUtilisation = 50%
- `Instance warmup` Stops instances from being placed behind the load balancer, failing the health check and being terminated early
    - Helps avoid thrashing
    - Keep an eye on provisioning times
        - Bake AMIs to reduce
- `Instance Cool down` Pauses auto scaling for a set amount of time, helps to avoid runaway scaling events
    - Helps avoid thrashing
    - default value is 300 seconds. 
- Scaling Types
    - `Dynamic Scaling` playing catchup, once load is there measure it and determine if you need more
    - `Scheduled Scaling` crate scaling event to get your resources ready to go before they are needed
        - For predictable workloads
    - `Predictive Scaling` AWS used ML to determine when you'll need to scale
        - Scaling forecasts are revaluated every 24 hours to forecast for next 48 hours
        - Cyclical traffic, such as high use of resources during regular business hours and low use of resources during evenings and weekends
        - Recurring on-and-off workload patterns, such as batch processing, testing, or periodic data analysis 
        - Applications that take a long time to initialize, which causes a noticeable latency impact on application performance during scale-out events
- How to keep costs down
    - Use EC2 Reserved instances and compute saving plans for minimum counts
### EC2 Auto Scaling
- `EC2 Auto Scaling` helps you maintain application availability and lets you automatically add or remove EC2 instances using scaling policies that you define. 
- `Auto Scaling Groups` collection fo EC2 instances that are treated as a collective group for the purposes of scaling and management
- `EC2 Fleet` define a combination of EC2 instance types to make up the desired capacity of your group.
    - capacity is defined as a percentage of each type of purchasing option. 
    - maintain the desired cost optimization as your group scales in or out. 
    - Groups that are made up of mixed fleets still support the same lifecycle hooks, instance health checks, and scheduled scaling as a single-fleet group.
    - [Spot Fleet](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/spot-fleet.html) is a set of Spot Instances and optionally On-Demand Instances that is launched based on criteria that you specify.
- auto scales networking, where instances will reside
- Need to select a Load Balancer for instances to live behind
- Steps
    1. Define Launch Template or Launch Configuration
    2. Pick Network and purchasing options
        - Picking multiple AZs allows for high availability 
    3. Load Balancer Configuration: EC2 instances can be registered behind an Load Balancer
        - Auto scaling group can be set to respect Load Balancer health checks
    4. Scaling Policy
        - Minimum, maximum and desired capacity
    5. Notifications: SNS notifications, let you know when a scaling event occurs
- `Lifecycle Hooks` perform custom actions on instances when lifecycle events occur
    - Wait for up to 2 hours
    - `Scaling out hooks` installing/configuring software
    - `Scaling in hooks` storing application logs
    - Lifecycle
        1. EC2 Instance gets launched by EC2 Auto scaling group
        2. WAIT state entered via Lifecycle hooks capability
        3. Whilst in WAIT state, instance runs user data script to install application
        4. Script install and application configuration
        5. Once the application is validated to be working correctly, the instance sends a complete-lifecycle action command.
- [Default termination policy](https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-termination-policies.html) designed to help ensure that your instances span Availability Zones evenly for high availability
    1. Determine which Availability Zones have the most instances, and at least one instance that is not protected from scale in. 
    2. Determine which instances to terminate so as to align the remaining instances to the allocation strategy for the on-demand or spot instance that is terminating. 
        1. Determine whether any of the instances eligible for termination use the oldest launch template or launch configuration
        2. If there are multiple unprotected instances to terminate, determine which instances are closest to the next billing hour. If there are multiple unprotected instances closest to the next billing hour, terminate one of these instances at random.
## Scaling relational databases
- Multi-AZ should be used for write and availability scaling
- Ways to scale relational databases
    - `Vertical scaling` Resizing database instance to a larger size
        - Larger instances can be good to improve performance, but balance this
    - `Storage scaling` storage can only scale up not down
    - `Read Replicas` for read-heavy workloads, read-only copies of data can help spread out the workload
        - Cannot be used for any data writing purposes
        - Not used for failover
    - `Aurora Serverless` offload scaling to AWS
        - Good for unpredictable workloads
        - Use when possible when a relational database is needed
## Scaling non-relational databases
- DynamoDB, AWS does most of the scaling for you
    - Capacity units for DynamoDB
        - `Read Capacity Unit (RCU)` reads per second for an item up to 4KB in size
            - One strongly consistent read or two eventually consistent reads per second 
            - Example: RCUs for 1 strongly consistent read per second for a 7KB object
                - 7KB/4KB = `2 RCU` (round up)
        - `Write Capacity Unit (WRU)` writes per second for an item up to 1KB in size
            - Example: RCUs for 1 write per second for a 3KB object
                - 3KB/1KB = `3 WCU` (round up)
    - Read write scaling options:
        - `Provisioned capacity` allocate read/write costs in advance
            - used for predictable workloads
        - `On-Demand Capacity` pay for actual reads/writes
            - used for sporadic workloads
            - Optimises costs
        - Can only change between modes 2 times in a 24 hour period
## Elastic Load Balancing (ELB)
- `Elastic Load Balancing (ELB)` automatically distribute incoming application traffic across multiple instances
- Improves availability within a region
- Can be done across multiple AZs
    - designed to only run in one region and not across multiple regions
    - `Cross-zone load balancing` must be enabled enabled for ELB to distribute traffic across the registered targets in all enabled AZs.
- `Health Checks` periodically send requests to load balancers registered instances to test their status
    - Unhealthy instances are marked as `OutOfService`
    - Routes requests to only health instances
- `De-registration delay/connection draining` allows load balancers to keep connections open if instances are de-registered or become unhealthy
    - Enables load balancer to complete in-flight requests made to instances that are unhealthy or de-registering
    - Disable to immediately close connections with unhealthy or de-registering instances
- `Target group` routes requests to one or more instances using the specified protocol and port number. 
    - can register a target with multiple target groups.
- [Listeners](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-listeners.html) process that checks for connection requests
    - Rules are evaluated in priority order, from the lowest value to the highest value
    - Need to configure protocol and port 
    - Need to specify port and protocol (HTTP or HTTPS)
    - `HTTP listener rule` can be used to redirect HTTP requests to HTTPS
- Types of load balancer
    - `Application Load Balancer (ALB)` intelligent load balancer
        - If an instance fails a health check , the ALB stops sending traffic to the instance.
        - best suited for load balancing of HTTP and HTTPS
        - Only support HTTP/HTTPS
            - Supports gRPC 
        - For HTTPS, need a SSL certificate deployed on load balancer
        - can use AWS PrivateLink and expose static IP addresses for applications that are built on Application Load Balancer
        - Supports Redirects
        - Can have lambda functions as a target
        - Fixed-response actions
        - Layer 7, application aware
        - `path conditions/ path-based routing` to define rules that route requests based on the URL in the request 
        - `host conditions/ host-based routing` to define rules that route requests based on the host name in the host header
        - Rules are used to determine how load balancer will route requests
            - Each rule has a priority, one or more actions, and one or more conditions
            - When rule conditions are met then actions are performed
            - Need to define a default rule for each listener
        - `Sticky sessions` allow you to bind a users session to a specific instance
        - `deregistration delay` time for Elastic Load Balancing to wait before deregistering a target. 
            - range is 0–3600 seconds. 
            - The default value is 300 seconds.
            - Increase to ensure that requests are completed during a scale in
    - `Network Load Balancer` performance load balancer
        - Can handle millions of requests per second, ultra-low latency
        - Layer 4, connection level
        - Supports TCP, TLS, UDP, TCP_UDP
        - Supports 1-65535
        - Supports static IPs
        - Can use TLS listener to offload encryption to load balancer
            - Must deploy exactly one SSL certificate
        - Can perform HTTP health checks
        - Selects a a target from target group
            - Attempts to open a TCP connection to the target on the port specified in the listener config
            - Listener forwards the request to the target group
        - No rules
    - `Gateway Load Balancer` for inline Virtual Appliance Load balancing
        - Layer 3, network level
        - Appliances must support the GENEVE protocol
        - Use when deploying inline Virtual Appliances where network traffic is not destined for the Gateway Load Balancer itself
        - manage your third-party virtual appliances
        - invisible to the source and destination
    - `Classic Load Balancer` Legacy/test/dev load balancer
        - Layer 7, application level
        - For HTTP/HTTPS
        - `X-forwarded-for` contains original IPv4 of the client
        - `Gateway timeouts` responds with 504 error if application stops responding
        - `Sticky sessions` allow you to bind a users session to a specific instance
            - Useful is storing information locally in an instance
            - If an instance is removed traffic may continue to be directed to that instance
                - Disable Sticky sessions to resolve
## CloudWatch
- `CloudWatch` monitoring and observability platform that was designed to give us insight into our AWS architecture
- Metrics are stored on a regional basis
- Up to 1 second granularity on metrics
- up to 15 months of metrics storage and retention
- Any application logs that need processed should be sent to CloudWatch logs
    - Allows easy aggregation and storage
    - When logs don't need processed should be sent to S3
    - S3 should also be used for long term log storage
- `Basic Monitoring` every 5 mins
- `Detailed Monitoring` every 1 min
    - Costs more than Basic
- `Default Metrics` CPU Utilisation, Network Throughput, DiskReadOps
- `Custom Metrics` EC2 memory utilization, EBS Storage Capacity
- Uses
    - Alerting on failed SSH attempts
    - Determine source IP addresses that are port probes
    - Ad-hoc queries
- CloudWatch features  
    - `System Metrics` metrics you get out of the box
        - more managed the service is the more metrics
    - `Application Metrics` by installing a CloudWatch agent, you can get information from EC2 instances
    - `Alarms` alert you when something goes wrong
- `CloudWatch Logs` tool that allows you to monitor, store and access log files from a variety of sources
    - Gives ability to query your logs to look for potential issues or relevant data
    - `Log Event` record of what happened, timestamp and data
    - `Log Stream` collection of log events from same source
        - From a single instance
    - `Log Group` collection of log streams
        - Can group all common instance logs together
    - Features:
        - `Filter Patterns` look for specific terms in logs
            - Example: 400 errors
        - `CloudWatch Logs Insights` allows you to query all your logs using a SQL-like solution
        - `Alarms` alert you when something goes wrong
- `CloudWatch Agent` used for to collect and monitor system and application metrics on AWS services and on-prem
    - Use for custom logs
    - `Cloudwatch Metric Streams` continuous, near real-time stream of metrics to a destination of your choice.
    - Can send metrics to Datadog, New Relic, Splunk, Dynatrace, Sumo Logic, and S3.
### CloudWatch Dashboard
- `CloudWatch Dashboard` Customizable home pages in the CloudWatch console that you can use to monitor your resources in a single view, even those spread across different regions.
- all dashboards are global, not region-specific
### CloudWatch Container Insights
- `CloudWatch Container Insights` collects, aggregates, and summarizes metrics and logs from your containerized applications and microservices.
- Integrates with ECS and EKS
### EventBridge
- `EventBridge (CloudWatch Events)` serverless event bus that allows you to pass events from a source to an endpoint
- Components
    - `Events` recorded change in application or service
    - `Rules` used to match events and send them to targets
    - `Event Bus` router that delivers events to targets
        - Every account has default bus
        - can create custom buses
            - Cross-account access
- Uses
    - Trigger an action based on something that happened in AWS
        - Trigger Lambda functions
    - Quickly respond to events happening on AWS
        - Send messages to respond to the environment, SNS
    - Capture state information
### CloudWatch Alarms
- `CloudWatch Alarms` watches a single metric over a specified time period, and performs one or more specified actions, based on the value of the metric relative to a threshold over time.
- Alarm States
    - `OK` The metric or expression is within the defined threshold.
    - `ALARM` The metric or expression is outside of the defined threshold.
    - `INSUFFICIENT_DATA` The alarm has just started, the metric is not available, or not enough data is available for the metric to determine the alarm state.
- create alarms that automatically stop, terminate, reboot, or recover your EC2 instances
- can also monitor your estimated AWS charges
    - can only track the estimated AWS charges in CloudWatch and not the actual utilization of your resources
    - only set coverage targets for your reserved EC2 instances in AWS Budgets or Cost Explorer, but not in CloudWatch.
## Managed Grafana
- `Managed Grafana` fully managed service that allows secure data visualisation for instantly querying, correlating, and visualising your operational metrics, logs, and traces from different sources
- open-source
- Grafana is a widely used data visualisation tool
- `Workspaces` logically isolated grafana servers, allow for separation of data visualisation and querying
    - Dashboards and visualisations are created for logs within workspaces
- Built-in security and compliance
- Pricing based on per active user in workspace
- Integrated with CloudWatch, Amazon Managed Prometheus, Amazon OpenSearch Service, AWS X-ray, and Amazon TimeStream
- Uses:
    - Container metric visualisations
    - IoT
    - Troubleshooting by operational teams
- Can leverage VPC endpoints for secure VPC access
## Managed Prometheus
- `Managed Prometheus` serverless, Prometheus-compatible service used for securely monitoring container metrics at scale
- Can leverage open-source Prometheus data model and PromQL query language
- open-source
- AWS manges scaling and availability
- High availability, replicated across 3 AZs in same region
- Choose Amazon EKS or self-managed Kubernetes clusters
- Data is retained for 150 days then deleted
- Can leverage VPC endpoints for secure VPC access
- Uses
    - Amazon EKS monitoring
    - self-managed Kubernetes cluster monitoring

# Module 8: Automation
- Manual builds are gamble, replace manual steps with automated ones where possible
- Saves time
- Easier to build secure environments
- Consistent environments
- `Immutable Pattern` Deployed application code can't modify existing cloud resources, which, as a result, requires the creation of new resources.
## CloudFormation
- `CloudFormation` allows you to provision resources quickly and consistently
- Manage resources through lifecycles
- No additional charge for CloudFormation
- Infrastructure as code
- Good for disaster recovery, rapidly rebuild resources
- `Template` resources defined using JSON or YAML
    - Provides visualisation of services defined in template
- If an error occurs during creation then will roll back all changes
- Need to copy AMI to another region before it can be used
    - Create a mapping in the CloudFormation template. Define the unique AMI value per region.
- Code is deployed as Stack or Stack Sets
    - `Stack` collection of resources that are managed together as a single logical unit
        - names are case sensitive
    - `Stack Set` way to manage stacks across accounts and regions
    - Stacks are regional
- `Drift detection` enables you to detect whether a stack’s actual configuration differs, or has drifted, from its expected configuration
    - A resource is considered to have drifted if any if its actual property values differ from the expected property values.
    - A stack is considered to have drifted if one or more of its resources have drifted.
- `Change sets` allow you to see how your changes might impact your running resources, especially for critical resources, before implementing them.
- Template fields
    - `AWSTemplateFormatVersion`
        - Optional
        - Example: 2010-09-09
    - `Parameters` used to dynamically create resources based on input values
        - Optional
    - `Mappings` used to lookup values based on data points
        - Optional
    - `Resources` defines resources in account and configuration
        - Required
    - `Outputs` where you specify what information and values you want to output
        - Optional
    - `Transform` specify macros/transforms that modify the template before its processed
        - Optional
        - Add custom automation to templates
- `CloudFormation registry` helps you discover and provision private and public extensions such as resources, modules, and hooks in your AWS CloudFormation templates.
- `CreationPolicy` attribute with a resource to prevent its status from reaching create complete until CloudFormation receives a specified number of success signals or the timeout period is exceeded
- CloudFormation workflow
    1. Create template
    2. Upload the template
    3. CloudFormation translates the template to API requests
    4. CloudFormation forms stack of resources
## Solutions Library 
– `Solutions Library` stores solutions that AWS and AWS Partners have built for a broad range of industry and technology use cases.
- Include the tools that you need to get started quickly, such as CloudFormation templates, scripts, and reference architectures.
- Solutions approved by AWS architects
## Cloud Development Kit
- `Cloud Development Kit (AWS CDK)` open-source software development framework to model and provision your application resources by using common programming languages. 
- no extra cost
- Uses any supported language to generate templates, Python, JavaScript, TypeScript, Java, or C#
- Supports autocomplete and inline documentation
- simplifies the creation and deployment of CloudFormation templates. 
- offers infrastructure components and groups of components that are preconfigured according to best practices. 
- can still customize your components and their settings
- Has proven defaults and reusable classes
- Provisions multiple environments
- `Stacks` a deployment of AWS resources defined in your CDK app. Each stack is a CloudFormation stack and can contain multiple AWS resources. 
- `CDK app` is a container for one or more stacks. It defines the cloud resources that will be created and how they will be connected
-  `Environments` can be used to deploy to different accounts, regions, or stages 
- `Stack drift` a feature that allows you to detect and compare the actual stack resources to the expected stack resources in your CloudFormation template.
## Elastic Beanstalk
- `Elastic Beanstalk` all in one service for deploying and scaling web applications and services
- No additional charge apart from resources used
- Provide code and some options
- Preferred solution to easily bundle and deploy applications
- Application files are stored in S3
    - server log files can also optionally be stored in S3 or in CloudWatch Logs. 
- Can handler containerised applications, Docker, Tomcat, Passenger, Puma
- Variety of supported languages
    - Java, .NET, PHP, Node.js, Python, Ruby, Go
- Platform as a Service (PaaS)
    - Apache Tomcat, Docker
- OS and application servers are updated for automatically
- Automates all deployments
- Automatically scales your application up and down
- Allows developers to focus on development
- Available as a subdomain of `elasticbeanstalk.com`
- `environment` version that is deployed on to AWS resources
    - runs only a single application version at a time, however, you can run the same version or different versions in many environments at the same time.
    - Under the hood made up of EC2 instances, Auto Scaling group, ELB
- Deployment policies:
    - `All at once` deploys the new version to all instances simultaneously and will be out of service for a short time.
    - `Rolling` deploys the new version in batches.
    - `Rolling with additional batch` deploys the new version in batches, but first launch a new batch of instances.
    - `Immutable` deploys the new version to a new set of instances.
    - `Traffic splitting` deploys the new version to a new set of instances and temporarily splits incoming client traffic.
- `Beanstalk Monitoring console` displays your environment’s status and application health at a glance.
- `Enhanced health reporting` is a feature that you can enable on your environment to allow AWS Elastic Beanstalk to gather additional information about resources in your environment
- `Saved Configuration` starting point for creating unique environment configurations.
## Systems Manager
- [Systems Manager](https://tutorialsdojo.com/aws-systems-manager/) Allows you to centralize operational data from multiple AWS services and automate tasks across your AWS resources
- available at no cost to manage your Amazon EC2 and on-premises resources
- patch, update, manage, and configure EC2 instances along with on-prem infrastructure
- Use roles to provide access to EC2 instances
- work with Organizations across all of the AWS accounts in your organization
- Health, compliance, and configuration management
- Capabilities
    - `Playbooks` predefined or custom documents to enable automatic resource management
    - `Run Command` remotely execute commands on managed compute without SSH or RDP
    - `Patch managed` patches OS and applications on managed systems
    - `Parameter Store` securely store secrets and application configuration info
    - `Maintenance windows` schedule for performing updates
    - `Session Manager` directly connect to managed instances without needing SSH
        - Logs all usage during sessions, send to CloudWatch and CloudTrail
- `SSM Agent` software component that is installed on manage instances on AWS/on-prem
    - Linux and Windows without opening ports
    - Often installed in AWS AMIs by default
    - Need to configure permissions on IAM for it to work properly
- Uses
    - Create logical groups of resources such as applications, different layers of an application stack, or development and production environments.
    - Select a resource group and view its recent API activity, resource configuration changes, related notifications, operational alerts, software inventory, and patch compliance status.
    - Take action on each resource group depending on your operational needs. 
    - Centralize operational data from multiple AWS services and automate tasks across your AWS resources.
## Lightsail
- [Lightsail](https://docs.aws.amazon.com/lightsail/) Easy way to build websites or web applications
- Supports WordPress, PrestaShop, Drupal, Ghost, Joomla, Plesk, Magento, Redmine
-  includes everything you need to launch your project quickly 
    - instances (virtual private servers)
    - container services, managed databases
    - content delivery network (CDN) distributions
    - load balancers
    - SSD-based block storage
    - static IP addresses
    - DNS management of registered domains
    - resource snapshots (backups) 
    - for a low, predictable monthly price.
- `Lightsail for Research` academics and researchers can create powerful virtual computers in the AWS Cloud
## CodeWhisperer
- `CodeWhisperer` analyses your comments and code as you write them in your integrated development environment (IDE). 
- goes beyond code completion by using natural language processing to comprehend the comments in your code. 
- By understanding English comments, CodeWhisperer generates complete functions and code blocks that align with your descriptions. 
- analyses the surrounding code, ensuring the generated code matches your style and naming conventions and seamlessly integrates into the existing context.
- assesses your code against multiple sets of standards and best practices. This includes the following: 
    - Open Worldwide Application Security Project (OWASP) standards
    - Crypto library best practices
    - AWS security standards
- `security scan` feature is continuously updated to help keep applications free from new security vulnerabilities.
- Supports Python, Java, JavaScript, TypeScript, C#, Go, Rust, PHP, Ruby, Kotlin, C, C++, Shell scripting, structured query language (SQL), and Scala.


# Module 9: Containers
## Microservices
- `Microservices` where software is composed of small independent services that communicate over well-defined APIs.
- scaled without affecting the functioning of other services
- designed for a set of capabilities and focuses on solving a specific problem
- Microservices can be either stateless or stateful
- `Stateful applications` save client session data on the server, allowing for faster processing and improved performance. 
    - Stateful applications excel in predictable workloads and offer consistent user experiences.
    - typically simple to deploy. 
    - require more resources to maintain state information
- `Stateless applications` do not save information about previous interactions, user sessions, or events.
    - typically align with the demands of dynamic workload and changing business requirements. 
    - Stateless application design can increase flexibility with horizontal scaling and dynamic deployment
    - flexibility helps applications handle sudden spikes in traffic, maintain resilience to failures, and optimize cost.
## Containers on AWS
- `Registry` repository to store containers for version control 
- `Orchestration tool/ launch type` manages the scaling, networking, and maintenance of your containers
    - Pulls container image from the registry, ECR, DockerHub
    - Deploys container to hosting resource, Fargate, EC2
- `Container hosting`
## Elastic Container Registry (ECR)
- `Elastic Container Registry (ECR)` managed container image registry
- Private repositories, permissions via IAM
- Supports OCI images/artifacts and docker images
- can compress, encrypt, and control access to your container images
- Components:
    - `Registry` private registry for each AWS account
    - `Authentication Token` required to push/pull images
    - `Repository` contains images
    - `Repository Policy` control access to repos and images
- `ECR Public` service for public image repositories
- `Lifecycle Rules` define rule for cleaning unused images
- `Image Scanning` automatically scan images for security vulnerabilities
- Can share images across regions and accounts
- `Tag Mutability` prevents image tags from being overwritten
- Integrates with on-prem, ECS, EKS, Amazon Linux
## Container Orchestration tools
### Elastic Container Service (ECS)
- `Elastic Container Service (ECS)` open-source container orchestration service that offers a more managed model for deploying your containers.
- allows you to easily launch and manage Docker containers running on AWS compute
    - Will manage and keep containers online
    - Containers are registered with Load Balancers automatically
    - Use when
        - all on AWS
        - Need simple way to manage containers
- Can host on EC2 or Fargate
- Application Load Balancer is used to route to correct container
- `ECS Anywhere` feature within Amazon ECS that allows for AWS managed container orchestration on-prem
    - No need to install and operate container software
    - Standardisation across environments
    - Deploy containers using EXTERNAL launch type
    - Requirements
        - SSM Agent
        - ECS Agent
        - Docker
- Backup container images for disaster recovery
-  `CloudWatch Container Insights` You can view the logs from your containerized applications and instances in one convenient location.
### Elastic Kubernetes Services (EKS)
- `Elastic Kubernetes Services (EKS)` managed kubernetes container orchestration service
- large-scale complex operations
- Overkill for most users needs
- manages clusters of EC2 instances and runs containers on those instances
- Can also deploy containers on Fargate
- Use when
    - Not all on AWS
    - Work to configure and integrate with AWS
    - Open source or Kubernetes already being used
    - require additional control over your configurations
- Autoscaling products:
    - `Karpenter` is a flexible, high-performance Kubernetes cluster auto scaler that helps improve application availability and cluster efficiency
        - Under a minute response
    - `Kubernetes Cluster Auto scaler` automatically adjusts the number of nodes in your cluster when pods fail or are rescheduled onto other nodes
- `aws-auth` ConfigMap is automatically created and applied to your cluster when you create a managed node group or when you create a node group using eksctl.
    - created to allow nodes to join your cluster and add role-based access control (RBAC) access to IAM principals
- `EKS Distro (EKS-D)` Kubernetes distro based on and used by EKS
    - You fully manage
    - Can run on-prem or cloud
    - built from the same source code as EKS
    - open-source
- `EKS Anywhere` on-prem way to run EKS
    - You fully manage
    - Standardisation across environments
## Container Hosting
### Fargate
- `Fargate` fully managed serverless compute engine tailored for docker containers
- It is Launch type
    - Requires use of EKS or ECS to deploy and manage containers
- Supports both Linux and Windows containers
- EFS used for persistent or shared storage
- Pay based on resources allocated and runtime
- Provides 20 GiB of free ephemeral storage
- Use when
    - No OS access required
    - Longer-running container tasks, use Lambda for short-running tasks
    - Isolated environments per container
    - Fast start times (<30s)
    - For jobs requiring less than 16 CPUs, no GPUs, <120GB
### Running Containers in EC2
- Running containers on top of an EC2 instance is common practice and uses elements of VM deployments and containerization.
- requires you to manage scaling, connectivity, and maintenance.
- can only scale to the size of the EC2 instance that is used
- scale out and scale in the number of EC2 instances that are used to host containers. 
- cost effective if managed correctly
- provides more control over the instance type.

# Module 11: Serverless
- Benefits of serverless
    - Ease of use, just write code
    - Event based, only uses resources when events happen
    - Pay as you go billing
## Lambda
- `Lambda` serverless compute service that lets you run code without provisioning or managing the underlying servers
- Pricing
    - `Free tier` 1m requests and 400TB of compute per month
    - After that pay per use
- Integrates with many AWS services
- Easy monitoring using CloudWatch
- Execution limit of 900 seconds (15 mins)
- Many languages, Python, Go, Java, Node.js
- Supports up to 10 GB memory 
- Options
    - `Runtime` environment to run code
    - `Permissions` what you Lambda function is allowed to do
    - `Networking` optionally can define the VPC, subnet and security groups
        - By default part of AWS owned VPC
    - `Resources` memory and timeout, CPU allocated automatically
    - `Trigger` what alerts Lambda function to start
- To secure Database credentials with Secrets Manager rather than environment variables
- `EC2ThrottledException` caused by your VPC not having sufficient subnet ENIs or subnet IPs
    - Specifying Multiple subnets in each of the Availability Zones, your Lambda function can run in another Availability Zone if one goes down or runs out of IP addresses.
- [Lambda function URL](https://docs.aws.amazon.com/lambda/latest/dg/lambda-urls.html) is a dedicated HTTP(S) endpoint for your Lambda function
    - Once created URL endpoint never changes
## Serverless Application Repository
- [Serverless Application Repository](https://aws.amazon.com/serverless/serverlessrepo/) allows users to find, deploy, and publish serverless applications
- Can share private or publicly
- `AWS SAM Template (manifest)` uploaded alongside code
    - Private by default
## Serverless Application Model (SAM)
- [Serverless Application Model (SAM)](https://tutorialsdojo.com/aws-serverless-application-model-sam/) open-source framework for building serverless applications.
- JSON or YAML configuration template to model your applications
-  transforms and expands the SAM syntax into AWS CloudFormation syntax. 
    - Any resource that you can declare in an AWS CloudFormation template you can also declare in an AWS SAM template.
- `SAM CLI` provides a Lambda-like execution environment that lets you locally build, test, and debug applications defined by SAM templates


# Module 12: Edge Services
- `External Caching` cache data that's going to be returned to users
- `Internal Caching` used to speed up services such as databases 
- Put a cache in front of everything you can
## CloudFront
- `CloudFront` Content Distribution Network (CDN) that allows us to spread out our resources all over the globe
- Helps speed up static content distribution
    - uses the nearest edge location to the customer or the originating request location
    - External caching
    - dynamic data, you can configure many CDNs to retrieve data from the origin servers
    - `Edges caches` frequently accessed static data
        - provide an alternative to having to retrieve that content from the origin server
    - `Regional edge caches` used when content that is not accessed frequently enough to remain in an edge location
    -  increased reliability and availability because copies of your files are now held in multiple edge locations around the world
- Helps resolve most global connection issues
- Settings
    - HTTPS by default, custom SSL cert
        - Used to put secure connections on S3 based websites
    - Global Distribution, cannot pick specific countries just general areas
        - Don't use to block country wide access, use WAF instead
    - Supports non-AWS endpoints
    - Can force expiration of stale content
- [Origin access control (OAC)](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html) permits only designated CloudFront distributions to access their S3 buckets
    - recommend
    - Supports S3 buckets in all AWS Regions, including opt-in Regions launched after December 2022
    - Supports S3 server-side encryption with AWS KMS (SSE-KMS)
    - Dynamic requests (PUT and DELETE) to Amazon S3
- `Origin access identity (OAI)` prevents users from viewing your S3 files by simply using the direct URL for the file
- `origin server` where CloudFront gets your files
    - Cloud be S3, EC2, On-prem server
- `geographic restrictions/ geo blocking` to prevent users in specific geographic locations from accessing content that you're distributing through CloudFront
- Improve performance
    - Choose your caching strategy 
        - Time to live (TTL)
        - Cache key settings
    - Improve your cache hit ratio
    - Use CloudFront Origin Shield
- Optional features
    - Can associate an edge function
    - Associate WAF web access control list (web ACL)
    - Add custom domain name
### CloudFront Origin Shield
- [CloudFront Origin Shield](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/origin-shield.html) centralized caching layer that sits in front of your origin 
- Improve your cache hit ratio, reduce the load on your origin, and help improve performance.
- improve its availability
- reduce its operating costs.
### Edge Functions
- [Edge Functions](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/edge-functions.html) code that you write and attach to your CloudFront distribution
- customize how your CloudFront distributions process HTTP requests and responses.
- `CloudFront Functions` write lightweight functions in JavaScript for high-scale, latency-sensitive CDN customizations. 
    - sub-millisecond startup times
    - scales immediately to handle millions of requests per second
    - highly secure. 
    - native feature of CloudFront, which means you can build, test, and deploy your code entirely within CloudFront.
- [Lambda@Edge](https://docs.aws.amazon.com/lambda/latest/dg/lambda-edge.html) extension of AWS Lambda that lets you deploy Python and Node.js functions at Amazon CloudFront edge locations.
    - Lambda function must be in the US East (N. Virginia) Region.
    - Significantly reduces latency and improves the user experience.
    - an have CloudFront invoke your Lambda function when the following events occur:
        - `viewer request` When CloudFront receives a request from a viewer 
        - `origin request` Before CloudFront forwards a request to the origin
        - `origin response` When CloudFront receives a response from the origin
        - `viewer response` Before CloudFront returns the response to the viewer
            - cannot modify the HTTP status code of the response, regardless of whether the response came from the origin or the CloudFront cache.
    - Uses:
        - customize the content that your CloudFront distribution delivers to your end users
        - used in origin groups for use in [origin failover situations](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/high_availability_origin_failover.html)
## Global Accelerator
- `Global Accelerator` networking service that sends your users traffic through AWS global network infrastructure via accelerators
- helps speed up external connections
- Global Service
- IP caching, meant for TCP and UDP traffic
    - different layer to CloudFront
- `Anycast IP Addresses` fixed entry for all traffic
    - Provides 2 Anycast IP Addresses by default
    - `Dual Stack` provides 4 Anycast IP addresses
- `Accelerator` directs user traffic to the optimal AWS endpoints
    - improve availability and performance for internet applications
    - `Standard` traffic is routed based on user location, health checks and weights
    - `Custom` traffic routed to specified instances and ports in a VPC
- `Listeners` process inbound connections based on ports and protocols
- `Endpoints` resources that Global Accelerator directs traffic to
- provides two global static public IPs that act as a fixed entry point to your application endpoints, such as Application Load Balancers, Network Load Balancers, Amazon Elastic Compute Cloud (EC2) instances, and elastic IPs.
- helps single region applications by bridging the gap between local and global traffic.
- multiple regions, you can accumulate a long list of user facing IP addresses and ever increasing traffic routing logic.


# Module 13: Backup and Recovery
- `Recovery Point Objective (RPO)` what point in time do you want data recovered to
    - How much can you afford to lose in time
    - Lower the time, greater the cost
- `Recovery Time Objective (RTO)` how fast do you want to failover
    - How much time can the business afford to be down for
    - Lower the time, greater the cost
## Backup Recovery types
- `Backup and restore` restore system from a backup  
    - Cheap but slow
    - High RPO and RTO in hours
    - S3 is ideal for backups
    - Use cloudformation to recreate resources
    - Low priority services
- `Pilot Light` live data replication to a database in another Region
    - Low RPO, RTO in minutes-hours
    - Redundant database, no web servers, no other services
        - Other services may be switched off ready to start
    - redirect traffic to this database in a failover
    - Still some downtime
    - Use Route 53 to route to recovery setup
    - Use for core services
- `Warm standby` scaled-down version of production system in another Region
    - Low RPO, RTO in seconds to minutes
    - Scaled-down database, web servers, other services
    - Scale up in failover region
    - More expensive but quicker recovery
    - Use Route 53 to route to recovery setup
    - Business critical services
- `Active/Active failover/ Multi-site` two active sites both active and traffic split between them
    - Low RPO, RTO immediately to seconds
        - Real-time recovery
    - If one site fails the other takes the load
    - Most expensive but no downtime
    - Have to have both sites at 200% normal capacity for no downtime
## Elastic Disaster Recovery (DRS)
- [Elastic Disaster Recovery (DRS)](https://docs.aws.amazon.com/drs/latest/userguide/what-is-drs.html) provides continuous block-level replication, recovery orchestration, and automated server conversion capabilities
- fast, reliable recovery of on-premises and cloud-based applications using affordable storage, minimal compute
- point-in-time recovery.
- minimizes downtime and data loss
- RPO of seconds, RTO 5–20 minutes
- In the event of a disaster, assists in performing a failover to AWS for immediate recovery. 
- `Elastic Disaster Recovery Failback Client` is installed on the target server, and specific credentials are generated. 
- Cross-Region or cross-AZ failover and failback can be executed directly from the AWS DRS Console.

# Security
## DDoS
- `Layer 4` attack at TCP/ transport layer, 
    - SYN Floods/ NTP Amplification attacks
- `Layer 7` GET/POST request floods
    - Usually from a botnet 
## CloudTrail
- `CloudTrail` records AWS management console and API calls
- Can identify which users and accounts called AWS
- Request, response, source IP, caller identity, metadata, time
- Stores logs in S3
- enabled log file integrity validation within the CloudTrail console for your trails to prevent tampering
- By default, encrypted by Amazon with SSE-S3
    - can instead use SSE-KMS instead for more management
- Uses
    - Intrusion detection
    - Incident investigation
    - Compliance
- [CloudTrail Lake](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-lake.html) lets you run SQL-based queries on your events. 
    - converts existing events in row-based JSON format to Apache ORC format
## Shield
- `Shield` free DDoS protection for Elastic Load Balancers, CloudFront, and Route53
    - Protections against Layer 3/4 attacks
    - detects malicious traffic and it provides real-time issue mitigation
    - Free and on by default for all customers
- `Shield Advanced` enhanced protection for Elastic Load Balancers, CloudFront, and Route53 against larger and more sophisticated DDoS
    - Provides real-time notifications of DDoS attacks
    - Protects against bill spikes
    - Dedicated DDoS response team
    - additional detection and mitigation against large and sophisticated DDoS attacks
    - near real-time visibility
    - integration with WAF
    - Protections against Layer 3-7 attacks
## Web Application Firewall (WAF)
- `Web Application Firewall (WAF)` lets you monitor the HTTP and HTTPS requests that are forwarded to CloudFront or an Application Load Balancer
- Lets you control access to content
- Protects against Layer 7 attacks
- Protects against XSS and SQLi
- can also monitor HTTP(S) requests that are forwarded to your compatible AWS services.
- Supported services
    - CloudFront
    - Application Load Balancer
    - API Gateway
    - AppSync
    - Cognito user pools
- Characteristics WAF can look for
    - IP addresses
    - Request country
    - Request header values
    - Script/SQL Code
    - Strings in request
- Use WAF to block requests from a specific country
- `Web ACLs` protect a set of AWS resources. You create a web ACL and define its protection strategy by adding rules.
    - `Rules` define criteria for inspecting web requests and specify how to handle requests that match the criteria.
    - `Rule groups`  can define own or Managed Rules for AWF and AWS Marketplace sellers provide managed rule groups for your use. 
    - `Rule statements` This is the part of a rule that tells AWS WAF how to inspect a web request. When AWS WAF finds the inspection criteria in a web request, we say that the web request matches the statement.
    - `IP set` collection of IP addresses and IP address ranges that you want to use together in a rule statement. IP sets are AWS resources.
    - `Regex pattern set` collection of regular expressions that you want to use together in a rule statement. Regex pattern sets are AWS resources.
- `Monitoring and logging` monitor web requests, web ACLs, and rules using CloudWatch. 
    - You can also activate logging to get detailed information about traffic that is analyzed by your web ACL. 
    - send your logs to CloudWatch Logs, S3, Kinesis Data Firehose.
## Firewall Manager
- `Firewall Manager` security management service that allows you to centrally manage firewall rules across accounts and applications.
- set up baseline security.
    - Automatically discover new accounts and remediate non-compliant events
- Consistently enforce the protections.
    - Simplify rule management across applications and accounts
- Deploy AWS WAF rules from AWS Marketplace.
- Activate rapid response to attacks across all accounts
- Requires
    - activate AWS Organizations with full features
    - use AWS Config
    - assigned user as the Firewall Manager administrator
## DDoS-resilient reference architecture 
- User Request -> Route 53 -> CloudFront -> WAF -> CloudFront -> ELB -> EC2
- With Global Accelerator
    - Global Accelerator itself doesn't support AWS WAF
    - User -> Global Accelerator -> Application Load Balancer with AWS WAF -> EC2 instance
## GuardDuty
- `GuardDuty` threat detection service that uses ML to monitor for malicious behaviour
- Alerts appear in console and CloudWatch events
- Can receive feeds from 3 parties, CrowdStrike, AWS Security about malicious domains
- Monitors logs
- Centralise threat detection across accounts
- Takes 7-14 days to set up baseline
## Macie
- `Macie` used to discover sensitive data in S3
- uses machine learning and pattern matching 
- Alerts you about unencrypted or public buckets
- `Macie alerts` can be sent to EventBridge
- Step functions can be used to automated remediation actions
## Inspector
- `Inspector` automated security assessment service
- Helps improve security and compliance of applications deployed on AWS
- Inspects network and EC2 instances
- Types of assessment
    - `Network assessment` checks for ports reachable outside VPC
        - Inspector agent not required
    - `Host Assessment` vulnerable software, host hardening, and security best practice
        - Inspector agent required
## Key Management Service (KMS) and CloudHSM
- `Key Management Service (KMS)` managed service that allows you to create and control encryption keys
    - Integrates with EBS, S3, and RDS
    - Use to encrypt EC2 operating system
    - Automatic key rotation, once a year by default
    - `Customer Master Key (CMK)` logical representation of the master key
    - `Hardware Security Module (HSM)` physical computing device that safeguards and manages keys
    - cannot store credentials in KMS
- `CloudHSM` cloud-based Hardware Security Module
    - Full control of keys, groups and users
    - Physical device entirely dedicated to you
    - No automatic key rotation
## Secrets Manager
- `Secrets Manager` securely stores, encrypts and rotates secrets
- Can be called via API, not hard coded
- Disable rotation if you credentials are hard coded    
- Uses
    - RDS credentials
    - Any type of secret
## Parameter Store
- `Parameter Store` capability of Systems Manager that provides secure, hierarchical storage for configuration data management
- Free alternative to Secrets manager
- Can store up to 10,000 params
- No key rotation
- Hierarchical storage
    - Example: /dev/bdpass
- `Parameter Polices` used to define expiration dates
- Parameter Types
    - `String` block of plaintext
    - `StringList` comma separated list of values
    - `SecureString` sensitive data
## Presigned-URLs and cookies
- Objects in S3 are private by default
- Can be in S3 or CloudFront
- `Presigned-URLs` can be used to share an S3 object with others
    - Must provide security credentials, bucket name, object key, HTTP method, expiration date
    - Only valid for specified duration
- `Presigned Cookies` can be used to share S3 objects with others
## Certificate Manager
- `Certificate Manager (ACM)` allows you to create, manage, and deploy public and private SSL certificates
- Free 
- Automated renewals and deployments
- using events and metrics that are published into EventBridge to alert for expiring certificates
    - Create an EventBridge (CloudWatch Events) rule that will check AWS Health or ACM expiration events related to ACM certificates. Send an alert notification to an Amazon Simple Notification Service (Amazon SNS) topic when a certificate is going to expire in 30 days
## Audit Manager
- `Audit Manager` allows you to automatically audit AWS usage
- Produces reports specific to auditors, GDPR, HIPAA
## Artifact
- `Artifact` single source to get compliance related information
- AWS security and compliance reports or online agreements
## Cognito
- `Cognito` authentication, authorisation and user management service for web and mobile apps
- Users can sign in directly with username and password they create or through a third-party
- Uses
    - Sign-in and registration for apps
    - Access for guest users
    - Identity broker for third parties sign-in
    - Sync user data across devices
- Commonly used for mobile apps to get access to AppSync resources
- `Cognito User Pools` directories of users that provide registration or sign-in options for users
    - Authentication
    - Can add MFA to a user pool
    - can enable your app users to sign in through a social identity provider (IdP) such as Facebook, Google, Amazon, and Apple
    - Uses
        - Design sign-up and sign-in webpages for your app.
        - Access and manage user data.
        - Track your user device, location, and IP address, and adapt to sign-in requests of different risk levels.
        - Use a custom authentication flow for your app.
- `Cognito Identity Pools/ Federated Identities` grant temporary credentials that grant users access to specific AWS resources, whether the users are anonymous or are signed in.
    - authorization
    - create unique identities for users, and give them access to other AWS services.
    - Give your users access to AWS resources, such as an Amazon Simple Storage Service (Amazon S3) bucket or an Amazon DynamoDB table.
    - Generate temporary AWS credentials for unauthenticated users
- `Cognito Sync` is an AWS service and client library that makes it possible to sync application-related user data across devices
- Can use User and Identity pools together or separately
## Detective
- `Detective` analyse, investigate and identify root causes of potential issues or suspicious activities
- Pulls data from AWS resources and uses ML to build linked set of data
- Uses
    - Triage security findings
    - Threat hunting
## Network Firewall
- `Network Firewall` managed service that allows you to deploy physical firewall protection across VPCs
- Uses
    - Filter internet/outbound traffic
    - Inspect VPC-to-VPC traffic
- Works with Firewall Manager
## Security Hub
- `Security Hub` single place to view security alerts from AWS security services
- Integrated with GuardDuty, Inspector, Macie, Firewall Manager
- Uses
    - Cloud Security Posture Management (CSPM)
    - Correlate security findings


# Application Services
- `Tight Coupling` one instance talking directly to another instance
- `Loose Coupling` instances are directly aware of other instances as all communication is done through an intermediary (load balancer, SQS etc.)
## Simple Queue Service (SQS)
- `Simple Queue Service (SQS)` fully managed message queueing service that enables you to decouple and scale microservices, distributed systems, and serverless applications.
- Uses
    - handle billions of messages in a day
    - Loose coupling
    - Failure tolerance
    - Request offloading, move slow operations off of interactive request paths by enqueueing the request. 
    - Absorbs spikes
    - Auto scaling, used to determine load, scale on queue size
- can securely share SQS queues anonymously or with specific AWS account
    - can restrict queue sharing by IP address and time of day
- `Poll-based messaging` sent and received when the consumer polls
- Provides at least once delivery
- Queues are bi-directional, need a second queue to send back
- Choose Kinesis instead when their cannot be a delay
- Allows asynchronous processing of work
    - One resource writes to SQS and then another retrieves from SQS
- SQS settings
    - `Delivery Delay` default 0, can be set up to 15 minutes
    - `Message Size` can be up to 256KB of text in any format
    - `Encryption` messages are encrypted in transit, but you can add at-rest
    - `Message Retention` default 4 days, can be set between 1 minute and 14 days
    - `Long vs short polling` short polling is the default but long polling is better
        - Short polling = connect, check, disconnect, high CPU cycles
            - Increases the number of responses and therefore costs
        - Long Polling = connect, check, wait, check, wait.... disconnect, low CPU cycles
            - less frequent responses but decreases cost
    - `Queue Depth` trigger for autoscaling
    - `Visibility Timeout` lock after instance polls and downloads message, default 30 seconds
        - Ensures proper handling of message
            - If instance fails message will become visible again after timeout
        - Message is removed when instance has processed message fully
- `Streaming Single Instruction Multiple Data (SIMD) Extensions (SSE)` protects the contents of messages in SQS queues using keys managed in AWS KMS. 
    - encrypts messages as soon as Amazon SQS receives them.
    - messages are stored in encrypted form, and Amazon SQS decrypts messages only when they are sent to an authorized consumer.
### SQS Dead-Letter queues
- `SQS Dead-Letter queues (DLQ)` targets for messages that cannot be processed successfully
- One to one
- Polling based
- Special type of SQS queue, created the same way
- Almost unlimited transactions per second
- Can be set up to receive from all queues in a region or specific queues only
- Works with both SQS and SNS
    - Can be used with FIFO queues too but DLQ must also be FIFO
- Uses
    - debugging
        - Can isolate messages to troubleshoot
        - Help identify which log files to investigate for exceptions
        - Analyse SQS for errors
        - Troubleshoot permission errors
    - Configure CloudWatch alarms based on message availability counts
- Uses
- `Redrive capability` allows you to move the message back to the source queue
### SQS FIFO
- `First-In-First-Out (FIFO)` guarantees that the first message in will be the first message out of the queue
- Should only be used when FIFO is required, use standard SQS otherwise
- Costs more than standard SQS
- No message duplication
- 300 transactions per second, 3,000 using batching
    - 9,000 using FIFO High Throughput, 90,000 using batching APIs
## Simple Notification Service (SNS)
- `Simple Notification Service (SNS)` fully managed message service for both applications-to-application (A2A) and application-to-person (A2P) communication
- `Push-based messaging/ publish-subscribe` sent and immediately received by the consumer
- One to many
- Proactive notifications
- Uses
    - deliver messages to subscribers
    - Alert a system or a person, CloudWatch alarms
    - Push notifications
    - publish to multiple SQS queues
- SNS Settings and quotas
    - Subscriber types:
        - Kinesis data firehose
        - SQS
        - Lambda
        - email/ email-JSON
        - HTTP/HTTPS
        - SMS
        - Mobile Push Notifications
        - Platform application endpoint
    - `Message Size` up to 256KB of text in any format
        - `Large Message Payloads` allows for messages up to 2GB in size
            - Payload stored in S3 then linked in message
    - `DLQ Support` messages that fail to be delivered can be stored in an SQS DLQ
    - `FIFO or Standard` FIFO only supports SQS FIFO queues as subscriber
    - `Encryption` messages are encrypted in transit, but you can add at-rest
    - `Access Policy` resource policy can be added to a topic for cross-account access control
    - `Retry Policy` supported for HTTP/HTTPS endpoints
- `SNS Fanout` messages published to SNS topic are replicated to multiple subscribers/SQS queues
    - Decoupled asynchronous message processing
- by default messages are sent to all subscribers
- [`Message Filtering/ filter policies`](https://docs.aws.amazon.com/sns/latest/dg/sns-message-filtering.html) use JSON to define which messages get sent to which subscribers
- `access control mechanisms` to protect topics and messages from unauthorized access. 
    - Topic owners can set policies for a topic that restrict who can publish or subscribe to a topic
- `encrypted topics`uses AWS Key Management Service (AWS KMS) keys to encrypt your messages.
- No way to recall messages
- `SNS Delivery Policy` to control the retry pattern: linear, geometric, exponential backoff, maximum and minimum retry delays, and other patterns.
- all messages are stored redundantly across multiple AZs
## API Gateway
- `API Gateway` fully managed service that makes it easy for developers to create, publish, maintain, monitor, and secure APIs at any scale.
- Automatically scales, use throttling to protect services behind
    - Supports 100,000+ concurrent requests
- RESTful APIs
- You pay only for the API calls you receive and the amount of data transferred out. 
- Security benefits
    - Minimise attack surface, hides endpoints
    - can attach a Web Application Firewall (WAF)
    - Stop Abuse, DDoS protection, throttling limits
    - Use Signature Version 4 (SigV4) to authorize access to APIs. 
    - Authentication, via IAM, Amazon Cognito or custom Lambda functions
- Easy to build APIs
- Use to monetize API usage by third-party developers
- API Options
    - `REST API` API Keys, per-client throttles, validation of requests, WAF
        - RESTful API
    - `HTTP API` simpler, cheaper, minimal options
        - RESTful API
    - `Web Socket API` integrates with Lambda, HTTP endpoints and other AWS services
- Endpoint Types
    - `Edge-optimised` default option, requests are sent through a CloudFront edge location
        - Best for global users
        - Requires ACM cert in `us-east-1` region
    - `Regional` API on regional basis, can leverage CloudFront if required 
        - Requires ACM cert in region
    - `Private` only accessible via VPC
- [Canary release](https://docs.aws.amazon.com/apigateway/latest/developerguide/canary-release.html) is a software development strategy in which a new version of an API is deployed for testing purposes, and the base version remains deployed as a production release for normal operations on the same stage.
## Amazon MQ
- `Amazon MQ` message broker service that allows for easier migration of existing applications to the AWS cloud
- Good for migrations but for new applications should consider SNS/SQS instead
- Can use different programming languages, OSs and messaging protocols
    - Supports Apache Active MQ and RabbitMQ engines
    - Supports JMS, AMQP 0-9-1, AMQP 1.0, MQTT, OpenWire, and Stomp messaging protocols
- Requires private networking, VPC, Direct Connect or VPN
## Step Functions
- `Step Functions` serverless orchestration service to combine AWS services for business applications
- Many AWS services are integrated with Step Functions
- Graphical console for easier application workflows view and flows
- Provides simple error catching and logging if a step fails
- `Amazon State Language Format` language which all states are written in
- Components
    - `State Machine` workflow with different event-driven steps
    - `States` elements within state machines
        - `Pass` passes any input directly to its output, no work done
        - `Tasks` state within a workflow, representing a single unit of work
        - `Choice` adds branching logic
        - `Wait` creates a specified time delay
        - `Succeed` stops execution successfully
        - `Fail` stops execution and marks them as failed
        - `Parallel` runs parallel branches of executions within state machines
        - `Map` runs a set of steps based on elements in an input array
- Workflow types
    - `Standard` exactly once execution
        - Can run for up to 1 year
        - Good for long running workflows
        - Up to 2,000 executions per second
        - Pricing based on state transitions
    - `Express` at-least-once execution
        - Can run for up to 5 minutes
        - Good for high-event-rate workloads
            - IoT
        - Pricing based on executions, durations and memory consumed 
- Works with many services
    - Lambda
## AppFlow
- `AppFlow` fully managed service for exchanging data between SaaS apps and AWS services
- Pulls data records from SaaS apps and stores them in S3
- Bi-Directional for some SaaS services
- Components
    - `Flow` transfers data between sources and destinations
    - `Data Mapping` how source data is stored within destinations
    - `Filters` controls which records are transferred
    - `Trigger` how the flow is started
- Uses
    - Transfer Salesforce records to Amazon Redshift
    - Ingest Slack conversations in S3
    - Aggregate data up to 100GB per flow to S3
## Simple Workflow Service (SWF)
- [Simple Workflow Service (SWF)](https://docs.aws.amazon.com/amazonswf/latest/developerguide/swf-welcome.html) provides a way to build, run, and scale background jobs that have parallel or sequential steps.
- can coordinate work across distributed components, tracking the state of tasks
    - coordination of tasks involves managing execution dependencies, scheduling, and concurrency in accordance with the logical flow of the application.
- `task` represents a logical unit of work that is performed by a component of your application
- `workers` programs that interact with SWF to get tasks, process them, and return their results.
    - can run in cloud or on-prem
- Use step functions for new applications
    - more productive and agile approach to coordinating application components using visual workflows
- Use if you require `external signals (deciders)` to intervene in your processes, or you would like to launch child processes that return a result to a parent
- supported by the AWS SDKs for Java, .NET, Node.js, PHP, Python and Ruby
## Simple Email Service (SES)
- [Simple Email Service (SES)](https://docs.aws.amazon.com/ses/latest/dg/Welcome.html) is an email platform that provides an easy, cost-effective way for you to send and receive email using your own email addresses and domains.
- regional service
- for applications that need to send communications via email

# Developer Tools
## X-Ray 
- `X-Ray` collects application data for viewing, filtering and gaining insights
- Uses
    - Application insights
    - response times of downstream resources
    - HTTP response analysis
- View calls to other AWS resources
- Components
    - `Segments` data containing resource names, request details, and other information
    - `Subsegments` segments providing more granular timing information and details
    - `Service graph` graphical representation of service interaction
    - `Traces` trace ID tracks of requests and traces collect all segments in a request
    - `Tracing Header` extra HTTP header (`X-Amzn-Trace-Id`) containing sampling decisions and trace ID
- `X-Ray Daemon` application that listens, collects and sends to X-Ray
    - on UDP port 2000
    - Install on EC2, ECS, Lambda, Elastic Beanstalk, API Gateway, SNS, SQS


# Big Data
## Redshift
- `Redshift` fully managed, petabyte-scale data warehouse service in the cloud
- Very large relational database
- Not meant to be replacement for RDS in traditional applications
- Can store up to 16PB data
- Based on PostgreSQL
- 10x performance of other cloud data warehouses
    - result caching to deliver sub-second response times for repeat queries.
    - massively parallel processing data warehouse architecture to parallelize and distribute SQL operations
    - columnar storage, data compression, and zone maps to reduce the amount of I/O needed to perform queries.
- sub-second response times, don't use for real-time
- not used in Online Transaction Processing
- Storage of data is stored in column-based, allows for efficient parallel queries
- supports client connections with many types of applications, including business intelligence (BI), reporting, data, and analytics tools.
    - can run analytic queries against petabytes of data stored locally in Redshift, and directly against exabytes of data stored in S3.
- must specifically design, build, and load your tables to use massively parallel processing, columnar data storage, and columnar data compression
- Supports multi-AZ deployments, currently 2 AZs
    - Cannot convert from single-AZ to multi-AZ
- `Snapshots` can be taken of databases
    - Automated or manual
    - Contained in S3, cannot manage the bucket
- `Redshift Spectrum` efficiently query and retrieve data from S3 without having to load the data into Redshift tables
- `RedShift Streaming Ingestion` Allows you to consume and process data directly from a streaming source to a Redshift cluster using SQL.
- `Redshift ML` Allows you to train and deploy machine learning models using the data stored in your Amazon Redshift cluster through a simple CREATE MODEL SQL statement.
- `Redshift Data Sharing` Redshift Data Sharing is a secure way to share live data across Redshift clusters within an AWS account, without the need to copy or move data.
- `Redshift Cross-Database Queries` provide the ability to query across databases in a Redshift cluster, regardless of which database you are connected to.
- `Redshift Cluster Snapshots` Point-in-time backups of a cluster stored in S3 using SSL.
- `database audit logging` feature to track information about authentication attempts, connections, disconnections, changes to database user definitions, and queries run in the database. The logs are stored in S3 buckets.
- `Enhanced VPC Routing` all COPY and UNLOAD traffic is forced through your VPC
    - enhances security and controls
    - Can use VPC features
### Redshift Serverless
- `Redshift Serverless` lets you access and analyze data without the usual configurations of a provisioned data warehouse
## Elastic MapReduce (EMR)
- `Elastic MapReduce (EMR)` simplifies running big data frameworks to help with Extract, Transform, Load (ETL) processing
- Use tools such as Spark, Hive, HBase, Flink, Hudi, Presto
- enables you to quickly and easily provision as much capacity as you need, and automatically or manually add and remove capacity.
- EMR Storage types
    - `Hadoop Distributed File System (HDFS)` distributed scalable file system
    - `EMR File System (EMRFS)` directly access data stored in S3 as if it were a part of HDFS
    - `Local File System` locally connected disk created with each EC2 instance
        - Not persistent
- `Clusters` groups of EC2 instances within EMR
    - Cluster types
        - On-demand
        - Reserved
        - Spot
- `Nodes` each instance is a node
    - `Primary Node` manages the cluster, distributes tasks, tracks health
    - `Core Node` runs tasks and stores data in HDFS, long running
    - `Task Node` only runs tasks, typically spot instances
- `EMR Notebooks` provide a managed environment, based on Jupyter Notebooks, to help users prepare and visualize data, collaborate with peers, build applications, and perform interactive analysis using EMR clusters.
- analyze the data and access it using Business Intelligence (BI) tools and SQL queries
## Kinesis
- `Kinesis` allows you to ingest, process, and analyse real-time streaming data
- Choose this over SQS when their cannot be a delay
- Supports SQL, Python and Scala
- Kinesis forms:
    - `Data Streams` real-time streaming for ingesting data
        - Used for READING data
        - massively scalable, highly durable
        - Real-time, milliseconds
        - Ordered records
        - `Producers` put data records in
            - You manage creating consumer and scaling the stream
        - `Consumers` read the streaming data that the producers generate
            - Can send to S3, OpenSearch, Redshift, and custom HTTP endpoints
        - `Shard` base throughput unit of a Kinesis data stream.
            - stores records from 24 hours by default, up to 365 days
        - `Kinesis Agent` application that offers an easy way to collect and send data to your Kinesis data stream.
    - `Data Firehose` managed service to load streaming data into data stores and analytics tools
        - Used for LOADING data
        - `Producers` put data records in
        - `Consumers` data store
            - Transfer data to S3, Redshift, Elasticsearch, Splunk, generic HTTP endpoints, Datadog, New Relic, OpenSearch
        - Difference to data steams 
            - automatically scales to match the throughput of your data
            - Near real time, 60 seconds
            - Serverless data transformations with Lambda
            - No data storage
        - Transformations
            - can also batch, compress, and encrypt the data before loading it
            - can convert the format of incoming data from JSON to Parquet or ORC
            - provides pre-built Lambda blueprints for converting common data sources
            - can concatenate multiple incoming records based on the buffering configuration 
- `Amazon Managed Service for Apache Flink/ Kinesis Data Analytics` transform and analyze streaming data in real time
    - allows data analysis using SQL
    - Fully managed by AWS
    - Pay for amount of resources you consume as data passes through
    - Supported by Data Firehose and Data Streams
    - Allows you to query Kinesis data streams and perform interactive data analytics
        - does not stream the data by itself
### Kinesis Scaling
- `Resharding` increase or decrease the number of shards in a stream in order to adapt to changes in the rate of data flowing through the stream. 
    -  typically performed by an administrative application that monitors shard data-handling metrics
- `record processor` one record processor for every shard 
    - Record processors run in parallel within the same process
- `Auto Scaling` to automatically scale your instances based on appropriate metrics
- [UpdateShardCount](https://docs.aws.amazon.com/kinesis/latest/APIReference/API_UpdateShardCount.html) Updates the shard count of the specified stream to the specified number of shards
## Amazon Athena and AWS Glue
- `Athena` interactive query service that makes it easy to analyze data in S3 using SQL
    - Directly query S3 bucket without loading it into a database
    - Fully managed
    - Serverless
    - Can work by itself
    - columnar formats you can improve performance and reduce your costs.
- `Glue` serverless data integration service that makes it easy to discover, prepare and combine data.
    - Can perform Extract, Transform, Load (ETL)
    - Fully managed
    - Serverless
    - Used to design a schema
    - Example: convert .csv to Apache Parquet format
    - [Job Bookmark](https://docs.aws.amazon.com/glue/latest/dg/monitor-continuations.html) persisted state information, used to track data that has already been processed during a previous run 
- `Serverless SQL` achieved by combining Athena and Glue
## Lake Formation
- `Lake Formation` managed service that makes it easy to set up, secure, and manage your data lakes
- helps you discover your data sources and then catalog, cleanse, and transform the data
- Manages user permissions
- Ingests data into S3
- [Lake Formation tag-based access control (LF-TBAC)](https://docs.aws.amazon.com/lake-formation/latest/dg/granting-catalog-perms-TBAC.html) Formation tag-based access control to grant Lake Formation permissions on Data Catalog databases, tables, views, and columns
- `workflow` encapsulates a complex multi-job extract, transform, and load (ETL) activity. 
    - generate AWS Glue crawlers, jobs, and triggers to orchestrate the loading and update of data. 
- create a workflow from a blueprint
- `blueprints types`
    - `Database snapshot` Loads or reloads data from all tables into the data lake from a JDBC source. You can exclude some data from the source based on an exclude pattern.
    - `Incremental database` Loads only new data into the data lake from a JDBC source, based on previously set bookmarks. 
    - `Log file` bulk loads data from log file sources, including AWS CloudTrail, Elastic Load Balancing logs, and Application Load Balancer logs.
## Quicksight
- `Quicksight` fully managed business intelligence (BI) data visualisation service
- Can create dashboards and share them with other users
    - Can group users
- Integrates with RDS Amazon Aurora, Athena, S3
    - Commonly integrated with Athena
- `SPICE` robust in-memory engine used to perform calculations
- `Column-Level Security` available for additional cost
- Pricing is on a per-session and per-user basis
## Data Exchange
- `Data Exchange` service that helps AWS easily share and manage data entitlements from other organizations at scale.
- data receivers  can track and manage all of your data grants and AWS Marketplace data subscriptions in one place. 
- data senders can create and send data grants to data receivers.
## Data Pipeline
- [Data Pipeline](https://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/what-is-datapipeline.html) managed Extract, Transform, Load (ETL) service for automating movement and transforming data
- tasks can be dependent on the successful completion of previous tasks
- Uses
    - archive your web server's logs to S3 each day and then run a weekly EMR cluster over those logs to generate traffic report
        - ensures that Amazon EMR waits for the final day's data to be uploaded
- Components:
    - `Pipeline Definition` specifies business logic
    - `Managed Compute` service will create EC2 instances to perform your activities
    - `Task Runners` poll for different tasks and perform them when found
    - `Data Nodes` define location and types of input/output data
- Uses
    - Processing data in EMR using Hadoop streaming
    - Importing or exporting DynamoDB data
    - Copying CSV files or data between S3 buckets
    - Exporting RDS data to S3
    - Copying data to Redshift
## Amazon MSK
- `Amazon Managed Streaming for Apache Kafka (Amazon MSK)` fully managed service for running data streaming applications that use Apache Kafka
- Can support existing Kafka applications
- Handles all control-plane operations so you can focus on data plane
- Automatic recovery
- Components:
    - `Broker Nodes` specifies amount of nodes per AZ at time of creation
    - `ZooKeeper Nodes` created for you
    - `Producers, Consumers, Topics` Kafka data plane operations
    - `Flexible Cluster Operations` performs cluster operations
- `MSK Serverless` cluster type that offers serverless cluster management
- Security:
    - Integrates with Amazon KMS for SSE 
    - Encryption at rest and in-transit by default
    - API calls are logged to CloudTrail
- Logging integrates with CloudWatch, S3 and Kinesis Data Firehose
## OpenSearch Service
- `OpenSearch` managed service that allows you to run search and analytics engines
- Successor to Amazon Elasticsearch Service
- Commonly part of an Extract, Transform, Load (ETL) process
- Easily scalable
- IAM used for security control
- Multi-AZ capable
- Use for searching or analysing logs   
- SQL support for business intelligence apps
- Integrates with CloudWatch, CloudTrail, S3 and Kinesis
## ParallelCluster 
- [ParallelCluster](https://tutorialsdojo.com/aws-parallelcluster/) open source cluster management tool for deploying and managing High Performance Computing (HPC) clusters
- uses a simple text file to model and provision all the resources needed for your HPC applications in an automated and secure manner.
## CloudSearch 
- [CloudSearch](https://tutorialsdojo.com/amazon-cloudsearch/) managed service in the AWS Cloud that makes it easy to set up, manage, and scale a search solution for your website or application.
- index and search both structured data and plain text.
- Highlighting
- Autocomplete Suggestions
- You can get search results in JSON or XML, sort and filter results based on field values, and sort results alphabetically, numerically, or according to custom expressions.
- Scales to accommodate the amount of data uploaded to the domain and the volume and complexity of search requests.
- Integrates with API Gateway.

# Governance
## Organisations
- `Organisations` free governance tool that allows you to create and managed multiple AWS accounts
- Account Types
    - `Management Account/ Payer Account` primary account that hosts and manages the organisation
        - One per organisation
    - `Member accounts` all other accounts that belong to the organisation
        - linked to management account
        - Separate accounts based on environment and teams
- `Consolidated Billing` rolls all bills up to the payer account, single payment method
    - `Usage Discounts` aggregate usage discounts
    - `Shared Savings` easily share reserved instances and savings plans across the org
- `Multi-account strategy` manage multiple accounts from a central location
- `Tag Enforcement` require specific tags for all AWS services
- `Organisational Unit (OU)` logical grouping of accounts to allow for easy management and separation
    - Can be OUs under OUs
    - AWS accounts fall under OUs
- `Service Control Policies (SCPs)` JSON policies that get applied to OUs or accounts to restrict actions that are allowed or denied
    - Only works when organisations is enabled
    - Permission boundary
    - Similar format to IAM policies
    - Do not affect management account
    - Restricts what root users can do
- `Centralised Logging account` to aggregate all organisational CloudTrail logs 
## Resource Access Manager (RAM)
- `Resource Access Manager (RAM)` free services that allows you to share AWS resources with other accounts inside or outside your organisation
- Resources that can be shared
    - Transit gateway
    - VPC subnets
    - Licence manager
    - Route 53 Resolver rules and endpoints
    - Dedicated hosts
- `Owners` create and manage the VPC resources that get shared
    - Cannot delete or modify resources deployed by participant accounts
- `Participant Accounts` able to provision services into the shared VPC subnets
    - Cannot delete or modify shared resources 
## Config
- `Config` fully managed service that provides you with an resource inventory, configuration history, and configuration change notifications to enable security and governance.
- inventory management and control tool
- it allows you to show the configuration history of infrastructure over time
- `Config Rules` created to ensure resources conform to your requirements
    - Rules are evaluated on a schedule or by a trigger
    - Capable of receiving alerts via SNS
    - Can be automatically fixed using SSM automation documents and Lambda
    - Multi-account, multi-region data aggregation gives you an enterprise-wide view of compliance status
    - can associate your AWS organization to quickly add your accounts.
- Configured on a per region basis
    - Results can be aggregated across accounts and regions
- Can easily discover what architecture you have in your account
- Can be used to detect resources that have not be tagged according to company policy
    - Can be used to [automatically detect when S3 buckets have been made public](https://aws.amazon.com/blogs/security/how-to-use-aws-config-to-monitor-for-and-respond-to-amazon-s3-buckets-allowing-public-access/)
- Record software configuration changes within your EC2 instances and servers running on-premises, as well as servers and Virtual Machines in environments provided by other cloud providers. You gain visibility into:
    - operating system configurations
    - system-level updates
    - installed applications
    - network configuration
- `Configuration snapshot` a point-in-time capture of all your resources and their configurations. 
- `Config records` details of changes to your AWS resources to provide you with a configuration history, and automatically deliver it to an S3 bucket you specify.
## Directory Service
- `Directory Service` fully managed version of Active Directory
- Types
    - `Managed Microsoft AD` entire AD suite, easily build out AD on AWS
    - `AD Connector` creates a tunnel between AWS and on-prem AD
    - `Simple AD` standalone directory powered by Linux Samba AD compatible server
## Pricing Calculator
- [Pricing Calculator](https://calculator.aws/#/) can be used to calculate costs
## Billing and Cost Management
- [Billing and Cost Management](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/billing-what-is.html) provides a suite of features to help you set up your billing, retrieve and pay invoices, and analyze, organize, plan, and optimize your costs.
- Primary dashboard to see your monthly AWS bill, access account activity, and view AWS payment history. 
- Understand your monthly charges, view and pay invoices, and manage preferences for billing, invoices, tax, and payments.
- Analyze your costs, export detailed cost and usage data, and forecast your spending.
- Organize your costs across teams, applications, or end customers.
- Estimate the cost of a planned workload, and create budgets to track and control costs.
- Optimize resource usage and use flexible pricing models to lower your bill.
## Cost Explorer
- `Cost Explorer` tracks and analyses your AWS usage.
- Use to view custom reports and analyse costs
- free for all accounts
- must be enabled before it can be used
- allows you to visualise and analyse your cloud costs
- Can generate custom reports from resource tags
- Can forecast costs up to 12-months
    - view data for up to the last 12 months, forecast how much you’re likely to spend for the next three months
- Can filter by time, service, tag, category etc.
- `Cost Explorer API` programmatically access the usage cost-related data they need on specific services.
## Budgets
- `Budgets` manage budgets for your account.
- Use to `set` budgets
- allows you to plan and set expectations around cloud costs
- Can track ongoing spend
- Can add alerts to let users know they are close to spend allocation
    - alert you when your costs or usage exceed or are forecasted to exceed your budgeted amount.
- Types of budgets
    - `Cost budgets` spending on a service
    - `Usage Budgets` spending on one or many services
    - `Reserved Instance Utilisation Budgets` utilisation threshold, under/over utilisation
    - `Reserved Instance Coverage Budget` how much of instance usage is covered by a reservation
    - `Savings Plan Utilisation Budgets` utilisation threshold, under/over utilisation
    - `Savings Plan Coverage Budgets` how much of instance usage is covered by savings plans
## Cost and Usage Reports
- `Cost and Usage Reports (CUR)` provides information about your use of AWS resources and estimated costs for that usage.
- Use when you need detailed, raw dataset for custom analysis or for integration with business intelligence tools.
- most comprehensive set of cost and usage data available for AWS spending
- depends on `cost allocation tags` to aggregate, map, and report the data
- Publish billing reports to S3 for centralised collection
    - Updates these reports once a day using CSV format
    - stored in an S3 bucket
- Break costs down by time span, service, resource, tags etc.
- Integrates with Athena, Redshift, QuickSight
- Uses
    - AWS Organisations
    - Track savings plans
    - Monitor on-demand capacity reservation
    - Break down data transfer charges
    - Cost allocation tag resource spending
### Cost Allocation Tags
- [Cost Allocation Tags](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html) tags that track and organize your resource costs on your cost allocation report, to make it easier for you to categorize and track your AWS costs. 
## Compute Optimizer
- `Compute Optimizer` service that analyses config and utilisation metrics of AWS resources
- Disabled by default
- `Savings Plans` offer flexible pricing models for long-term commitment
    - 1 or 3 year deals
    - up to 72% savings on compute
    - Applies to EC2, Lambda, Fargate, SageMaker
    - Savings plan types
        - `Compute` applies to EC2, Lambda or Fargate
            - Up to 66% off
            - Most flexible savings plan
            - Any family or region
        - `EC2 Instance` applies to EC2 instances of specific family and region
            - Up to 72% off
            - Stricter savings plan
        - `SageMaker` applies to SageMaker instances regardless or family or size
            - any region and any component
            - Up to 64% off
- Reports current usage optimisations and recommendations
- Graphs historical data
- Works with EC2, Auto Scaling Groups, EBS, Lambda
- Supported Accounts
    - `Standalone` account without organisations enabled
    - `Management Account/ Payer Account` primary account that hosts and manages the organisation
    - `Member accounts` all other accounts that belong to the organisation
## Trusted Advisor
- `Trusted Advisor` fully managed best-practice auditing tool
- Inspects account and makes recommendations
    - Categories
        - Cost Optimisation
        - Performance
        - Security
        - Service Limits
        - Fault Tolerance
    - Uses industry and customer-established standards to check account 
- Different levels of support depending on plan
## Control Tower
- `Control Tower` service to set up and govern multi-account environment
- Extends AWS organisations
- `Account Factory` Automates account creation and security controls
- `Landing Zone` well-architected, multi-account environment based on compliance and security best practices
    - Each organization can have one landing zone
    - `Organizational Units (OUs)`
    - `Shared Accounts` three accounts used by Control Tower during Landing Zone Creation
        - `management account` root user for this account and the IAM user or IAM administrator user for this account have full access to all resources within your landing zone.
        - `audit account` restricted to security and compliance teams with auditor (read-only) and administrator (full-access) cross-account roles to all accounts in the landing zone
        - `log archive account` contains a central Amazon S3 bucket for storing a copy of all AWS CloudTrail and AWS Config log files for all other accounts in your landing zone
    - `Root` parent that contains all OUs.
    - `Security OU` contains the shared accounts.
    - `Sandbox OU` contain the registered accounts used by your users to carry out their AWS workloads.
    - `IAM Identity Center directory` scope of permissions of each user.
    - `IAM Identity Center users` identities that your users can use to perform AWS workloads.
- `Guardrails` high level rules providing continuos governance for AWS environments
    - Applies to both OU and AWS accounts within the OU
    - `Preventative` disallow violating actions using Service Control Policies
        - Supported in all regions
    - `Detective` detects and alerts using Config rules
        - Only apply to certain regions
- `Account Factory` Automates provisioning of new accounts.
- `CloudFormation StackSet` automated deployments of templates deploying repeated resources for governance
- `Log Archive account` for centralized security logs and an Audit account for any SNS notifications around compliance violations.
    - managed solution to centralize all CloudTrail logs and alert on config changes as well. 
    - The Log Account and Audit account are both locked down by default, and the Organization admins must grant access. 
## Licence Manager
- `Licence Manager` service that handles software licence management
- Can set usage limits on licences to help licence abuse
## Personal Health Dashboard
- `Health/ Personal Health Dashboard` provides visibility of resource performance and availability of services and accounts
- Can view upcoming maintenance tasks
    - Can automate actions based on incoming events using EventBridge
- Has instant delivery of alerts
- `Health Event` sent on behalf of AWS services or AWS
- `Account Specific Events` specific to your account
- `Public Events` reported on public services, not specific to accounts
- `Event Type Code` includes affected services and type of event
- `Event Type Category` category attached to each event
- `Event Status` open, closed, upcoming
- `Affected Entities` AWS resources affected by event
## Service Catalog and Proton
- `Service Catalog` used by organisations to create and manage catalogs of approved IT services
    - List AMIs, servers, software, databases, preconfigured components
    - Centrally managed
    - Written and listed using CloudFormation templates
- `Proton` service that creates and manages infrastructure and deployment tooling for users, serverless and container-based applications
    - Automates Infrastructure as Code (IaC) provisioning
    - Automatically configures CI/CD pipelines and deploys code
    - Supports CloudFormation and Terraform template
## OpsWorks
- [OpsWorks](https://tutorialsdojo.com/aws-opsworks/) configuration management service that helps you configure and operate applications in a cloud enterprise 
- `OpsWorks for Chef Automate` let you use Chef cookbooks and solutions for configuration management
- `OpsWorks for Puppet Enterprise` lets you configure a Puppet Enterprise master server in AWS.

# Migration
## Snow Family
- `Snow Family` set of secure appliance that provide petabyte-scale data collection and processing solutions for migration to/from AWS services
- Offer built-in compute capabilities to allow customers to run operations in remote locations
- `Snowcone` smallest device in the snow family
    - 8TB storage, 4GB memory, 2 vCPUs
    - For easy to migrate data after it's been processed
    - IoT sensors integration
    - Good for environments where power and space are constrained
- `Snowball edge` jack of all trades
    - 48-81 TB, different memory and vCPU capacities
    - Perfect for off-the-grid computing or migration
    - Can be used for large database migrations
        - Used with Schema Conversion Tool 
- `Snowmobile` heavy lifter, physical truck
    - 100PB storage
    - designed for data center migrations
## Storage Gateway
- `Storage Gateway` service that gives your applications seamless and secure integration between on-premises environments and AWS storage.
- hybrid cloud storage that helps merge on-prem resources with the cloud
- Helps with one-time or long-term migration to cloud
- Virtual machines that run on-prem provided by AWS
- `File Gateway` caching of local files
    - NFS or SMB mount
    - Backs up data to S3
- `Volume Gateway` backs up drives to the cloud
    - iSCSI mount
    - `Cached volumes` store your data in S3 and retain a copy of frequently accessed data subsets locally.
    - `Stored volumes` low-latency access to your entire dataset, first configure your on-premises gateway to store all your data locally
    - Create EBS snapshots
- `Tape Gateway` replaces physical tapes
    - Backs up tapes to Glacier Deep Archive
    - Doesn't change current workflow, tricks services into thinking they are backing up to tape but it's really AWS
    - Encrypted communication
## DataSync
- `DataSync` data transfer service that facilitates moving data between on-premises storage and Amazon EFS, Amazon FSx, and Amazon S3
- agent-based solution for migrating on-prem storage to cloud
- usually uses an agent, an agent is not required
- Move data from NFS and SMB shares to AWS storage
- Good for moving large amounts of data in a one-time migration
- Saves data to S3, EFS, or FSx for Windows File Server
- can transfer data to archival storage, such as S3 Glacier Deep Archive.
- encrypts data in-transit via TLS.
## Transfer Family
- `Transfer Family` allows you to move files out of S3 or EFS
- Uses SFTP, FTPS or FTP protocols
    - FTP is only supported inside VPC for security reasons
- Used mostly for legacy applications that cannot be changed
- DNS entry stays the same but location for storage becomes S3
## Migration Hub
- `Migration Hub` single place to track progress of application migration to AWS
## Server Migration Service
- `Server Migration Service` used to move on-prem servers to AWS
- Can schedule when copying of VM takes place
- Converts VMWare to AMI
## Database Migration Service
- `Database Migration Service` used to move databases to AWS databases services
- Migration Types
    - `Full Load` move all existing data from sources to target in parallel
    - `Full load and Change Data Capture` full load and capture changes to source tables during migration
        - Guarantees transactional integrity of database
    - `Change Data Capture` only replicate the data changes from the source 
    - [Heterogeneous Database Migrations](https://docs.aws.amazon.com/prescriptive-guidance/latest/migration-oracle-database/heterogeneous-migration.html) source and target databases engines are different
        - schema and code must be transformed before the data migration starts.
        1. Used SCT to convert the source schema and code to match that of the target database. 
        2. Used DMS to Migrate data from the source database to the target database.
- `Schema Conversion Tool (SCT)` used to covert on-prem databases to AWS databases
    - Used for heterogeneous database migrations
    - Convert from relational, data warehouses, NoSQL and other data stores
    - Convert to Aurora, Redshift, RDS, or Databases running on EC2
    - can also scan your application source code for embedded SQL statements and convert them as part of a database schema conversion project
    - can help migrate data from various data warehouses to Redshift by using built-in data migration agents
- Should use `Snowball Edge` to move large databases with Schema Conversion Tool 
- Can be used for one-time or ongoing migrations
- Can keep same engine
- Can migrate from different engines, Oracle to PostgreSQL
- can migrate data to Amazon S3 
    - both full load and change data capture (CDC) data is written csv by default
- Process
    1. DMS is a server running replication software
    2. Create source and target connections/endpoints
    3. Schedule tasks to run on the DMS server to move data
    4. Creates tables, indexes and primary keys if they don't already exist
            - Optionally, create target tables before hand
## Application Discovery Service and Application Migration Service
- Used to migrate workloads to AWS
- `Application Discovery Service` helps plan migrations to AWS via collection of usage and config data from on-prem servers
    - Integrates with migration hub
    - Discovery types
        - `Agentless` OVA file within the VMWare vCenter
        - `Agent based` application discover agent on each VM and physical server
            - Installer for Windows and Linux
- `Application Migration Service (MGN)` lift-and-shift service for expediting application migration to AWS
    - Replicate source servers and translates infrastructure to AWS services
    - `Recovery Time Objective` minutes, dependent on OS boot time
    - `Recovery Point Objective` measured in sub-second range
    - [Replication Agent](https://docs.aws.amazon.com/drs/latest/userguide/What-Agent-Do.html) installed on source servers
        - performs an initial block-level read of the content of any volume attached to the server and replicates it to the replication server. 
        - acts as an OS-level read filter to capture writes and synchronizes any block level modifications to the Elastic Disaster Recovery replication server
            - ensures near-zero RPO.
    - does not offer a way of automatically refactor your existing infrastructure to better fit AWS


# Front-End Web and Mobile
## Amplify
- `Amplify` suite of tools for front-end and mobile development
- Allows developers to quickly build full-stack applications
- `Amplify Hosting` service that provides hosting for web apps
    - that supports single-page application frameworks, React, Angular, Vue
    - Supports static site generators, Gatsby, Hugo
    - Separate production and staging environments for front and back end
    - Support for Server Side Rendering, Next.js
- `Amplify Studio` visual interface that allows developers to easily build and deploy web and mobile apps
    - Easy authentication
    - Visual development environment
    - Ready-to-use components, easy creation of backends, automated connections between front and back ends  
## Device Farm
- `Device Farm` application testing service for testing and interacting with Android, iOS and web apps
- Provides actual phones and tablets hosted by AWS
- Testing methods
    - `Automated` upload scripts or use built-in tests for automated parallel tests on mobile devices
    - `Remote access` swipe, gesture, and interact with devices in real time via web browsers
## Pinpoint
- `Pinpoint` service that allows you to engage with customers through messaging channels
- Emails, SNS
- Meant for marketers, business users, and sometimes devs
- Features
    - `Projects` collection of information, segments, campaigns, and journeys
    - `Channels` platform where you intend to engage your audience segments
    - `Segments` dynamic or imported, designates which users receive specific messages
    - `Campaigns` initiatives engaging specific audience segments using tailored messages
    - `Journeys` customised, multi-step engagements
    - `Message Templates` content and settings for easily reusing repeated templates
    - `Machine Learning` use models to predict user patterns
- Uses
    - Marketing
    - Transactions, order confirmations
    - Bulk communications
## AppSync
- [AppSync](https://tutorialsdojo.com/aws-appsync/) scalable GraphQL interface for application developers
- serverless 
- Combine data from multiple sources, such as DynamoDB and Lambda
- Data interaction via GraphQL
- `GraphQL` data language that enables apps to fetch from servers
- Integrates with React, ReactNative, iOS and Android
- Uses
    - Fetching app data
    - Declarative coding
    - Frontend app data fetching
- `GraphQL Schema` each GraphQL API is defined by a single GraphQL schema.
- `Data Source` AWS resources that GraphQL APIs can interact with.
- `Resolvers` uses mapping templates to convert a GraphQL expression into a format that the data source can use.
    - `Unit resolver` performs a single operation against a predefined data source.
    - `Pipeline resolver` executes multiple operations against multiple data sources.


# Machine Learning
## Comprehend
- `Comprehend` uses NLP to help understand meaning and sentiment of text
    - [Comprehend Medical](https://aws.amazon.com/comprehend/medical/) Extract information from unstructured medical text accurately and quickly
## Kendra
- `Kendra` allows you to create intelligent search service powered by ML
    - Helps search information stored in different locations, S3, Databases
## Textract
- `Textract` allows you to process handwriting, text, tables and more
## Forecast
- `Forecast` time-series forecasting service
- Designed to give business insights
- Can take data from TimeStream storage
## Fraud Detector
- `Fraud Detector` service built to detect fraud in your data
- Build model based on your data
- Uses
    - Account fraud
    - Suspicious online payments
## Polly
- `Polly` turns text to lifelike speech
##  Transcribe
- `Transcribe` converts audio and video files to text
## Lex
- `Lex` allows you to build conversational interfaces (bot) in your applications
## Rekognition
- `Rekognition` computer vision service that allows you to automate the recognition of pictures and videos
- Uses
    - Content moderation
    - Face detection
    - Celebrity recognition
    - Video event detection
## SageMaker
- `SageMaker` service that allows you to build and deploy machine learning models in the AWS cloud
- Components
    - `Ground Truth` manage labelling  of jobs for training datasets using active and human labelling
    - `Notebook` Jupyter Notebook environment in python
    - `Training` train and tune models
    - `Inference` package and deploy models
- `Offline Usage` async or batch usage
    - Generate predictions for entire data set at once
    - Uses SageMaker batch transform
    - Input/output varies depending on model
- `Online Usage` synchronous or real-time usage
    - Generate low-latency predictions
    - Uses SageMaker hosting services
    - Input varies depending on model
    - Output is JSON string
- Model stages
    1. Create a model
    2. Create an endpoint config/ production variant
        - Specify model, inference instance type, instance count, variant name, weight
    3. Create an endpoint/ publish model
- `SageMaker Neo` customise models for specific CPU processors
- `Elastic Interface` speeds up throughput and decreases latency of real-time inferences
    - Uses only CPU-based instances rather than GPUs, more cost effective
- `Automatic Scaling` dynamically adds/removes instances to a production variant
    - Define scaling policy using CloudWatch metrics
- SageMaker is high availability
## Translate
- `Translate` service that translates text into other languages
- Highly accurate and continuously improving
## Bedrock
- [Bedrock](https://tutorialsdojo.com/amazon-bedrock/) managed service that allows you to build and scale generative AI applications. 
    - These applications can generate text, images, audio, and synthetic data in response to prompts.
## Personalise
- [Personalise](https://tutorialsdojo.com/amazon-personalize/) fully managed machine learning service for building recommendation systems.
- allows you to train, build, and deploy recommendation models without an extensive machine learning experience.
- Offers batch and real-time recommendations.
## Deeplens
- [Deeplens](https://tutorialsdojo.com/aws-deeplens/) deep learning-enabled camera for developers
- A wireless-enabled camera integrated with AWS Cloud
- Optimized for Apache MXNet, TensorFlow, and Caffe
- Integrates with Amazon Rekognition for advanced image analysis


# Media
## Elastic Transcoder
- `Elastic Transcoder` covert/transcode media files from source format into versions optimised for various devices
- Elastically scalable for large files
## Kinesis Video Streams
- `Kinesis Video Streams` service to stream media content from a large number of devices to AWS 
- Allows you to processing streamed media
- Elastically scalable for a large number of devices
- Uses  
    - Smart devices
    - Industrial automation