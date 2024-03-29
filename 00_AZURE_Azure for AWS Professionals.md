## Azure for AWS Professionals

|  AWS 	| AZURE	| Description |   	
|:-:  |:-:  |:-:  |
|||**Compute - Virtual servers**|
|Elastic Compute Cloud (EC2) Instances|	Virtual Machines	|Virtual servers allow users to deploy, manage, and maintain OS and server software. Instance types provide combinations of CPU/RAM. Users pay for what they use with the flexibility to change sizes.|
|Batch	|Batch|	Run large-scale parallel and high-performance computing applications efficiently in the cloud.|
|Auto Scaling	|Virtual Machine Scale Sets	|Allows you to automatically change the number of VM instances. You set defined metric and thresholds that determine if the platform adds or removes instances.|
|VMware Cloud on AWS	|Azure VMware Solution	|Seamlessly move VMware-based workloads from your datacenter to Azure and integrate your VMware environment with Azure. Keep managing your existing environments with the same VMware tools you already know while you modernize your applications with Azure native services. Azure VMware Solution is a Microsoft service, verified by VMware, that runs on Azure infrastructure.|
|Parallel Cluster|	CycleCloud	|Create, manage, operate, and optimize HPC and big compute clusters of any scale|
|||**Object storage**|
| Simple Storage Services (S3)	| Blob storage|	Object storage service, for use cases including cloud applications, content distribution, backup, archiving, disaster recovery, and big data analytics.|
|||**Virtual server disks**|
| Elastic Block Store (EBS)	|managed disks	|SSD storage optimized for I/O intensive read/write operations. For use as high-performance Azure virtual machine storage.|
|||**Shared files**|
| Elastic File System	|Files	|Provides a simple interface to create and configure file systems quickly, and share common files. Can be used with traditional protocols that access files over a network.|
|||**Archiving and backup**|
| S3 Infrequent Access (IA)|	Storage cool tier	| Cool storage is a lower-cost tier for storing data that is infrequently accessed and long-lived.|
| S3 Glacier, Deep Archive|	Storage archive access tier	|Archive storage has the lowest storage cost and higher data retrieval costs compared to hot and cool storage.|
|Backup|	Backup	|Back up and recover files and folders from the cloud, and provide offsite protection against data loss.|
|||**Hybrid storage**|
| Storage Gateway	| StorSimple	|Integrates on-premises IT environments with cloud storage. Automates data management and storage, plus supports disaster recovery.|
|DataSync	|File Sync	|Azure Files can be deployed in two main ways: by directly mounting the serverless Azure file shares or by caching Azure file shares on-premises using Azure File Sync.|
|||**Bulk data transfer**|
| Import/Export Disk	|Import/Export|	A data transport solution that uses secure disks and appliances to transfer large amounts of data. Also offers data protection during transit.|
|Import/Export Snowball, Snowball Edge, Snowmobile	|Data Box	|Petabyte- to exabyte-scale data transport solution that uses secure data storage devices to transfer large amounts of data to and from Azure.|
|||**Serverless**|
|Lambda	|Functions	|Integrate systems and run backend processes in response to events or schedules without provisioning or managing servers.|
|||**Web applications**|
| Elastic Beanstalk	|App Service	|Managed hosting platform providing easy to use services for deploying and scaling web applications and services.|
|API Gateway|	API Management	|A turnkey solution for publishing APIs to external and internal consumers.|
|CloudFront	|Content Delivery Network	|A global content delivery network that delivers audio, video, applications, images, and other files.|
|Global Accelerator	|Front Door	|Easily join your distributed microservices architectures into a single global application using HTTP load balancing and path-based routing rules. Automate turning up new regions and scale-out with API-driven global actions, and independent fault-tolerance to your back end microservices in Azure-or anywhere.|
|Global Accelerator	|Cross-regional load balancer	|Distribute and load balance traffic across multiple Azure regions via a single, static, global anycast public IP address.|
|LightSail|	App Service	|Build, deploy, and scale web apps on a fully managed platform.|
|||**Database**|
|Relational database	RDS|	SQL Database, Database for MySQL, Database for PostgreSQL	| Managed relational database service where resiliency, scale, and maintenance are primarily handled by the platform.|
| NoSQL / Document	DynamoDB , SimpleDB , Amazon DocumentDB |	Cosmos DB	| A globally distributed, multi-model database that natively supports multiple data models: key-value, documents, graphs, and columnar.|
| Caching	ElastiCache	| Cache for Redis	| An in-memory–based, distributed caching service that provides a high-performance store typically used to offload nontransactional work from a database.|
| Database migration	Database Migration Service	|Database Migration Service	|Migration of database schema and data from one database format to a specific database technology in the cloud.|
|||**Miscellaneous**|
| Backend process logic	- Step Functions |	Logic Apps	|Cloud technology to build distributed applications using out-of-the-box connectors to reduce integration challenges. Connect apps, data and devices on-premises or in the cloud.|
| Enterprise application services	- WorkMail, WorkDocs |	Microsoft 365|	Fully integrated Cloud service providing communications, email, document management in the cloud and available on a wide variety of devices.|
|Gaming	- GameLift, GameSparks	|PlayFab	|Managed services for hosting dedicated game servers.|
|Media transcoding-	Elastic Transcoder	|Media Services|	Services that offer broadcast-quality video streaming services, including various transcoding technologies.|
|Workflow	-Simple Workflow Service (SWF)	|Logic Apps	|Serverless technology for connecting apps, data and devices anywhere, whether on-premises or in the cloud for large ecosystems of SaaS and cloud-based connectors.|
|Hybrid	- Outposts	|Stack	Azure |Stack is a hybrid cloud platform that enables you to run Azure services in your company's or service provider's datacenter. As a developer, you can build apps on Azure Stack. You can then deploy them to either Azure Stack or Azure, or you can build truly hybrid apps that take advantage of connectivity between an Azure Stack cloud and Azure.|
| Media - 	Elemental MediaConvert	|Media Services|	Cloud-based media workflow platform to index, package, protect, and stream video at scale.|
|||**Messaging and eventing**|
|Simple Queue Service (SQS)	|Queue Storage|	Provides a managed message queueing service for communicating between decoupled application components.|
|Simple Queue Service (SQS)	|Service Bus	|Supports a set of cloud-based, message-oriented middleware technologies including reliable message queuing and durable publish/subscribe messaging.|
|Amazon EventBridge	|Event Grid	|A fully managed event routing service that allows for uniform event consumption using a publish/subscribe model.|
|||**DevOps and application monitoring**|
| CloudWatch, X-Ray	|Monitor|	Comprehensive solution for collecting, analyzing, and acting on telemetry from your cloud and on-premises environments.|
| CodeDeploy, CodeCommit, CodePipeline	|DevOps	|A cloud service for collaborating on code development.|
|Developer Tools|	Developer Tools	|Collection of tools for building, debugging, deploying, diagnosing, and managing multiplatform scalable apps and services.|
|CodeBuild	|DevOps	|Fully managed build service that supports continuous integration and deployment.|
|Command Line Interface	|CLI|PowerShell	Built on top of the native REST API across all cloud services, various programming language-specific wrappers provide easier ways to create solutions.|
|AWS CloudShell	|Azure Cloud Shell|	Azure Cloud Shell is an interactive, authenticated, browser-accessible shell for managing Azure resources. It gives you the flexibility to choose the shell experience that best suits the way you work, either Bash or PowerShell.|
|OpsWorks (Chef-based)|	Automation	|Configures and operates applications of all shapes and sizes, and provides templates to create and manage a collection of resources.|
|CloudFormation	|Resource Manager , VM extensions , Azure Automation	|Provides a way for users to automate the manual, long-running, error-prone, and frequently repeated IT tasks.|
|||**Containers and container orchestrators**|
|Elastic Container Service (ECS) Fargate |	Container Instances	|Azure Container Instances is the fastest and simplest way to run a container in Azure, without having to provision any virtual machines or adopt a higher-level orchestration service.|
|Elastic Container Registry	|Container Registry	|Allows customers to store Docker formatted images. Used to create all types of container deployments on Azure.|
|Elastic Kubernetes Service (EKS)|	Kubernetes Service (AKS)	|Deploy orchestrated containerized applications with Kubernetes. Simplify monitoring and cluster management through auto upgrades and a built-in operations console. See AKS solution journey.|
|App Mesh	|Service Fabric Mesh	|Fully managed service that enables developers to deploy microservices applications without managing virtual machines, storage, or networking.|
|||**Analytics and visualization**|
|Kinesis Analytics	| Stream Analytics , Azure Data Explorer, Data Lake Analytics| Data Lake Store	Storage and analysis platforms that create insights from large quantities of data, or data that originates from many sources.|
|QuickSight|Power BI |Business intelligence tools that build visualizations, perform ad hoc analysis, and develop business insights from data.|
|CloudSearch	|Cognitive Search	|Delivers full-text search and related search analytics and capabilities.|
|Athena	|Data Lake Analytics|	Provides a serverless interactive query service that uses standard SQL for analyzing databases.|
|||**Data warehouse**|
|Redshift	|Synapse Analytics	|Cloud-based Enterprise Data Warehouse (EDW) that uses Massively Parallel Processing (MPP) to quickly run complex queries across petabytes of data.|
|Lake Formation	|Data Share|	A simple and safe service for sharing big data|
|||**Big data processing**|
|EMR	|Azure Data Explorer	|Fully managed, low latency, distributed big data analytics platform to run complex queries across petabytes of data.|
|EMR|	Databricks|	Apache Spark-based analytics platform.|
|EMR|	HDInsight	|Managed Hadoop service. Deploy and manage Hadoop clusters in Azure.|
|EMR|	Data Lake |Storage	Massively scalable, secure data lake functionality built on Azure Blob Storage.|
|||**Data orchestration / ETL**|
|Data Pipeline, Glue|	Data Factory	|Processes and moves data between different compute and storage services, as well as on-premises data sources at specified intervals. Create, schedule, orchestrate, and manage data pipelines.|
|Glue	|Data Catalog	|A fully managed service that serves as a system of registration and system of discovery for enterprise data sources|
|Dynamo DB| Table Storage, Cosmos DB |	NoSQL key-value store for rapid development using massive semi-structured datasets.|
|||**Mobile services**|
| Mobile Hub	|App Center , Xamarin Apps|	Provides backend mobile services for rapid development of mobile solutions, identity management, data synchronization, and storage and notifications across devices.|
|Mobile SDK	|App Center	|Provides the technology to rapidly build cross-platform and native apps for mobile devices.|
|Cognito	|App Center	|Provides authentication capabilities for mobile applications.|
|Device Farm	|App Center	|Provides services to support testing mobile applications.|
|Mobile Analytics	|App Center|	Supports monitoring, and feedback collection for the debugging and analysis of a mobile application service quality.|
|||**Firewall**|
| Web Application Firewall	| Web Application Firewall	| A firewall that protects web applications from common web exploits.|
|Web Application Firewall	|Firewall	|Provides inbound protection for non-HTTP/S protocols, outbound network-level protection for all ports and protocols, and application-level protection for outbound HTTP/S.|
|||**Networking**|
|Cloud virtual networking	- Virtual Private Cloud (VPC)|	Virtual Network|	Provides an isolated, private environment in the cloud. Users have control over their virtual networking environment, including selection of their own IP address range, creation of subnets, and configuration of route tables and network gateways.|
|Cross-premises connectivity	- VPN Gateway|	VPN Gateway	|Connects Azure virtual networks to other Azure virtual networks, or customer on-premises networks (Site To Site). Allows end users to connect to Azure services through VPN tunneling (Point To Site).|
|DNS management	- Route 53|	DNS	|Manage your DNS records using the same credentials and billing and support contract as your other Azure services|
| 53	| Traffic Manager	|A service that hosts domain names, plus routes users to Internet applications, connects user requests to datacenters, manages traffic to apps, and improves app availability with automatic failover.|
|Dedicated network	- Direct Connect	|ExpressRoute	|Establishes a dedicated, private network connection from a location to the cloud provider (not over the Internet).|
| Load balancing	- Network Load Balancer|	Load Balancer	|Azure Load Balancer load balances traffic at layer 4 (TCP or UDP). Standard Load Balancer also supports cross-region or global load balancing.|
|	Application Load Balancer	|Application Gateway	|Application Gateway is a layer 7 load balancer. It supports SSL termination, cookie-based session affinity, and round robin for load-balancing traffic.|
|||**Authentication and authorization**|
| Identity and Access Management (IAM)|	Azure Active Directory	|Allows users to securely control access to services and resources while offering data security and protection. Create and manage users and groups, and use permissions to allow and deny access to resources.|
|Identity and Access Management (IAM)|	Azure role-based access control|	Azure role-based access control (Azure RBAC) helps you manage who has access to Azure resources, what they can do with those resources, and what areas they have access to.|
|Organizations	|Subscription Management + Azure RBAC	|Security policy and role management for working with multiple accounts.|
|Multi-Factor Authentication	|Multi-Factor Authentication|	Safeguard access to data and applications while meeting user demand for a simple sign-in process.|
|Directory Service	|Azure Active Directory Domain Services	|Provides managed domain services such as domain join, group policy, LDAP, and Kerberos/NTLM authentication that are fully compatible with Windows Server Active Directory.|
|Cognito	|Azure Active Directory |B2C	A highly available, global, identity management service for consumer-facing applications that scales to hundreds of millions of identities.|
|Organizations	|Policy	Azure |Policy is a service in Azure that you use to create, assign, and manage policies. These policies enforce different rules and effects over your resources, so those resources stay compliant with your corporate standards and service level agreements.|
|Organizations	|Management Groups	|Azure management groups provide a level of scope above subscriptions. You organize subscriptions into containers called "management groups" and apply your governance conditions to the management groups. All subscriptions within a management group automatically inherit the conditions applied to the management group. Management groups give you enterprise-grade management at a large scale, no matter what type of subscriptions you have.|
|||**Security**|
| Inspector |	Security Center |	An automated security assessment service that improves the security and compliance of applications. Automatically assess applications for vulnerabilities or deviations from best practices.|
| Certificate Manager	| App Service Certificates available on the Portal|	Service that allows customers to create, manage, and consume certificates seamlessly in the cloud.|
|GuardDuty	|Advanced Threat Protection	|Detect and investigate advanced attacks on-premises and in the cloud.|
|Artifact|	Service Trust Portal	|Provides access to audit reports, compliance guides, and trust documents from across cloud services.|
|Shield|	DDos Protection Service	|Provides cloud services with protection from distributed denial of services (DDoS) attacks.|
|||**Encryption**|
| Server-side encryption with Amazon S3 Key Management Service	| Azure Storage Service Encryption	|Helps you protect and safeguard your data and meet your organizational security and compliance commitments.|
|Key Management Service (KMS), Cloud HSM	| Key Vault	| Provides security solution and works with other services by providing a way to manage, create, and control encryption keys stored in hardware security modules (HSM).|
|||**Marketplace**|
|AWS Marketplace |	Azure Marketplace |	Easy-to-deploy and automatically configured third-party applications, including single virtual machine or multiple virtual machine solutions.|
|||**AI and machine learning**|
| SageMaker | Machine Learning | A cloud service to train, deploy, automate, and manage machine learning models.|
| Alexa Skills Kit |	Bot Framework	| Build and connect intelligent bots that interact with your users using text/SMS, Skype, Teams, Slack, Microsoft 365 mail, Twitter, and other popular services. |
| Lex |	Speech Services	| API capable of converting speech to text, understanding intent, and converting text back to speech for natural responsiveness. |
| Lex	| Language Understanding (LUIS) |	Allows your applications to understand user commands contextually. |
|Polly, Transcribe |	Speech Services |	Enables both Speech to Text, and Text into Speech capabilities. |
|Rekognition	|Cognitive Services	| Computer Vision: Extract information from images to categorize and process visual data. Face: Detect, identify, and analyze faces in photos. Emotions: Recognize emotions in images. |
|Skills Kit|	Virtual Assistant	|The Virtual Assistant Template brings together a number of best practices we've identified through the building of conversational experiences and automates integration of components that we've found to be highly beneficial to Bot Framework developers.|
|||**Internet of things (IoT)**|
|IoT	|IoT Hub	|A cloud gateway for managing bidirectional communication with billions of IoT devices, securely and at scale.|
|Greengrass	|IoT Edge|	Deploy cloud intelligence directly on IoT devices to run in on-premises scenarios.|
|Kinesis Firehose, Kinesis Streams	|Event Hubs|	Services that allow the mass ingestion of small data inputs, typically from devices and sensors, to process and route the data.|
|IoT Things Graph	|Digital Twins	|Azure Digital Twins is an IoT service that helps you create comprehensive models of physical environments. Create spatial intelligence graphs to model the relationships and interactions between people, places, and devices. Query data from a physical space rather than disparate sensors.|
|||**Management**|
| Trusted Advisor	|Advisor|	Provides analysis of cloud resource configuration and security so subscribers can ensure they're making use of best practices and optimum configurations.|
|Usage and Billing Report	|Billing API	|Services to help generate, monitor, forecast, and share billing data for resource usage by time, organization, or product resources.|
|Management Console	|Portal	|A unified management console that simplifies building, deploying, and operating your cloud resources.|
|Application Discovery Service	|Migrate	|Assesses on-premises workloads for migration to Azure, performs performance-based sizing, and provides cost estimations.|
|EC2 Systems Manager|	Monitor	|Comprehensive solution for collecting, analyzing, and acting on telemetry from your cloud and on-premises environments.|
|Personal Health Dashboard	|Resource Health|	Provides detailed information about the health of resources as well as recommended actions for maintaining resource health.|
|CloudTrail	|Monitor|	Comprehensive solution for collecting, analyzing, and acting on telemetry from your cloud and on-premises environments.|
|CloudWatch	|Application Insights	|Application Insights, is an extensible Application Performance Management (APM) service for developers and DevOps professionals.|
|Cost Explorer	|Cost Management	|Optimize cloud costs while maximizing cloud potential.|


![1633322113298](https://user-images.githubusercontent.com/8856857/136013428-c1780681-7038-4864-bfbf-2da17a5b0de3.jpeg)
![1633322113427](https://user-images.githubusercontent.com/8856857/136013435-9e507813-be3a-44e9-8fb1-01e4e7185b74.jpeg)
