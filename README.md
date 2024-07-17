Welcome to GCP PDE Notebook!!


# Table of Contents:
---
# 1. Cloud Basics

- Offers pay-as-you-go pricing
- Companies minimize up-front IT infrastructure costs
- is the on-demand delivery of IT resources (compute/storage/etc)
- Delivery by a cloud services platform via the internet

![image](https://github.com/user-attachments/assets/48ac9f7a-8c96-4564-99e4-3e0c0d9dbc4a)

# Cloud-computing models
- Software as a Service (SaaS)
- Infrastructure as a Service (IaaS)
- Platform as a Service (PaaS)

  
![image](https://github.com/user-attachments/assets/5351a0fe-ad5a-4040-a486-da8de1fcfd94)

----

## GCP Basics

## GCP Services

In this, we will learn about GCP Services.

### 1. Compute
- App Engine – A PaaS for deploying Java, PHP, Node.js, Python, C#, .Net, Ruby and Go applications.
- Kubernetes Engine (GKE) or GKE on-premises offered as part of Anthos platform – Uses Kubernetes to offer Containers as a Service in GCP
- Compute Engine – IaaS to run Microsoft Windows and Linux VMs in GCP.
- Professional Data Engineer Google Cloud gcp services

  ![image](https://github.com/user-attachments/assets/792a0031-f200-4827-9e35-ac4e88bda528)

### 2. Storage & Databases
- Cloud Storage – Object storage with edge caching, to store unstructured data in GCP.
- Cloud Bigtable – A managed NoSQL database service in GCP.
- Datastore in Cloud – NoSQL database suitable for web and mobile applications requirements.
- Cloud SQL – Database as a Service based on MySQL and PostgreSQL by Google.
- Cloud Spanner – A relational database service which is horizontally scalable and consistent
### 3. Networking
- Cloud Load Balancing – Load balance traffic and is software-defined.
- VPC – VPC or Virtual Private Cloud, a private network with network resources being managed by software.
- Cloud Armor – Web application firewall protecting against DDoS and other attacks
### 4. Big Data
- BigQuery – On demand data warehouse which is scalable and fully managed for analytics.
- Cloud Composer – Workflow orchestration service using the Apache Airflow.
- Dataproc – Executes Apache Hadoop and Apache Spark jobs.
- Datalab in Cloud – Managed Jupyter Notebook service for data exploration, analysis, visualization and machine learning.
- Dataflow – A stream and batch data processing service using Apache Beam
- Cloud Pub/Sub – Scalable event ingestion service based on message queues.
- Professional Data Engineer Google Cloud 
- AutoML – Train and deploy custom machine, learning models service.
- Cloud Machine Learning Engine – Service to train and build ML models using mainstream frameworks.

![image](https://github.com/user-attachments/assets/75ee7f61-a9f1-4a86-8bfe-47cb4dde9d0c)

### 5. Management Tools
- Cloud Console – Web interface to manage GCP resources.
- Deployment Manager in Cloud- Deploys GCP resources defined as per templates in YAML, Python or Jinja2.
- Cloud Shell – Browser-based shell command-line access to manage GCP resources.
### 6. Identity & Security
- IAM – Identity and Access Management service for policies using RBAC (role-based access control).
- Cloud Identity – Single sign-on (SSO) service using SAML 2.0 and OpenID.
- Cloud Key Management Service – Encryption key management service for use with IAM and audit logging.
### 7. IoT
- Cloud IoT Core – Secure device connection and management service for IoT
- Cloud IoT Edge – Providing AI to the edge computing layer.
### 8. API Platform
- Apigee API Platform – API Lifecycle management service involving design, security, deployment, monitoring, and scaling APIs.
- API Analytics –API based programs analysis service

## Google Cloud Functions

Google Compute Engine (Virtual Machines)

Run applications as App Engine/Container Engine/ Cloud Functions.
Support for Linux and Windows VMs with Google maintained or custom machine images
 

### Networking

- Software defined management of network resources
- Unrelated subnets in a private networks which can communicate as per defined policy
- List firewall rules based on iptables style IP ranges or tags assigned to network resources.
- All network objects are global, hence any VM is able to communicate if on same private network.
 

### Storage

- Multiple storage options offered as per requirement
- Persistent Disks – block storage for VMs and has option of HDD or SSD. Disks are independent of the VM and can attach to multiple VMs simultaneously.
- Cloud storage 
	– Object store to store blobs and is stored in a bucket. Bucket is versioned, replicated and shared.
	- Offers many storage classes: regional, multi-regional, nearline, and coldline.
	- Multi-regional storage buckets are geographically redundant automatically	
	- Nearline and coldline storage buckets are for performance boost
- Database solutions
	- Relational data solution – Cloud SQL ((MySQL or Postgres instance) and Cloud Spanner.
	- NoSQL solutions offered – Datastore and Bigtable.
- Scaling and High-Availability implemented by more instances of the service (horizontal scaling), or increasing the compute/storage resources (vertical scaling )
 
### Instance Groups

- It bundles VMs for easy management and load-balancing
- Load Balancers – To detect unhealthy or absent VMs and direct customer traffic to a healthy instance without intervention.
- Auto-Scaling – Automatic scaling as per defined metric, like CPU usage / connections. It deletes VMs when workload decreases
- Automated Infrastructure – Easy software based management with REST API for provisioning, maintenance, and monitoring.
- Deployment Manager – Defines infrastructure in template files. Offers versioning and documentation.

---
# 2. Storage Models
## ER Model
- ER Model is based on – Entities, their attributes and relationships among entities.
- An entity represents real-world entity with properties called attributes like chair with size.
- Entity is represented as tables also called relations
- Columns in table represent attributes or properties
- Relations are normalized to store atomic values.
- Every row is unique and is a collection of all attributes for a entity’s instance
- Relationship refers to logical association among entities, mapping entities to each other.
- Cardinality is number of association between two entities similar to parent-child and is – one to one, one to many, many to one or many to many.

  
## NoSQL Model
In this, we will learn the concepts of NoSQL Model in GCP.

- Key Value Store – schema-less , key points to an specific item but lack of consistency
- Document Store – Similar to key value stores, documents store data in encoding (XML/JSON)
- Column Store – Data stored in columns, comprised of multiple column families which logically group specific columns. A key identify and point to a number of columns, each column store in separate file and has tuples of names-values, ordered and comma-separated.
- Graph Base – It is a directed graph structure and consists of edges and nodes. represents pack of objects, connected by links.

### GCP document-oriented database:
- Firestore is a document-oriented database that runs on top of NoSQL.
- There are no tables or rows in this database, unlike a SQL database. Data is instead stored in documents that are arranged into collections. A collection of key-value pairs may be found in each document. Firestore is designed to hold enormous amounts of tiny 

### Documents.
Collections must be used to hold all papers. Subcollections and nested objects, both of which can include simple fields like strings or complicated objects like lists, can be found in documents. In Firestore, collections and documents are formed implicitly.
Simply said, data may be assigned to a document within a collection. Firestore builds the collection or document if it does not exist.
Documents
The document is the storage unit in Firestore. A document is a simple record with fields that correspond to values. A name assign to each document.

The following is an example of a document describing a user alovelace:

	class alovelacefirst : "Ada"
	last : "Lovelace"
	born : 1815
Maps are hierarchical, complex items in a document. For example, you could use a map to organise the user’s name from the previous example:

	class alovelacename :
	first : "Ada"
	last : "Lovelace"
	born : 1815
You’ll note that the papers resemble JSON. They are, in reality, essentially the same. Although there are significant distinctions (for example, documents enable more data types and restrict to 1 MB in size), documents may treat as lightweight JSON records in general.

### Collections
nosql model example
Documents are stored in collections, which are nothing more than storage containers for documents. You might, for example, have a users collection that contains all of your different users, each of whom represents by a document:

collections_bookmark users

	class alovelacefirst : "Ada"
	last : "Lovelace"
	born : 1815

	class aturingfirst : "Alan"
	last : "Turing"
	born : 1912

### Hierarchical Data
Consider a chat app with messages and chat groups to see how hierarchical data structures function in Firestore.

You may save different chat rooms in a collection named rooms:

collections_bookmark rooms

class roomAname : "my chat room"

class roomB...

Decide how you’ll save your messages now that you’ve had chat rooms. It’s possible that you won’t want to save them in the chat room’s document. Firestore documents should be light, and a chat room might have a big amount of messages. However, as subcollections, you may construct more collections within your chat room’s document.


## Google Products and Storage Options

Various storage systems in Google cloud are discussed with their uses.

### Cloud SQL

- A fully managed relational database service
- Easily set up and manage RDBMS – PostgreSQL, MySQL, and SQL Server in GCP
- Apt to be used for WordPress, backends, CRM tools, MySQL, PostgreSQL, and Microsoft SQL Servers
 

### Cloud Spanner

- A scalable relational database service
- Full transactions support
- Provides strong consistency and high availability
- Useful for mission-critical applications
- Provides scale insurance
 

### Cloud Bigtable

- NoSQL database service from GCP
- Provides low latency reads
- Supports high throughput writes
- Enables scalability and reliability
- Suitable for large analytical workloads and low-latency applications
- Store large amount of structured objects.
- No support for SQL’s queries or multi-row transactions.
- Provision for capacity petabytes with a maximum unit size of 10 megabytes per cell and 100 megabytes per row.
 

### Cloud Memorystore

- A managed in-memory data store service for Redis
- Useful for sub-millisecond data access using Redis
- Can build application caches
- Provides scalable, secure and highly available GCP infrastructure.
 

 

### Cloud Firestore

- Managed, serverless, cloud-native NoSQL document database.
- Useful for client side mobile and web applications and gaming leaderboards
 

### Firebase Realtime Database

- A NoSQL database from GCP to store and sync data between users in real time.
- Useful for
	- creating onboarding flows
	- rolling out new features
	- building serverless apps

### BigQuery

- Serverless, highly scalable, and cost-effective data warehouse service
- Lowers data warehouse costs as all infrastructure in GCP
- Useful for
	- real-time analytics
	- advanced and predictive analytics
	- large-scale events

### Cloud Datastore

- NoSQL document database service
- Fully-managed service by GCP
- Easy scalability without configuration or downtime.
- Useful for
	- user profiles
	- product catalogues
	- mobile games.
- Useful for web and mobile applications which may require massive scale in future
- Supports storage of unstructured objects, transactions and SQL-like queries.
- Provides terabytes of capacity
- maximum unit size of one megabyte per entity.
 

### Cloud Storage

- For storing immutable blobs larger than 10 megabytes like images or movies.
- Provides huge capacity with a maximum unit size of five terabytes per object.
 

 

### Select the right GCP database service

- Existing database – GCP database service
- Redis – Cloud Memorystore for Redis
- MemcacheD – App Engine for MemcacheD
- MySQL – Cloud SQL for MySQL
- PostgreSQL – Cloud SQL for PostgreSQL
- SQL Server – Cloud SQL for SQL Server
- HBase – Cloud Bigtable
 

### Use Case

- If need full SQL support with OLTP use Cloud SQL or Cloud Spanner. Cloud SQL provides terabytes capacity and Cloud Spanner provides petabytes capacity
- For big data analysis and interactive query use BigQuery
- For semi structured application use Cloud Datastore
- For analytical data with heavy read/write events like Advertisement Tech, Financial or IoT data use Bigtable
- To store structured and unstructured, binary data like images/ multimedia files and backups, use Cloud Storage
- For popular web frameworks use Cloud SQL
- For huge database applications more than 2 terabytes use Cloud Spanner. Use cases like financial trading and e-commerce.
![image](https://github.com/user-attachments/assets/25594e72-4470-49aa-b173-24e59e9d984b)


### Evaluating Cloud Storage Options

The key considerations in evaluation of GCP data storage options, are:

- Scalability – Able to scale as per requirement
- Durability – High availability and consistency to store critical data
- Able to store unstructured/semi-structured and structured data
- Free from fixed schema
- Separation of components Able to decouple storage, compute and other components for scaling of each.
- Cost Effective – Should be cost effective and offer pay as you use model.

### Functional requirements

- Data format to be stored – data type to store like transactional data, JSON objects, telemetry, search indexes, or flat files.
- Scale and structure. Need for data partitioning and total storage capacity needed
- Data size supported – Size of entities to store and will be stored as a document, or can be split across multiple
- Data relationships. Relationship to support one to one, one-to-many or many-to-many relationships
- Consistency model. – Level of consistency needed ACID needed or  accept eventual consistency
- concurrency needed during data updation and synchronization, pessimistic or optimistic concurrency
- Schema flexibility. fixed schema or schema less needed
- Data lifecycle.
- Data movement. Level of data movement, ETL for moving data to data stores or data warehouses
 

### Non-functional requirements

- Performance and scalability. performance requirements needed for data ingestion or processing rates, acceptable response times for query
- Level of fault-tolerance needed, backup and restore capabilities
- Either distribute among multiple replicas or regions, replication capabilities needed
 

### Management and cost

- Managed service. managed service provided for easy management
- Region availability. available in all regions or selected ones
- Does data need to be  migrated
- Proprietary versus OSS usage and license
- Overall cost.
 

### Security

- encryption used, authentication mechanism needed
- audit log level of details and what can be audited
- Networking requirements. Any restriction in access to data
 

### DevOps

- Skill set. Specific programming languages, operating systems, or other technology needed
- Clients client support for development languages
- Big Data Architectures
- Capacity Planning


## Data Migration

- Present Environment
- Workload
- Types of migrations
- Google Cloud Adoption Framework
- The migration Process

## Data Quality Management

- Validate Data
- Quality metadata
- Auditing

## Data Lifecycle
- Ingest
- Store
- Process and analyze
- Explore and visualize
- Orchestration

## Schema Design
- What is Schema Design
- Relational Schema Design
- Non-relational Schema Design in Cloud Bigtable
- Table design

## Cloud SQL
- Cloud SQL Features
- Importing Data
- Exporting Data
- CloudSQL Instance settings

## Datastore
- Datastore Overview
- Data Organization
- Queries
- Indexing
- Data Consistency

## Bigtable
- Bigtable Overview
- Cloud Bigtable architecture
- Data Organization
- Load balancing
- Columns
- Supported data types
- Empty cells
- Column qualifiers
- Compactions
- Mutations and deletions
- Data compression
- Data durability
- Security
- Instance Configuration
- Storage types
- Data Management
- cbt tool
- Best Practices

## Cloud Spanner
- Cloud Spanner Overview
- Schema and data model
- Cloud Spanner Instances

## Cloud Pub/Sub
- Cloud Pub/Sub Overview
- Monitoring

## Cloud Dataflow

- Cloud Dataflow Overview
- Key Concepts
- Pipeline Design
- Pipeline Lifecycle, creation and Transform
- Cloud Dataflow templates
- Streaming Pipeline
- Best Practices

## Dataproc
- Dataproc Overview
- Configure Dataproc Cluster and Submit Job
- Migrating to Google Cloud
- Best Practices

## BigQuery
- BigQuery Overview
- Interacting with BigQuery
- Loading Data
- Exporting Data
- Optimize for Performance and Cost
- Queries
- BigQuery Logging and Monitoring
- BigQuery Best Practices

## Google Stackdriver
- Monitoring
- Logging
- Error Reporting
- Debugging
- Tracing

## Machine Learning
- What is Machine Learning?
- Inductive Learning
- Machine Learning Algorithms
- Neural Networks

## Google AI Platform (Formerly Cloud ML Engine)
- AI Platform Overview
- AI Platform Training
- AI Platform Pipelines

## Pre-trained Machine Learning API’s
- Pre-trained ML API’s
- Cloud Vision Product Search
- Vision API
- NL API

## Datalab
- Datalab Overview
- Running Datalab

## Dataprep
- Dataprep Overview

## DataStudio
- DataStudio Basics
- Steps to use the tool

## Cloud Composer
- Cloud Composer Overview

## Security and Compliance
- Google Security Culture
- Operational Security
- Technology with Security at Its Core
- Independent Third-Party Certifications
- Regulatory compliance
- General Data Protection Regulation (GDPR)
- The Health Insurance Portability and Accountability Act of 1996 (HIPAA)
- Cloud Data Loss Prevention (DLP)
- Encryption Basics
- Cloud Key Management Service

## Cloud IAM
- Access management
- Cloud IAM policy
- Cloud IAM working
