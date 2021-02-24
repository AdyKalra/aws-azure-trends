### HSBC's PayMe for Business app
[HSBC](https://www.youtube.com/watch?v=KEYqG0IcUy8&list=PLXtHYVsvn_b_v4EKljH6dGo9qJ7JjItWL&index=26)

* 39 Mil HSBC cx's
* 1.5 Mil using PayMe app
* PayMe for Consumer
* PayMe for Business
* Cloud Native solution
* Microservices architecture - User Profile, Business Profile, Onboarding, Payment transactions, Payment reporting, security authentication, social, timeline, notification, QR code service, Optical Character Recognition, FAQ, Messages
* Transaction = Merchant -> amount on app -> QR code on merchant -> QR scanned by consumer -> details of payment -> confirmation -> payment transaction (process) -> notification service for consumer / merchant.
* Each microservice has its own -> azure key vault, azure DB for MySQL, Redis cache, Azure event hub, Azure blob storage, Azure application insights
* Scaling Out -> Payment transactions, compute and DB layer - Read replicas of MySql db (upto 500 mil transactions)
* Comms b/w microservices - Each microservice runs its own subnet and communicate with azure services like azure event hub, azure key vault, azure active directory, azure blob storage , azure db for mysql, azure cosmosdb, azure appln insights.
* Vnet service endpoint - creates secure endpoints as if they were local, yet secure
* CDN to control traffic
* Advanced threat protection built in for azure db for mysql that monitor events and sends risks
* Analytics and Data - all transactional data put in graph data model using cosmos db (used as an analytics store) + azure databricks to stich together all the interactions -> used both for data engineering workload and data science workload
* streamline data from transactional data stores, event hub , storage into Databricks -> refine the data moved to clear staging model -> connected data in SLIM(Simple Lightly Integrated Model) used by Data science (realtime)
* Transactional data not real time -> on databricks workloads
* Use managed services to reduce effort -> ideation to live faster
* Design your architecture -> isolate microservices - increase resiliency , availability

### Azure Mobile Apps 
* Monitor the health and status of your Azure resources
* Quickly diagnose and fix issues
* Run commands to manage your Azure resources
* Data is secure and encrypted
