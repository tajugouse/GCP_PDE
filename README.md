Welcome to GCP PDE Notebook!!


# Table of Contents:
---
# 1. Cloud Basics
### Cloud Computing
- Offers pay-as-you-go pricing
- Companies minimize up-front IT infrastructure costs
- is the on-demand delivery of IT resources (compute/storage/etc)
- Delivery by a cloud services platform via the internet

![image](https://github.com/user-attachments/assets/48ac9f7a-8c96-4564-99e4-3e0c0d9dbc4a)

### Cloud-computing models
- Software as a Service (SaaS)
- Infrastructure as a Service (IaaS)
- Platform as a Service (PaaS)

  
![image](https://github.com/user-attachments/assets/5351a0fe-ad5a-4040-a486-da8de1fcfd94)

----

# 2. GCP Basics

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

## Big Data Architectures
A big data architecture is designed to handle

- Ingestion
- Processing
- analysis
of too large or complex data which RDBMS are not able to manage

 

Usually workloads involved are

- Batch processing for big data sources at rest.
- Real-time processing for big data in motion.
- Interactive exploration of big data in motion or rest
- Predictive analytics and machine learning of big data.
 

Big data architectures is applied when

- traditional database unable to store and process large volumes of data
- To process and transform unstructured data for analysis and reporting.
- For unbounded streams of data, acquire, process and analysis in real time or low latency.

Components of a big data architecture

- Data sources: It is the essential component and may include
	- Application data stores or RDBMS
	- Static files given by applications like logs
	- Real-time data sources as from IoT devices.
- Data storage. Distributed file store are used to for data storage to store huge volumes in various formats. .
- Batch processing. It is applied as huge data volume for data processing jobs like filtering, aggregation, or  prepare for analysis. Steps involved are reading data, processing and writing to new files in a batch manner.
- Real-time message ingestion. For real-time data sources and involves capture and storage of messages for real-time stream processing.
	- A message ingestion store is used as a buffer and called as stream buffering.
	- Stream processing. After capture, real-time processing done like filtering, aggregation, or data preparation for analysis.
	- Output of processing foes to a output sink.
- Analytical data store. Big data requires data preparation for analysis and provide data as per analysis tool requirement. The analytical data store provides the storage and replies to the queries.
- Analysis and reporting. For providing insights by data analysis and reporting.
- Repeated data processing tasks are orchestrated as workflows and automated from data capture, transform and analysis.

## Capacity Planing
Capacity is the amount of resources needed to run service or services for fulfilling the requirement.

In computing it could be RAM capacity/ storage capacity or computing capability

Capacity planning involves planning capacity to address future and present needs and it involves steps as

Step 1 : Bottom-Up Capacity

Analyze current system capacity

Step 2 : Primary Drivers

Figure out present resource usage and their utilization.

Step 3 : Theoretical Minimum Capacity

Deduce the minimum capacity needed in present setup  or  for tasks the system is accomplishing

Step 4 : Past Predicts Future

Use past capacity changes for requirement fulfilment

Step 5 : Assumptions

Focus on assumptions for future systems and their designs. Also, include risks to be taken in  terms of  assumptions made.

Step 6 : Risks

Mitigate or accept risks as part of the capacity planning. Mitigation is done  by addressing the risk and acceptance is resolved by making suitable provisions as applicable with aim of lowest cost for resolution. At least plan for long term for resources like 3/5 years.

PLAN B

Develop a backup plan

# 3. Data Migration

## Present Environment
Present environment to be migrated, should be mapped first

It can be

- on-premises environment – Have full ownership, responsibility and control
- Private hosting environment – Like colocation facility, involves only part of infrastructure and its management being outsourced to an third party. Shared amongst customers.
- Public cloud environment – fully managed services

Table comparing each environment

	Resources			On-premises	Private hosting				Public cloud
	Physical security and safety	You		Service provider		Service provider
	Power and network cabling	You		Service provider		Service provider
	Hardware (incl. maintenance)	You		Depends on service provider	Service provider
	Virtualization platform	You	You		Service provider
	App resources			You		You				You (eventually leveraging fully managed services)


## Workload
- Understanding workloads type is essential for migration and is next after understanding the environment.
- Usually legacy workloads and operations might not be suitable for cloud environments.
- Various combinations of environment and workload types to consider during migration are
	- On-premises environment with legacy workloads and operations.
	- On-premises environment with cloud-native workloads and operations.
	- Public cloud environment with legacy workloads and operations.
	- Public cloud with cloud-native workloads and operations.

## Types of migrations
There are three major types of migrations:

Lift and shift:

- Move workloads to a target environment with little or no modifications.
- Minimum changes needed are applied to operate in target cloud environment.
- Suitable if environment and workloads are similar or little or no business need for change.
- It requires the least time and is the quickest migration
Improve and move:

- It involves changing the workloads or operation to benefit from cloud-native capability
- Improvement in performance/ features/ cost/ user experience is realized
- Suitable if a major update was to be done on the workload
Rip and replace:

- Complete redesign and development of existing workload or operation is done
- Suitable if existing is not to be maintained or change in requirements or no support in GCP

## Google Cloud Adoption Framework
- To evaluate the organizational readiness for cloud technology adoption
- It is a map for present and targeted IT capabilities
- Identify gaps and fill them

![image](https://github.com/user-attachments/assets/a075faac-6d65-4351-bac0-5f58756a52d3)

Four themes are assessed:

- The quality and scale of learning programs.
- Support to IT departments from leadership for migration
- Level of cloud-native services usage
- Level of security of present environment

For each theme, identify your phase as below

- No plans only a quick ROI and least IT disruption is required.
- A plan is present but only streamlining of operations are needed for more efficiency.
- Focused on long term goals. Improve efficiency by cloud model

## The migration Process
A migration is a journey and involves various phases with multiple options to reach destination. As per diagram

![image](https://github.com/user-attachments/assets/9ddb7cc7-c696-464d-8487-7e5d612f6017)


Professional Data Engineer Google Cloud 

There are four phases of migration:

- 	- Involves assessment and discovery of existing environment,
	- understand app and environment inventory
	- identify app dependencies and requirements
	- perform TCO and app performance benchmarks.
- 	- Create the basic cloud infrastructure for workloads
	- Make plan how to move apps.
	- Planning involves enlisting identity management, organization and project structure, networking, sorting apps, and a prioritized migration strategy.
	- Design, implement and execute migration
	- May refine cloud resources as per any need
- Optimize
	- Analyze and optimize cloud resource utilization
	- Reduce costs
	- Implement Automation, ML and AI services
#### Assess Phase
- Build an inventory of apps – Use teams for each workload in current environment.
- The inventory should include
	- apps
	- Dependencies of each app
	- Services supporting app infrastructure
	- Servers configurations
	- Network devices, firewalls, and other dedicated hardware.
- For each item gather
	- Source code location
	- Deployment method
	- Network restrictions or security requirements.
	- Licensing requirements
- Categorize apps
	- Categorize to prioritize the apps to migrate first
	- Also understand complexity and risk involved
	- A catalog matrix is used for purpose
#### Transferring large datasets

For large datasets transfer involves various steps as

- building the right team
- planning early
- testing transfer plan before implementing

#### Data transfer

- Process of moving data without transforming
- It involves
	- Making a transfer plan to decide transfer option and get approvals
	- Coordinating team that executes the transfer
	- Choosing the right transfer tool based on resources, cost, time
	- Overcoming data transfer challenges, like insufficient bandwidth, moving actively used datasets, protecting and monitoring the data during transfer and ensuring successful transfer
- Other types of data transfer projects
	- ETL transformation use Dataflow.
	- To migrate a database and related apps use Cloud Spanner
	- For virtual machine (VM) instance migration use Migrate for Compute Engine.
 

Step 1: Assembling team

Planning a transfer typically requires personnel with the following roles and responsibilities:

- Storage, IT, and network admins to execute transfer
- Data owners or governors, legal persons approval for transfer

Step 2: Collecting requirements and available resources

- Identify datasets to move.
	- Use Data Catalog to organize data into logical groupings
	- Work with teams to update these groupings.
- Identify datasets you can move.
	- Any regulatory, security, or other factors prohibit transfer
	- Remove sensitive data or reorganize data as needed. Use Dataflow or Cloud Data Fusion or Cloud Composer.
- For movable datasets decide where to transfer each dataset.
	- Select storage option to store data.
	- Understand data access policies to maintain after migration.
	- Any region or geography specific requirement
	- data structure in the destination
	- transfer on an ongoing basis or one off
- For movable datasets also enlist following
	- Time: When to transfer
	- Cost: budget available
	- People: Who will execute the transfer
	- Bandwidth (for online transfers):
	
Step 3: Evaluating transfer options

Data transfer options are selected as per following factors

- Cost
- Time
- Offline versus online transfer options
- Transfer tools and technologies
- Security
 

#### Cost:

It includes

- Networking costs
- Egress charges if any
- bandwidth charges for transfer
- Storage and operation costs for Cloud Storage during and after the transfer of data
- Personnel costs for support
 

#### Time:

- Time involved for transfer
- when to undertake transfer
- Connection options for data transfer between private data center and GCP
	- A public internet connection by using a public API
	- Direct Peering by using a public API
	- Cloud Interconnect by using a private API
	
#### Connecting with a public internet connection 

- Less predictable
- Dependent on ISP capacity
- low costs
- Google offers peering arrangements if applicable
 

#### Connecting with Direct Peering –

- Access GCP network with lesser network hops
- Direct Peering connects ISP network and Google’s Edge Points of Presence (PoPs)
- A registered Autonomous System (AS) Number need to be set up along with around-the-clock contact with network operations center.

#### Connecting with Cloud Interconnect –

- Cloud Interconnect is a direct connection to GCP by Cloud Interconnect service providers.
- No need to send data on the public internet
- more consistent throughput for large data transfers.
- SLAs for network availability and performance

#### Online versus offline transfer –

- Transfer data over a network, or by using storage hardware.
 

Deciding among Google’s transfer options

Factors to choose a transfer option


![image](https://github.com/user-attachments/assets/162554e1-46b0-42bc-b5ed-1705a40bf425)


#### gsutil

- suitable for smaller transfers of on-premises data (less than a few TB)
- include gsutil in default path if using Cloud Shell.
- By default provided with Cloud SDK.
- manages Cloud Storage instances,
- functions provided –
- copying data to and from the local file system and Cloud Storage.
- move and rename objects and
- perform real-time incremental syncs
- Use scenarios
	- transfers as-needed basis, or in command-line sessions by users.
	- If transfer few files or very large files, or both.
	- consuming output of a program like streaming output to Cloud Storage
	- if watching and syncing a directory with a fewer number of files
- For using gsutil, create a Cloud Storage bucket and copy data to it.
- For security use HTTPS
- For large datasets transfer
- use gsutil -m for multi-threaded transfers
- use Composite transfers for a single large file, it breaks large files into smaller chunks to increase transfer speed.
 

#### Storage Transfer Service

- for large transfers of on-premises data
- Designed for large-scale transfers (up to petabytes of data or billions of files).
- supports full copies or incremental copies,
- Offers graphical user interface
- Usage scenarios
	- If sufficient bandwidth available to move the data volumes
	- For large internal users who cannot use gsutil
	- need error-reporting and a record of data moved.
	- limit the impact of transfers on other workloads
	- To run recurring transfers on a schedule.
- Install agents to use Storage Transfer Service on-premises
- Agents are in Docker containers and run or orchestrate them by Kubernetes.
- After setup start transfers by providing
	- a source directory
	- destination bucket
	- time or schedule
- Storage Transfer Service recursively crawls subdirectories and files in the source directory and creates objects with a corresponding name in Cloud Storage
- Automatically re-attempts transfer if any transient errors
- You can monitor files moved and the overall transfer speed
- After transfer a tab-delimited file (TSV) file lists all files transferred and error messages
- Best Practices
	- Use an identical agent setup on every machine.
	- More agents results in more speed so deploy many agents
	- Bandwidth caps can protect other workloads
	- Plan time for reviewing errors.
	- Set up Cloud Monitoring for long-running transfers.
 

#### Transfer Appliance –

- Used for larger transfers if limited network bandwidth or costly
- Usage scenarios:
	- data at a remote location with limited / no bandwidth.
	- Required bandwidth is not available
- Involves receiving and shipping back the hardware
- It is Google-owned hardware.
- Available only in specific countries.
- Factors for choosing it are cost and speed.
- Request a appliance in the Cloud Console detailing data to transfer
- Approximate turnaround time for a appliance to be shipped, loaded with data, shipped back, and rehydrated on Google Cloud is 50 days.
- cost for the 480 TB device process is less than $3,000.
 

#### Storage Transfer Service for cloud-to-cloud transfers –

- Storage Transfer Service is a fully managed and highly scalable data transfer service
- Automates transfers from other public clouds into Cloud Storage.
- supports transfers into Cloud Storage from Amazon S3 and HTTP.
- For Amazon S3,
	- access key and an S3 bucket details are needed
	- Daily copies of any modified objects is also supported
	- Cannot transfer to Amazon S3.
- For HTTP, list of public URLs in a specified format are needed
- Script needed with size of each file in bytes, with Base64-encoded MD5 hash of the file contents.
 

#### Security

- Primary focus during transfer
- different levels of security offered by GCP
- consider protection of
- data at rest (authorization and access to the source and destination storage system),
- data in transit,
- access to the transfer product.

Security offered by product.

![image](https://github.com/user-attachments/assets/55880d88-9360-4024-a03f-527f7223fc97)



Step 4: Preparing for transfer

Steps involved are

- Pricing and ROI estimation.
- Functional testing. to confirm product set up and that network connectivity
	- Confirmation of install and operation of the transfer.
	- Enlist issues that block data movement
	- List operations needed like training needed
- Performance testing. run a transfer on a large sample of data and confirm   speed and fix bottlenecks
 

Step 5: Ensuring the integrity of transfer

- Enable versioning
- backup on destination to circumvent any accidental deletes.
- Validate data before removing the source data.
  
# Data Quality Management

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
