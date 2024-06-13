## Riot Games: A New Data Ingest Pipeline 
### Summary: 
Riot Games ingests about 20 TB of data every day on AWS.  This data powers a wide range of products including match-making, personalization, analytics, security, anti-cheat and player behavior.  Until recently, this data was only queryable hours after it was produced (in some cases up to 6).  With AWS MSK, the team was able to bring that time down to 5 minutes and unlock use cases that require stream processing.  MSK also allowed us to lower our TCO and deprecate an aging, Map-Reduce based pipeline. In this session, we will talk about the before state, migration path, current state and future state of our data ingestion pipeline.

- Data ingest system for league of legends
- Players -> Game Servers Data Cemtres
- Players(Millions in 20+ Shards) -> API in EKS
  - 8 TB of data a day
  - 500 mil events / second
  -  Global outreach
-  EKS -> MSK (Managed streaming for Kafka) with a scaling pattern, acts as a regional buffer where there are five different regions, 
where data flows in, data is collected, and it's prepared for processing.
- Mirror Maker (componet of Kafka) used to replicate data out of local Kafka cluster[Data center] - into those regional MSK clusters.
- After processing spark streaming job that writes data into data lake in S3
- 
