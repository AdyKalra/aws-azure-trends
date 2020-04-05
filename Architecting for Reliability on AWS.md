## Architecting for Reliability on AWS
* AWS Well architected framework 
  * **CORPS** (Cost optimization , Operational excellence , Reliability , Performance efficiency , Security ) 
  * **Operational Excellence** - The operational excellence pillar focuses on **running and monitoring systems to deliver business value, and continually improving processes and procedures**. Key topics include managing and automating changes, responding to events, and defining standards to successfully manage daily operations.
  * **Security** - The security pillar focuses on **protecting information & systems**. Key topics include confidentiality and integrity of data, identifying and managing who can do what with privilege management, protecting systems, and establishing controls to detect security events.
  * **Reliability** - The reliability pillar focuses on the **ability to prevent, and quickly recover from failures to meet business and customer demand**. Key topics include foundational elements around setup, cross project requirements, recovery planning, and how we handle change.
  * **Performance Efficiency** - The performance efficiency pillar focuses on **using IT and computing resources efficiently**. Key topics include selecting the right resource types and sizes based on workload requirements, monitoring performance, and making informed decisions to maintain efficiency as business needs evolve.
  * **Cost Optimization** - Cost Optimization focuses on **avoiding un-needed costs**. Key topics include understanding and controlling where money is being spent, selecting the most appropriate and right number of resource types, analyzing spend over time, and scaling to meet business needs without overspending.
* The **AWS Well-Architected Tool** - Define a **workload based on one of your existing cloud applications** and review the answers.
* AWS is called Amazon web services since everything can be accessed using a REST based API 


* **Identity and Access Management** - is a web service for **securely controlling access to AWS services**. With IAM, you can centrally manage users, security credentials such as access keys, and permissions that control which AWS resources users and applications can access. You use IAM to **control who is authenticated (signed in) and authorized (has permissions) to use resources**.
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

* **AWS CloudTrail** is an AWS service that helps you enable governance, compliance, and operational and risk auditing of your AWS account. Actions taken by a user, role, or an AWS service are recorded as events in CloudTrail. **Events include actions taken in the AWS Management Console, AWS Command Line Interface, and AWS SDKs and APIs.**
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
   
   
