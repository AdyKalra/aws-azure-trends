# Architecting for Reliability on AWS
## AWS Well architected framework 
  * **CORPS** (Cost optimization , Operational excellence , Reliability , Performance efficiency , Security ) 
  * **Operational Excellence** - The operational excellence pillar focuses on **running and monitoring systems to deliver business value, and continually improving processes and procedures**. Key topics include managing and automating changes, responding to events, and defining standards to successfully manage daily operations.
  * **Security** - The security pillar focuses on **protecting information & systems**. Key topics include confidentiality and integrity of data, identifying and managing who can do what with privilege management, protecting systems, and establishing controls to detect security events.
  * **Reliability** - The reliability pillar focuses on the **ability to prevent, and quickly recover from failures to meet business and customer demand**. Key topics include foundational elements around setup, cross project requirements, recovery planning, and how we handle change.
  * **Performance Efficiency** - The performance efficiency pillar focuses on **using IT and computing resources efficiently**. Key topics include selecting the right resource types and sizes based on workload requirements, monitoring performance, and making informed decisions to maintain efficiency as business needs evolve.
  * **Cost Optimization** - Cost Optimization focuses on **avoiding un-needed costs**. Key topics include understanding and controlling where money is being spent, selecting the most appropriate and right number of resource types, analyzing spend over time, and scaling to meet business needs without overspending.
* The **AWS Well-Architected Tool** - Define a **workload based on one of your existing cloud applications** and review the answers.
* AWS is called Amazon web services since everything can be accessed using a REST based API 


## **Identity and Access Management** 
- is a web service for **securely controlling access to AWS services**. With IAM, you can centrally manage users, security credentials such as access keys, and permissions that control which AWS resources users and applications can access. You use IAM to **control who is authenticated (signed in) and authorized (has permissions) to use resources**.
  * **Principals** - A person or application that uses the AWS account root user, an IAM user, or an IAM role to sign in and make requests to AWS.
  * An IAM user doesn't have to represent an actual person; you can create an **IAM user** in order to generate an access key for an application that runs in your corporate network and needs AWS access.
  * **Federating Existing Users** - If the users in your organization already have a way to be authenticated, such as by signing in to your corporate network, you don't have to create separate IAM users for them. Instead, you can **federate those user identities into AWS.**
    * If your corporate directory is compatible with **Security Assertion Markup Language 2.0 (SAML 2.0)**, you can configure your corporate directory to provide **single-sign on (SSO) access**
    * If you are creating a mobile app or web-based app that can let users identify themselves through an Internet identity provider like Login with Amazon, Facebook, Google, or any OpenID Connect (OIDC) compatible identity provider
    * If your corporate directory is **Microsoft Active Directory, you can use AWS Directory Service**
  * **Identity-based policies** control what actions the identity can perform, on which resources, and under what conditions.
  * **Resource-based policies** control what actions a specified principal can perform on that resource and under what conditions. Resource-based policies are inline policies, and there are no managed resource-based policies
  * **Attribute-based access control (ABAC)** is an authorization strategy that defines permissions based on attributes. In AWS, these attributes are called **tags**.
  * In Amazon Elastic Compute Cloud you log into an instance with a key pair (for Linux instances) or using a user name and password (for Microsoft Windows instances).
  * In Amazon Relational Database Service you log into the database engine with a user name and password that are tied to that database.
  * In Amazon WorkSpaces, users sign in to a desktop with a user name and password.
  * In Amazon WorkDocs, users get access to shared documents by signing in with a user name and password.
  * **IAM Access Analyzer** - helps you identify the resources in your organization and accounts, such as Amazon S3 buckets or IAM roles, that are shared with an external entity.
    * Access Analyzer analyzes only policies that are applied to resources in the same AWS Region that it's enabled in. To monitor all resources in your AWS environment, you must create an analyzer to enable Access Analyzer in each Region
 
 * **Run cost as architecture fitness function** - https://www.thoughtworks.com/radar/techniques?blipid=1338
 
  * **AWS Security Token Service (STS)** is a web service that enables you to request temporary, limited-privilege credentials for AWS Identity and Access Management (IAM) users or for users that you authenticate (federated users).
 
  * **IAM Best Practices**
    * Lock Away Your AWS Account Root User Access Keys
    * Create Individual IAM Users
    * Use Groups to Assign Permissions to IAM Users
    * Grant Least Privilege
    * Get Started Using Permissions with AWS Managed Policies
    * Use Customer Managed Policies Instead of Inline Policies
    * Use Access Levels to Review IAM Permissions
    * Configure a Strong Password Policy for Your Users
    * Enable MFA
    * Use Roles for Applications That Run on Amazon EC2 Instances
    * Use Roles to Delegate Permissions
    * Do Not Share Access Keys
    * Rotate Credentials Regularly
    * Remove Unnecessary Credentials
    * Use Policy Conditions for Extra Security
    * Monitor Activity in Your AWS Account

## **AWS CloudTrail** 
is an AWS service that helps you enable governance, compliance, and operational and risk auditing of your AWS account. Actions taken by a user, role, or an AWS service are recorded as events in CloudTrail. **Events include actions taken in the AWS Management Console, AWS Command Line Interface, and AWS SDKs and APIs.**
  * **Event History** - stores all events for 90 days unless a trail is created and sent to the s3 bucket.

  * Working with CloudTrail Log Files
     * Create multiple trails per region.
     * **Monitor CloudTrail log files by sending them to CloudWatch Logs.**
     * Share log files between accounts.
     * Use the AWS CloudTrail Processing Library to write log processing applications in Java.
     * Validate your log files to verify that they have not changed after delivery by CloudTrail.
   
   * You can configure your trails to log the following:
     * **Data events**: These events provide visibility into the resource operations performed on or within a resource. These are also known as data plane operations.
     * **Management events**: Management events provide visibility into management operations that are performed on resources in your AWS account. These are also known as control plane operations. 
     * **Insights events**: Insights events capture unusual activity that is detected in your account. If you have Insights events enabled, and CloudTrail detects unusual activity, Insights events are logged to the destination S3 bucket for your trail, but in a different folder. 
   
## **CloudWatch** 
monitors your Amazon Web Services (AWS) resources and the applications you run on AWS in real time. You can use CloudWatch to collect and track metrics, which are variables you can measure for your resources and applications.
  * create custom dashboards to display metrics about your custom applications, and display custom collections of metrics that you choose.
  * create alarms which watch metrics and send notifications or automatically make changes to the resources you are monitoring when a threshold is breached
  
  * **Amazon CloudWatch Synthetics** enables you to create canaries to monitor your endpoints and APIs. **Canaries are configurable scripts that follow the same routes and perform the same actions as a customer**. This enables the outside-in view of your customers’ experiences, and your service’s availability from their point of view.
  
  * **CloudWatch ServiceLens enhances the observability of your services and applications by enabling you to integrate traces, metrics, logs, and alarms into one place.** ServiceLens integrates **CloudWatch with AWS X-Ray to provide an end-to-end view of your application to help you more efficiently pinpoint performance bottlenecks and identify impacted users.** A **service map** displays your service endpoints and resources as “nodes” and highlights the traffic, latency, and errors for each node and its connections. You can choose a node to see detailed insights about the correlated metrics, logs, and traces associated with that part of the service. This enables you to investigate problems and their effect on the application.

  * **Contributor Insights** to analyze log data and create time series that display contributor data. You can see metrics about the top-N contributors, the total number of unique contributors, and their usage. This helps you find top talkers and understand who or what is impacting system performance. For example, you can find bad hosts, identify the heaviest network users, or find the URLs that generate the most errors.
 
  *  **CloudWatch Container Insights** to collect, aggregate, and summarize metrics and logs from your containerized applications and microservices. Container Insights is available for Amazon Elastic Container Service, Amazon Elastic Kubernetes Service, and Kubernetes platforms on Amazon EC2.
  
 * AWS provides two levels of protection against DDoS attacks: **AWS Shield Standard and AWS Shield Advanced**.Is a **managed distributed denial of service(DDOS) protection**. AWS Shield Standard is automatically included at no extra cost beyond what you already pay for AWS WAF and your other AWS services. For added protection against DDoS attacks, AWS offers AWS Shield Advanced. AWS Shield Advanced provides expanded DDoS attack protection for your Amazon EC2 instances, Elastic Load Balancing load balancers, Amazon CloudFront distributions, and Amazon Route 53 hosted zones.


### **AWS Config for Change Management** 
provides a detailed view of the resources associated with your AWS account, including how they are configured, how they are related to one another, and how the configurations and their relationships have changed over time.
  * **Config rules** which represent your ideal configuration settings. AWS Config provides customizable, predefined rules called **managed rules** to help you get started. You can also create your own custom rules. While AWS Config continuously tracks the configuration changes that occur among your resources, it checks whether these changes violate any of the conditions in your rules. If a resource violates a rule, AWS Config flags the resource and the rule as **noncompliant.**

For example, when an EC2 volume is created, AWS Config can evaluate the volume against a rule that requires volumes to be encrypted. If the volume is not encrypted, AWS Config flags the volume and the rule as noncompliant
  * **AWS Config uses Amazon Simple Notification Service (SNS) topics to send you notifications every time a supported AWS resource** is created, updated, or otherwise modified as a result of user API activity. 
  * **If you want to programmatically consume the data from AWS Config in these or other ways, use an Amazon Simple Queue Service queue as the notification endpoint for Amazon SNS.**

  * With AWS Config, you can do the following:
    * Evaluate your AWS resource configurations for desired settings.
    * Get a snapshot of the current configurations of the supported resources that are associated with your AWS account.
    * Retrieve configurations of one or more resources that exist in your account.
    * Retrieve historical configurations of one or more resources.
    * Receive a notification whenever a resource is created, modified, or deleted.
    
    * View relationships between resources. For example, you might want to find all resources that use a particular security group.

## **AWS Trusted Advisor** 
is an online tool that provides you real time guidance to help you provision your resources following AWS best practices. Whether establishing new workflows, developing applications, or as part of ongoing improvement, take advantage of the recommendations provided by Trusted Advisor on a regular basis to help keep your solutions provisioned optimally.
  * **Cost Optimization** See how you can save money on AWS by eliminating unused and idle resources or making commitments to reserved capacity
  * **Security** Improve the security of your application by closing gaps, enabling various AWS security features, and examining your permissions.
  * **Fault Tolerance** Increase the availability and redundancy of your AWS application by take advantage of auto scaling, health checks, multi AZ, and backup capabilities.
  * **Performance** Improve the performance of your service by checking your service limits, ensuring you take advantage of provisioned throughput, and monitoring for overutilized instances.
  * **Service Limits** Checks for service usage that is more than 80% of the service limit. Values are based on a snapshot, so your current usage might differ. Limit and usage data can take up to 24 hours to reflect any changes.

# Architecting for availability and Fault Tolerance

### ** Availability zones and regions**

## EC2 Instances - Launching an EC2 Instance into an Availability Zone
**Amazon Elastic Compute Cloud (Amazon EC2)** provides scalable computing capacity in the Amazon Web Services (AWS) cloud. Using Amazon EC2 eliminates your need to invest in hardware up front, so you can develop and deploy applications faster.
 * You can use Amazon EC2 to launch as many or as few virtual servers as you need, configure security and networking, and manage storage. 
 * EC2 enables you to scale up or down to handle changes in requirements or spikes in popularity, reducing your need to forecast traffic.
 
### **Amazon EC2 provides the following features:**

 * Virtual computing environments, known as **instances**
 * Preconfigured templates for your instances, known as **Amazon Machine Images (AMIs)**, that package the bits you need for your server (including the operating system and additional software)
 * Various configurations of CPU, memory, storage, and networking capacity for your instances, known as **instance types**
 * Secure login information for your instances using key pairs (AWS stores the public key, and you store the private key in a secure place)
 * Storage volumes for temporary data that's deleted when you stop or terminate your instance, known as instance **store volumes**
 * Persistent storage volumes for your data using Amazon Elastic Block Store (Amazon EBS), known as **Amazon EBS volumes*
 * Multiple physical locations for your resources, such as instances and Amazon EBS volumes, known as **Regions and Availability Zones**
 * A firewall that enables you to specify the protocols, ports, and source IP ranges that can reach your instances using security groups
 * Static IPv4 addresses for dynamic cloud computing, known as **Elastic IP addresses**
 * Metadata, known as **tags**, that you can create and assign to your Amazon EC2 resources
 * Virtual networks you can create that are logically isolated from the rest of the AWS cloud, and that you can optionally connect to your own network, known as **virtual private clouds (VPCs)**
 
### Best practices for Windows on Amazon EC2
* Update Windows drivers
  * Leverage Trusted Advisor to keep Amazon EC2 Windows up to date with AWS-provided Windows drivers.
  * Use SNS topics to receive updates for new driver releases.
  * Use the AWS Systems Manager SSM document AWSSupport-UpgradeWindowsAWSDrivers to easily apply the updates across your instances.
* Launch new instances with the latest Windows AMIs
* Test system/application performance before migration
* Update launch agents
* Use separate Amazon EBS volumes for the operating system versus your data. Ensure that the volume with your data persists after instance termination

### **Amazon Elastic Graphics**
provides flexible, low-cost, and high performance graphics acceleration for your Windows instances. Elastic Graphics is suited for applications that require a small or intermittent amount of additional graphics acceleration, and that use OpenGL graphics support. If you need access to full, directly attached GPUs and use of DirectX, CUDA, or Open Computing Language (OpenCL) parallel computing frameworks, use an accelerated computing instance type instance instead.

### **Amazon EC2 Auto Scaling**
helps you ensure that you have the correct number of Amazon EC2 instances available to handle the load for your application. You create collections of EC2 instances, called **Auto Scaling groups.**
 * You can specify the minimum number of instances in each Auto Scaling group, and Amazon EC2 Auto Scaling ensures that your group never goes below this size. You can specify the maximum number of instances in each Auto Scaling group, and Amazon EC2 Auto Scaling ensures that your group never goes above this size
 * If you specify the desired capacity, either when you create the group or at any time thereafter, Amazon EC2 Auto Scaling ensures that your group has this many instances. 
 * If you specify scaling policies, then Amazon EC2 Auto Scaling can launch or terminate instances as demand on your application increases or decreases.
 
### **VM Import/Export**
 * VM Import/Export enables you to import virtual machine (VM) images from your existing virtualization environment to Amazon EC2, and then export them back. This enables you to migrate applications and workloads to Amazon EC2, copy your VM image catalog to Amazon EC2, or create a repository of VM images for backup and disaster recovery.

### **Active Redundancy**
 * Load balancer managing servers between multiple availability zones.
### **Standby Redundancy**
 * Master DB in one of the AZs and Backup / standby DB with synchronous / asynchronous updates in another AZ
 
### **Vertical Scaling** small to large instance type
is increasing the size and computing power of a single instance or node without increasing the number of nodes or instances
### **Horizontal Scaling** add more instances of similar type 
 involves adding more processing units or phyiscal machines to your server or database. It involves growing the number of nodes in the cluster, reducing the responsibilities of each member node by spreading the key space wider and providing additional end-points for client connections.
 
## Architecting with Services Instead of Servers
 * **Managed services** - is a set of services and tools that automate infrastructure management tasks for Amazon Web Services (AWS) deployments. 
   * RDS
   * S3
   * DynamoDB
   * ELB
 *  key benefits of managed services include:
   * Proactive infrastructure management. To get the most out of AWS, you need to be an expert at AWS. ...
   * Ongoing business evolution support. The cloud thrives on change. ...
   * Cloud operations management. ...
   * Contractual agreements that structure responsibilities.
 * **Serverless Architecture** is a way to build and run applications and services without having to manage infrastructure. ... You no longer have to provision, scale, and maintain servers to run your applications, databases, and storage systems.
   * Lambda - > API gateway to run them over http -> S3 for content -> Cloudfront as a cdn with multiple edge locations
   
## **Implementing Loose Coupling**
systems should ideally be designed in a way that reduces inter-dependencies. Your components need to be loosely coupled to avoid changes or failure in one of the components from affecting others.
 * From Webserver -> Backend service (DB server) To Webserver -> SQS -> Lambda function to pull from Backend service (DB server)
 * also called **asynchronous messaging**
 * **loosely coupled microservices architecture**
   * Componentization via Services. ...
   * Organized around Business Capabilities. ...
   * Products not Projects. ...
   * Smart endpoints and dumb pipes. ...
   * Decentralized Governance. ...
   * Decentralized Data Management. ...
   * Infrastructure Automation. ...
   * Design for failure.
 
