## Azure for AWS Professionals

|  AWS 	| AZURE	| Description |   	
|:-:  |:-:  |:-:  |
|||**Compute - Virtual servers**|
|Elastic Compute Cloud (EC2) Instances|	Virtual Machines	|Virtual servers allow users to deploy, manage, and maintain OS and server software. Instance types provide combinations of CPU/RAM. Users pay for what they use with the flexibility to change sizes.|
|Batch	|Batch|	Run large-scale parallel and high-performance computing applications efficiently in the cloud.|
|Auto Scaling	|Virtual Machine Scale Sets	|Allows you to automatically change the number of VM instances. You set defined metric and thresholds that determine if the platform adds or removes instances.|
|VMware Cloud on AWS	|Azure VMware Solution	|Seamlessly move VMware-based workloads from your datacenter to Azure and integrate your VMware environment with Azure. Keep managing your existing environments with the same VMware tools you already know while you modernize your applications with Azure native services. Azure VMware Solution is a Microsoft service, verified by VMware, that runs on Azure infrastructure.|
|Parallel Cluster|	CycleCloud	|Create, manage, operate, and optimize HPC and big compute clusters of any scale|
|||**Serverless**|
|Lambda	|Functions	|Integrate systems and run backend processes in response to events or schedules without provisioning or managing servers.|
|||**Database**|
|Relational database	RDS|	SQL Database, Database for MySQL, Database for PostgreSQL	| Managed relational database service where resiliency, scale, and maintenance are primarily handled by the platform.|
| NoSQL / Document	DynamoDB , SimpleDB , Amazon DocumentDB |	Cosmos DB	| A globally distributed, multi-model database that natively supports multiple data models: key-value, documents, graphs, and columnar.|
| Caching	ElastiCache	| Cache for Redis	| An in-memory–based, distributed caching service that provides a high-performance store typically used to offload nontransactional work from a database.|
| Database migration	Database Migration Service	|Database Migration Service	|Migration of database schema and data from one database format to a specific database technology in the cloud.|
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
