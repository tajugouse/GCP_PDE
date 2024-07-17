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
# 3. Storage Models
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

# 4. Data Migration

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
  
# 5. Data Quality Management
Processes include

- Creating validation controls
- Implement data quality monitoring and reporting
- Enabling root cause analysis
- Tracking data incidents.
- Remedy data issues.

### Validate Data
- Data processing like cleansing/enhancing/transforming can affect data quality
- Data validation checks for
- Consistency –
	- data should fit into expected values
	- field values should match the data type for the column
	- values within acceptable ranges
- Completeness –
	- expected values be included in data
No missing values

### Quality metadata
- Data quality management (DQM) is essential for metadata quality
- Put effort to discover, search, understand, and maintain metadata quality
- Data Catalog gives centralized metadata management by
	- Custom metadata tags, support data quality attributes by defining them and grouping for easy management
	- custom enumerated types to represent ordinal attributes, and double and string types
	- use the Data Catalog API for automation and in upstream processes.
### Auditing
- Audit ensures systems are working as designed
- Auditing involves
	- gathering data
	- identify discrepancy
	- act on issues raised
- perform regular audits
- May be needed for regulatory compliance
- GCP offers audit logs
- Important to audit who has the ability to change Cloud IAM policies
- Analyzing logs and answer “Who did what, where, and when?”
- For data, use Cloud Logging in two immutable log streams: Admin Activity and Data Access audit logs.
- For metadata, use Data Catalog
- Admin Activity logs has administrative actions details, changes done in configuration or metadata of resources.
- Data Access logs record user-authenticated API calls that create, modify, or read user-provided data.
- Create Cloud Monitoring alerts to trigger as per specific conditions.
- Audit logs may have sensitive information, so restrict access to the logs by using IAM roles.
- Cloud Logging keeps audit logs for log retention period only.
- Exporting logs to a BigQuery dataset

# 6. Data Lifecycle
In this, we will learn about the data lifecycle.

- GCP has many services to manage data lifecycle – acquisition to final visualization.
- The data lifecycle steps.
	- Ingest: Pull in the raw data, like streaming data from devices, on-premises batch data, app logs, or mobile-app user events and analytics.
	- Store: Store data in a durable and easy access format.
	- Process and analyze: Transformed data from raw into actionable information.
	- Explore and visualize: Convert results of analysis into a format to draw insights.
GCP services for data life cycle-

![image](https://github.com/user-attachments/assets/b4bbf1f8-1c11-40c6-92ba-4d87db1792a8)


#### Ingest
You may acquire raw data in a variety of ways, depending on the amount, source, and latency of the data.

- Data from app events, such as log files or user events, usually gathers via a push paradigm, in which the app uses an API to deliver the data to storage.
- Streaming: The data is a series of short, asynchronous messages that are in a continuous stream.
- Batch: A series of files containing a large amount of data is sent to storage in bulk.
#### Store
Data arrives in a variety of shapes and sizes, and its structure determines by the sources from which it derives. And, also the downstream use cases. Ingest data can store in a number of forms or places for data and analytics applications.

#### Process and analyze
You must convert and analyze data in order to gain business value and insights from it. This necessitates a processing architecture that can either analyze the data directly or prepare it for downstream analysis, as well as tools to assess and comprehend the outcomes of the processing.

- Processing: Data from source systems is cleansed, normalized, and processed across multiple machines, and stored in analytical systems.
- Analysis: Processed data stores in systems that allow for ad-hoc querying and exploration.
- Understanding: Depending on analytical results, data can be train and test automated machine-learning models.
#### Explore and visualize
In-depth data exploration and visualization are the final steps in the data lifecycle, and they help you better comprehend the outcomes of your processing and analysis. Insights operate improvements in the pace or amount of data input, the use of various storage mediums to expedite analysis, and upgrades to processing pipelines during exploration. Data scientists and business analysts having skills in probability, statistics, and recognizing business value, frequently explore and analyze big data sets.

### Ingest
- Capture raw data depending on the data’s size, source, and latency
- Various ingest sources
	- App: Data from app events, like log files or user events
	- Streaming: A continuous stream of small, asynchronous messages.
	- Batch: Large amounts of data in set of files to transfer to storage in bulk.
Google Cloud services map for app/streaming and batch workloads –

![image](https://github.com/user-attachments/assets/ba5c503e-5514-4bd6-adcd-37b1f8798670)


The data transfer model you choose depends on workload, and each model has different infrastructure requirements.

#### Ingesting app data
- Consists of apps and services data and includes
- app event logs
- clickstream data
- social network interactions
- e-commerce transactions
- App data helps in showing user trends and gives business insights
- GCP hosts apps from App Engine (managed platform) and Google Kubernetes Engine (GKE – container management).
- Use cases of GCP hosted apps
	- Writing data to a file: App outputs batch CSV files to the object store of Cloud Storage then to import function of BigQuery, an data warehouse, for analysis and querying.
	- Writing data to a database: App writes data to GCP database service
	- Streaming data as messages: App streams data to Pub/Sub and other app, subscribed to the messages, can transfer the data to storage or process it immediately in situations such as fraud detection.
-  Cloud Logging
	- A centralized log management service
	- Collects log data from apps running on GCP.
	- Export data collected by Cloud Logging and send the data to Cloud Storage, Pub/Sub, and BigQuery.
	- Many GCP services automatically record log data to Cloud Logging like App Engine
	- Also provide custom logging messages to stdout and stderr
	- displays data in the Logs Viewer.
	- Involves a logging agent, based on fluentd, which run on VM instances
	- Agent streams log data
#### Ingesting streaming data
- Streaming data is
	- delivered asynchronously
	- without expecting a reply
	- are small in size
- Streaming data can
	- fire event triggers
	- perform complex session analysis
	- be input for ML tasks.
- Streaming Data Use cases
	- Telemetry data: Data from network-connected Internet of Things (IoT) devices who gather data about surrounding environment by sensors.
	- User events and analytics: Mobile app logging events about app usage, crash, etc
#### Pub/Sub
- A real-time messaging service
	- sends and receives messages between apps
- A use cases is inter-app messaging to ingest streaming event data.
- Pub/Sub automatically manages
	- Sharding
	- replication
	- load-balancing
	- partitioning of the incoming data streams.
- Pub/Sub has global endpoints using GCP load balancer, with minimal latency.
- Automatic scaling to meet demand, without pre-provisioning the system resources.
- Message streams re organized as topics.
	- Streaming data target a topic
	- each message has unique identifier and timestamp.
- After data ingestion, apps can retrieve messages by using a topic subscription in a pull or push model.
	- In a push subscription, server sends a request to the subscriber app at a preconfigured URL endpoint.
	- In the pull model, the subscriber requests messages from the server and acknowledges receipt.
- Pub/Sub guarantees message delivery at least once per subscriber.
- No guarantees about the order of message delivery.
- For strict message ordering with buffering, use Dataflow for real-time processing
	- After processing, move the data into Datastore/BigQuery.
#### Ingesting bulk data
- Bulk data is
	- large datasets
	- ingestion needs high aggregate bandwidth between a small sources and the target.
- Data can be
	- files (CSV, JSON, Avro, or Parquet files) or in
	- a relational database
	- NoSQL database
- Source data can be on-premises or on other cloud platforms.
- Use cases
	- Scientific workloads
	- Migrating to the cloud
	- Backing up data or Replication
	- Importing legacy data
#### Storage Transfer Service

- Managed file transfer to a Cloud Storage bucket
- Data source can be
	- AWS S3 bucket
	- a web-accessible URL
	- another Cloud Storage bucket.
- Used for bulk transfer
- Optimized for 1 TB or more data volumes.
- Usually used for backing up data to archive storage bucket
- Supports one-time transfers or recurring transfers.
- Has advanced filters based on file creation dates/filename/times of day
- Supports the deletion of the source data after it’s been copied.
#### Transfer Appliance:
- 
- A shippable, high-capacity storage server
- It is leased from Google.
- connect it to network, load data and ship to an upload facility.
- Appliance comes in multiple sizes
- Use appliance a per cost and time feasibility for same
- Appliance deduplicates, compresses, and encrypts captured data with strong AES-256 encryption using a password and passphrase given by user. During reading of data from Cloud Storage, same password and passphrase are needed.
#### gsutil
- A command-line utility
- moves file-based data from any existing file system into Cloud Storage.
- Written in Python and runs on Linux, macOS and Windows.
- It can also
	- create and manage Cloud Storage buckets
	- edit access rights of objects
	- copy objects from Cloud Storage.
#### Database migration
- For RDBMS data, can migrate to Cloud SQL and Cloud Spanner.
- For Data warehouses data, migrate to
- For NoSQL databases migrate to Bigtable (for column-oriented NoSQL) and Datastore (for JSON-oriented NoSQL).
  
### Store
Data is of various types as

![image](https://github.com/user-attachments/assets/6babee60-9b67-47ae-9fd5-37af2fae6698)

#### Object Storage
Tools for object storage are listed.

Cloud Storage

- A managed object storage service
- Durable and highly-available storage for structured and unstructured data
- Can store
	- log files
	- database backup
	- export files
	- images
	- binary files.
- Files organized by project into individual buckets.
- Buckets can support either custom ACLs or IAM controls.
- Logging by Cloud Logging.
- Use cases
	- Data backup and disaster recovery
	- Content distribution – store and deliver media files
	- Storing ETL data
	- Storing data for MapReduce jobs
	- Storing query data
	- Seeding machine learning
	- Archiving cold data
- Multiple storage classes offered
	- Standard Storage has highest availability, low-latency access for frequently accessed data, like serving website content, interactive storage workloads, data supporting mobile and gaming apps, data-intensive computations and big data processing.
	- Nearline Storage is low-cost, highly durable storage if data is accessed once a month. Gives sub-second response times and apt for data archiving, online backup, or disaster recovery.
	- Coldline Storage is a very-low-cost, highly durable storage for one a quarter data access. Gives sub-second response times, and apt for data archiving, online backup, and disaster recovery.
	- Archive Storage is lowest-cost, highly durable storage for once a year data access. Gives fast access with sub-second response times and suitable for data archiving, online backup, and disaster recovery.
#### Cloud Storage for Firebase

- Scalable storage service for mobile app developers
- Designed to scale with user base.
- Also good for storing and retrieving assets such as images, audio, video, and other user-generated content in mobile and web apps.
- Firebase SDKs for uploads and downloads
- It stores files in a Cloud Storage bucket,
- Can do server-side processing like image filtering or video transcoding
 

#### Storing database data
Tools for databases, both RDBMS and NoSQL, are listed.

Cloud SQL

- A managed service giving MySQL and PostgreSQL engine
- built-in support for replication
- Provides low-latency, transactional and relational database workloads
- Supports standard APIs for connectivity.
- Has built-in backup and restoration, high availability, and read replicas.
- Supports RDBMS workloads up to 30 TB for both MySQL and PostgreSQL.
- Accessible from apps running on App Engine, GKE, or Compute Engine.
- Also supports standard connection drivers and app frameworks (like Django, Ruby on Rails) Data stored is encrypted in transit and at rest.
- Also has built-in support for access control, using network firewalls.
- Use cases for Cloud SQL OLTP
	- Financial transactions
	- User credentials
	- Customer orders
- Also suitable for OLAP workloads or data needing dynamic schemas on a per-object basis.
- For dynamic schemas, use Datastore and for OLAP use BigQuery and for wide-column schemas, use Bigtable. Use Dataflow or Dataproc for ETL
 

#### Bigtable

- A managed service for wide-column NoSQL
- Designed for terabyte- to petabyte-scale workloads.
- Built on Google’s internal Bigtable database infrastructure
- Provides consistent, low-latency, and high-throughput storage for large-scale NoSQL data. Supports real-time app serving and large-scale analytical workloads.
- Use a single-indexed row key associated with a series of columns
- queries are based on row key
- Schemas are structured as tall or wide
- The style of schema is dependent on the downstream use cases and it’s important to consider data locality and distribution of reads and writes to maximize performance.
- Tall schemas used for time-series events, as data is keyed by a timestamp, with relatively fewer columns per row.
- Wide schemas, a simplistic identifier as the row key along with a large number of columns.
- Use cases
	- Real-time app data
	- Stream processing
	- IoT time series data
	- Adtech workloads
	- Data ingestion
	- Analytical workloads
	- Apache HBase replacement
	- No support for multi-row transactions, SQL queries or joins.
 

#### Spanner

- A horizontally scalable relational database service
- Has strong consistency, high availability, and global scale.
- Has ease of use and familiarity of a RDBMS with the scalability of a NoSQL database.
- Spanner supports
- Schemas
- ACID transactions
- SQL queries (ANSI 2011)
- Scales horizontally in regions and can scale across regions
- Perform automatic sharding and give millisecond latencies.
- Security includes data-layer encryption, audit logging, and Cloud IAM integration.
- Use cases
	- Financial services
	- Ad tech
	- Retail and global supply chain
 

#### Firestore

- A flexible, scalable NoSQL database service
- stores JSON data
- JSON data can be synchronized in real time to connected clients
- Firestore API lets app persist data to a local disk
- Has a flexible, expression-based rules language
- Firestore Security Rules for authentication
- Use cases
	- Chat and social media
	- Mobile games
 

#### Ecosystem databases

- Can deploy own database software on Compute Engine VMs
- Traditional RDBMS supported like EnterpriseDB and Microsoft SQL Server
- NoSQL database systems like MongoDB and Cassandra
 

#### Storing data warehouse data
A data warehouse stores large quantities of data for query and analysis instead of transactional processing. For data-warehouse workloads, Google Cloud provides BigQuery.

 

#### BigQuery

- A managed data warehouse service
- Supports ingestion by web interface, command line tools, and REST API calls.
- Bulk loading in CSV, JSON, or Avro files.
- For streaming data, use Pub/Sub and Dataflow
- Can also stream data directly into BigQuery
  
### Process and analyze
- Processing and transformation is needed
- The processing framework can analyze data directly or prepare the data for downstream analysis
- Steps usually involved
- Processing: Data from source is cleansed, normalized, and processed
- Analysis: Processed data is stored for querying and exploration.
- Understanding: Based on analytical results, data is used to train and test automated machine-learning models.

#### Processing large-scale data
- Large-scale data processing with data source from Cloud Storage, Bigtable, or Cloud SQL
- For large to fit data frameworks manage distributed compute clusters
#### Dataproc

- A managed Apache Hadoop and Apache Spark service
- Hadoop and Spark are popular and supported by Dataproc
- No infrastructure needed to run Hadoop or Spark jobs in Dataproc
- Migrate Hadoop or Spark deployments to Dataproc
- Dataproc automates cluster creation, simplifies configuration and management of cluster
- Has built-in monitoring and utilization reports
- Use cases.
	- Log processing
	- Reporting
	- On-demand Spark clusters
	- Machine learning
- Simplifies operational activities like installing software or resizing a cluster.
- Also access, read data and write results in Cloud Storage, Bigtable, or BigQuery, or HDFS Can store and checkpoint data externally
 

#### Dataflow

- A serverless, fully managed batch and stream processing service
- Designed to simplify big data for both streaming and batch workloads.
- No need to specify a cluster size and manage capacity,
- Dataflow has on-demand resources are created, autoscaled, and parallelized.
- A true zero-ops service
- straggler workers addressed by constant monitoring, identifying, and rescheduling work, including splits, to idle workers across the cluster.
- Use-cases.
	- MapReduce replacement
	- User analytics
	- Data science
	- ETL
	- Log processing
- The Dataflow SDK released as Apache Beam
- Supports execution on Apache Spark and Apache Flink.
 

#### Dataprep by Trifacta

- A visual data exploration, cleaning, and processing service
- A service for visually exploring, cleaning, and preparing data for analysis.
- Use Dataprep by a browser based-UI, without coding.
- Automatically deploys and manages the resources required.
- Transform data in CSV, JSON, or relational-table formats.
- It uses Dataflow to scale automatically and can handle terabyte-scale datasets.
- Can export clean data to BigQuery
- Manage user access and data security with Cloud IAM
- Use cases
	- Machine Learning: You can clean training data for fine-tuning ML models.
	- Analytics: You can transform raw data so that it can be ingested into data warehousing tools such as BigQuery.
 


#### BigQuery

- A managed data warehouse service
- Supports ad-hoc SQL queries and complex schemas.
- Use standard SQL queries or BI and visualization tools
- It is a highly-scalable, highly-distributed, low-cost analytics OLAP data warehouse
- Can have a scan rate of over 1 TB/sec.
- To start, create a dataset in project, load data into a table, and execute a query.
- Data loading from Pub/Sub, Dataflow, Cloud Storage, or output from Dataflow or Dataproc. Can also import CSV, Avro and JSON data formats
- Supports nested and repeated items in JSON.
- All data accessed (at rest or in motion) are encrypted.
- Covered under Google’s compliance programs
- Access to data controlled by ACLs.
- Billing based on: queries and storage.
- Querying data under pricing models: on-demand or flat-rate.
	- on-demand pricing – charges as per terabytes processed.
	- flat-rate pricing – consistent query capacity with a simpler cost model.
- BigQuery automates infrastructure maintenance windows and data vacuuming.
- query plan explanation is used in design of queries
- Data stored in a columnar format, optimized for large-scale aggregations and data processing.
- Built-in support for time-series partitioning of data.
- Run queries by standard SQL, with support for querying nested and repeated data.
- built-in functions and operators also provided.
- Use cases
	- User analysis
	- Device and operational metrics
	- Business intelligence
 

#### Understanding data with machine learning
- Machine learning is now crucial in analysis phase of the data lifecycle.
- Used to augment processed results
- suggest data-collection optimizations
- predict outcomes in data sets.
- Use cases.
	- Product recommendations
	- Prediction
	- Automated assistants
	- Sentiment analysis
- ML Options
	- Task-specific machine learning APIs
	- Custom machine learning
	
##### The Vision API

- Used to analyze and understand the content of an image
- Uses pre-trained neural networks.
- Can classify images, detect individual objects and faces, and recognize printed words.
- Can detect inappropriate content.
- API is accessible through REST endpoints.
- Send images directly or upload to Cloud Storage and send link to image in the request. Requests can have single or multiple images
- Feature annotations can be selected
- Feature detection includes labels, text, faces, landmarks, logos, safe search, and image properties (like dominant colors).
- Response has metadata about each feature type annotation selected for each supplied in the original request.
- Integrate with other GCP services
 

##### Speech-to-Text

- Used to analyze audio and convert it to text.
- Recognizes more than 80 languages and variants
- Powered by deep-learning neural-network algorithms which constantly evolve and improve.
- Use cases
	- Real-time speech-to-text
	- Batch analysis
 

##### Natural Language API

- Used to analyze and reveal the structure and meaning of text.
- Can extract information about people, places, events, sentiment of the input text, etc.
- Results used to filter inappropriate content, classify content by topics, or build relationships
- Combine with the Vision API for OCR capabilities or the Speech-to-Text features
- API is available through REST endpoints.
- Send text directly to the service, or upload to Cloud Storage and send text file link in request.
 

##### Cloud Translation

- To translate more than 90 different languages.
- It automatically detects the input language, with high accuracy.
- Provide real-time translation for web and mobile apps
- supports batched requests for analytical workloads.
- Available through REST endpoints.
- Integrate the API with GCP services
 

##### Video Intelligence API: Video search and discover

- Used to search, discover, and extract metadata from videos.
- Has an easy-to-use REST API
- Can detect entities (nouns) in video content
- Also look for entities in scenes in the video content.
- Can annotate videos with frame-level and video-level metadata.
- Supports common video formats, like MOV, MPEG4, MP4, and AVI.
- Create a JSON request file with the location of the video and annotation types to perform, and submit to the API endpoint.
- Use cases
	- Extract insights from videos
	- Video catalog search
 

AI Platform

- A managed machine learning platform
- Used to run custom machine learning models at scale.
- Create models using the TensorFlow framework, and use AI Platform to manage preprocessing, training, and prediction.
- It is integrated with Dataflow for data pre-processing
- Can access data stored in Cloud Storage or BigQuery.
- Also works with Cloud Load Balancing
- Develop and test TensorFlow models
- Uses Datalab and Jupyter notebooks
- Models are completely portable.
- AI Platform workflow
	- Preprocessing: Involves training, evaluation, and test data
	- Graph building: convert supplied TensorFlow model into an AI Platform model with operations for training, evaluation, and prediction.
	- Training: Continuously iterates and evaluates the model according to submitted parameters.
	- Prediction: Use the model to perform computations in batches or on-demand


##### General-purpose machine learning

- Can deploy other high-scale ML tools like Mahout and MLlib
- Offers ML algorithms for clustering, classification, collaborative filtering, and more.
- Use Dataproc to deploy managed Hadoop and Spark clusters,
- Run and scale ML workloads

### Explore and visualize
- Involves data exploration and visualization
- to better understand the results of the processing and analysis.
- Insights gained to drive improvements
- Apply statistical methods and ML
 

##### Datalab

- An interactive web-based tool
- Used to explore, analyze and visualize data.
- Built on Jupyter notebooks earlier called IPython.
- Launch an interactive web-based notebook to write and execute Python programs to process and visualize data.
- The notebooks maintain their state and can be shared.
- Support popular data-science toolkits, like pandas, numpy, and scikit-learn
- Supports visualization packages, like matplotlib.
- Supports Tensorflow and Dataflow.
- Can load and cleanse data, build and verify models, and then visualize the results
 

##### Data science ecosystem

- Deploy data science tools on GCP
- Can deploy RStudio Server or Microsoft Machine Learning Server on a Compute Engine instance.
- Deploy Jupyter or JupyterHub on Compute Engine instances.
- Apache Zeppelin also supported
 

##### Visualizing business intelligence results

- Number of reporting and dashboarding tools in GCP
- Google Data Studio is a drag-and-drop report builder
- The charts and graphs in the reports can be shared and updated.
- Reports can contain interactive controls.
- Access data from data files, Google Sheets, Cloud SQL, and BigQuery.
- Visualize data in a spreadsheet, in Google Sheets
  
### Orchestration
- Incorporating all of the elements of the data lifecycle into a set of connected and cohesive operations requires some form of orchestration. Orchestration layers are typically used to
- It coordinate
	- starting tasks
	- stopping tasks
	- copying files
	- providing a dashboard to monitor data processing jobs.
- Orchestration workflows can be simple or complex
- Supports open-source orchestration tools like Luigi and Airflow
- For custom orchestration apps, create an App Engine app.
  
# 7. Schema Design
### What is Schema Design
A database schema is

- skeleton structure
- represents the logical view of the entire database.
- Also called as a metadata
- Describes the relationships between objects and information in a database.
  
### Relational Schema Design
Before delving into designing a schema, lets look at the properties that makes a good Database .

ACID properties

- Atomic : Transaction is a single unit, either succeeds or fails completely.
- Consistent : DB is consistent before and after the transaction.
- Isolated : reading and writing to multiple tables at the same time.
- Durability : once transaction is committed, will remain committed even in a system failure.
 

For a good Relational DB schema, following are important

- Relationship between entities
- Normalisation Form
##### Relationship Types
###### One to One –

- one record is associated with one and only one record in another table.
- Both tables have same Primary Key to identify the record.
- Get complete data from both the tables by a join on this primary key .
 

###### One to Many –

- Each record in first Table have many linked records in second Table, second table rows have only one corresponding record in first Table.
- For data, put the primary key of first table as foreign key of the second table
###### Many To Many

- Multiple records in a table are linked to multiple records of another table.
- It is usually not allowed in RDBMS
 

##### Normalization
It reduces redundancy from a relation or set of relations in DB .

- 1 NF — There has to be a key that uniquely identifies a record/ row
- 2 NF — should be in 1 NF and every non-key column should be fully dependent on the primary key
- 3 NF — it should be in 2-NF and Non key columns are independent of each other
  
### Non-relational Schema Design in Cloud Bigtable
In this, we will learn the basics of Non-relational Schema Design in Cloud Bigtable.

The following concepts are crucial:
- Each table has only one index, the row key.
- There are no secondary indices.
- Rows are sorted lexicographically by row key, from the lowest to the highest byte string.
- Row keys are sorted in big-endian byte order.
- Column group by column family and sort in lexicographic order within the column family.
- All operations are atomic at the row level.
	- Avoid schema design that require atomicity across rows.
	- Keep all information for an entity in a single row. Can split the entity across multiple rows.
- Reads and writes should distribute evenly across the row space of the table.
- Store related entities in adjacent rows, for efficient reads.
- Cloud Bigtable tables are sparse.
- Empty columns don’t take up any space.
- It’s better to have a few large tables than many small tables. .
##### Size limits
- Size limits on data to store within tables.
- Store a maximum of 10 MB in a single cell and 100 MB in a single row.
- Size limits are in binary megabytes (MB) or 220 bytes also called a mebibyte (MiB).
##### Choosing a row key
- Think carefully about composing row key.
- Efficient queries use the row key, a row key prefix, or a row range to retrieve the data.
- Other types of queries trigger a full table scan, which is much less efficient.
- Factors for selection
	- User information needed
	- User-generated content
	- Time series data requirements
##### Types of row keys
- Keep row keys reasonably short.
- Long row keys take up additional memory and storage and increase time to get responses
- Reverse domain names – If storing data about entities can be represented as domain names, use a reverse domain name (for example, company.product) as the row key. Effective if each row’s data tends to overlap with adjacent rows. Apt if data is spread across many different reverse domain names.
- String identifiers – If identification by a string, use the string identifier as row key. Use human-readable values.
- Timestamps – Useful if need to retrieve data based on the time when it was recorded. It is not recommended
- Multiple values in a single row key – Useful to include multiple identifiers in row key.
- Row key prefixes
	- It is the first value in a multi-value row key
	- Related data in contiguous rows enables access as a range of rows against inefficient table scans.
	- Provide a scalable solution for a “multi-tenancy” use case,
- Row keys to avoid
	- Domain names
	- Sequential numeric IDs
	- Frequently updated identifiers
	- Hashed values
- Column families
	- Cloud Bigtable can use up to about 100 column families
	- A row with multiple values which are related to one another, group into same column family. Column families enables retrieving from the family instead from each row.
	- The names of column families should be short as included in each request.
- Column qualifiers
	- Can create as many column qualifiers as per need in each row.
	- No space penalty for empty cells in a row.
	- Avoid splitting data across more column qualifiers than necessary
	- keep the names of column qualifiers short, as used in each request.
 
### Table design
- Cloud Bigtable has a limit of 1,000 tables per instance.
- Better to store all data in one big table.
- Assign a unique row key prefix to use for each data set
- Avoid small tables as
	- Sending requests to many different tables increases connection overhead
	- Multiple tables of different sizes disrupt load balancing
 
# 8. Cloud SQL
- A fully-managed database service
- Easy to set up, maintain, manage, and administer relational databases on GCP
- CloudSQL automates backups, replication, encryption patches and capacity increases.
- Connect from App Engine,/Compute Engine/GKE/ workstation.
- Use BigQuery for analytics
- Enable automatic failover for highly available database
- Data is automatically encrypted
- It is SSAE 16, ISO 27001, and PCI DSS v3.0 compliant
- Supports HIPAA compliance.
- Instance size is tied to network throughput
- Disk throughput and iops are tied to size of disk
- SSL access to sql instance is supported
- Instance access control is different from project access control and uses whitelisting
- Use with MySQL, PostgreSQL, or SQL Server.
  
### Cloud SQL Features
##### Common Features

- Create and manage instances in the Google Cloud Console in US, EU, Asia or Australia.
- Cloud SQL instances run on top of managed Compute Engine VMs whose type affects performance
- Customer data encrypted on Google’s internal networks and in database tables, temporary files, and backups.
- Access by
	- direct connection, needs whitelisting
	- proxy, whitelisting not needed
	- private access
- Support for secure external connections with the Cloud SQL Proxy or with the SSL/TLS protocol.
- Read replica can only be in same region
- Cloud SQL data is stored within the same region that the instance is hosted in.
- For data availability, backups are stored in two separate regions
- Binary logging needed for point in time restore, failover replication
- Data replication between multiple zones with automatic failover.
- Automated and on-demand backups, and point-in-time recovery.
- Instance cloning.
- Connections to Cloud SQL can be established either by using traditional IP whitelisting or by the Cloud SQL Proxy
- With Cloud SQL Proxy clients can connect to Cloud SQL instances over an encrypted TCP tunnel, without needing authorized networks /SSL certificates,
 

##### MySQL Features

- Fully managed MySQL Community Edition databases in the cloud.
- Second Generation instances support MySQL 5.6 or 5.7, and provide up to 416 GB of RAM and 30 TB of data storage, with the option to automatically increase the storage size as needed.
- First Generation instances support MySQL 5.5 or 5.6, and provide up to 16 GB of RAM and 500 GB of data storage.
- Support for private IP (private services access).
- Import and export databases using mysqldump, or import and export CSV files.
- Support for MySQL wire protocol and standard MySQL connectors.
- Does not supports
	- LOAD DATA INFILE
	- SELECT … INTO OUTFILE / DUMPFILE
	- INSTALL / UNINSTALL PLUGIN
	- CREATE FUNCTION … SONAME …
	- CREATE TABLE … SELECT statements
	- CREATE TEMPORARY TABLE statements inside transactions
	- Transactions or statements that update both transactional and nontransactional tables
	- LOAD_FILE() function
	- client program features – mysqlimport, mysqldump
 

##### PostgreSQL Features

- Fully managed PostgreSQL databases in the cloud, based on the Cloud SQL Second Generation platform.
- Custom machine types with up to 416 GB of RAM and 64 CPUs.
- Up to 30 TB of storage available, with automatic storage size increase
- Support for PostgreSQL client-server protocol and standard PostgreSQL connectors.
- Support for multiple PostgreSQL versions.
- Not supported
	- Point-in-time recovery (PITR)
	- Import/export in CSV format using Cloud Console or the gcloud command-line tool.
	- Low-Level Virtual Machine (LLVM) Just-in-Time (JIT) compilation
	- Logical replication
##### SQL Server Features

- Fully managed SQL Server databases in the cloud.
- Custom machine types with up to 416 GB of RAM and 64 CPUs.
- Up to 30 TB of storage available, with automatic storage size increase
- Import databases using native BAK and SQL files.
- Export databases using native BAK files.
- SQL Server Agent enabled to facilitate replication and other jobs.
- Not supported
	- SSRS, SSAS, SSIS, MSDTC, Data Quality Services
	- AD Authentication
	- SP_Configure settings
	- BULK INSERT and OPENROWSET(BULK…) features
	- Resource Governor, SQL Server Audit, Server-level triggers
### Importing Data
In this, we will learn the concept of importing data.

- To import data from Cloud Storage, the instance’s service account must have the legacyBucketReader Cloud IAM role set in the project.
- Import as SQL dump file or CSV for MySQL and PostgreSQL and for SQL Server option of BAK file is present
- Importing the SQL dump file / BAK file or CSV file to CloudSQL from console, as REST or use gcloud
- Import can be done by sql dump or csv.
- Sql dump cannot contain triggers, views, stored procedures.
##### Importing SQL dump files to Cloud SQL
- Do not use a system user (such as root@localhost) as the DEFINER for triggers, view, or stored procedures. You won’t have access to this user in Cloud SQL.
- The database you are importing into must already exist on Cloud SQL instance and it must be empty. You can’t overwrite existing data.
- The SQL Mode setting affects how Cloud SQL interprets SQL queries.
- Create a Cloud Storage bucket and upload the file to the bucket.
- Select the instance in the Cloud SQL Instances page in the Google Cloud Console.
- Click Import in the button bar.
- Enter the path to the bucket and SQL dump file
- For Format, select SQL.
- Select the database you want the data to be imported into.
 

##### Using gcloud Steps

- Create a Cloud Storage bucket, if you haven’t already.
- Upload the file to bucket.
- Describe the instance you are importing to: gcloud sql instances describe [INSTANCE_NAME]
- Copy the serviceAccountEmailAddress field.
- Use gsutil IAM to grant the legacyBucketWriter and objectViewer Cloud IAM roles to the service account for the bucket.
- Import the database: gcloud sql import sql [INSTANCE_NAME] gs://[BUCKET_NAME]/[IMPORT_FILE_NAME] \
- –database=[DATABASE_NAME]
- 
- If the command returns an error like `ERROR_RDBMS`, review the permissions; this error is often due to permissions issues.
### Exporting Data
- Export data from Cloud SQL to Cloud Storage and then, can download data from Cloud Storage to local environment.
- Can export to a CSV file / SQL dump file for MySQL / PostgreSQL.
- For SQL Server, export to BAK is supported
- Export can be done using console / gcloud / REST methods
 

Best practices when importing and exporting data:

- Don’t use Requester Pays buckets
- Use the correct flags when you create a SQL dump file
- Compress data to reduce cost
- Use InnoDB for MySQL

### CloudSQL Instance settings
Instance ID

- The instance ID is the name of the instance.
- Uniquely identify instance within the project.
- Instance name be aligned with the purpose of the instance when possible.
- The total length of project-ID:instance-ID must be 98 characters or less.
- You do not need to include the project ID in the instance name. This is done automatically where appropriate (for example, in the log files).
- You cannot reuse an instance name for up to a week after you have deleted the instance.
 

Storage capacity

- is the capacity to fit database size.
- After instance creation, storage capacity can be increased but cannot be decreased.
- Small capacity without enabling automatic storage increase can result in instance loosing its SLA.
 

Automatic storage increase

- If enabled, available storage is checked every 30 seconds and if available storage is below threshold size, additional storage capacity is added.
- Capacity added till it reaches the maximum of 30 TB.
- storage size can be increased but cannot be decreased till the life of the instance.
- If an instance runs out of available space, it can cause the instance to go offline, and is not covered by SLA
- This setting of a master instance automatically applies to any read replicas of that instance.
- This settings cannot be independently set for read replicas.
 

Threshold

- It’s size depends on the amount of storage currently provisioned for instance
- It cannot be larger than 25 GB.
- instances provisioned with 500 GB of storage (or more), the threshold is always 25 GB.
- For instances provisioned with less than 500 GB of storage, to find the threshold the formula is –  5 + (provisioned storage)/25 The result of the division is rounded down to the nearest whole 
- Automatic storage increase limit
- If enabled, it provides a specific limit on how large the storage for instance can automatically grow.
- Cannot be decreased
- Setting this limit to zero, the default value, means that there is no limit
- This setting for a master instance automatically applies to any read replicas of that instance.
- Auto backups
- To configure automated backups and binary logging
 

Other settings –

- Region (The Google Cloud Platform region where instance is located.)
- Zone (The GCP zone where instance is located.)
- Machine Type (or Tier, determines memory, virtual cores, and other resources available to Cloud SQL instance.)
- Database version
- Storage type ( Choosing SSD, the default value, for lower latency and higher data throughput else select HDD.)
- Private IP (Configures instance to use private IP)
- Public IP (If enabled, instance is allocated a public IPv4 address. When you disable Public IP, that address is released)
  
# 9. Datastore
- A highly-scalable NoSQL database for web and mobile applications.
  
### Datastore Overview
- A NoSQL database.
- Firestore is the newest version of Datastore
- NoSQL Database
- They are non-relational
- easy to scale (horizontally or vertically) better than relational databases
- Are either schema-free or have relaxed schemas
- No definition of the schema of the data needed
- Distributed in nature
- Have auto-scaling and fail-over capabilities
- May not comply with ACID requirement
- Types
	- Key-value – simplest, data item stored as an attribute name (or “key”) together with its value.
	- Wide-column – store data together as columns instead of rows and are optimized for queries over large datasets.
	- Document databases – pair each key with a complex data structure known as a document. Documents can contain many different key-value pairs, or key-array pairs, or even nested documents.
	- Graph databases – store information about networks, such as social connections.
- Hierarchies or entity groups: – set of entities connected through ancestry to a common root element.
- Join operation is not supported, we need to denormalize table
- Aggregation and “group by” are not supported
- Inequality filters are limited to at most one property
- Do not support substring matches, case-insensitive matches, or so-called full-text search.
- The NOT, OR, and != operators are not natively supported
  
### Data Organization
- Records, called “entities” in Datastore, are retrieved by using a key.
- The key is a complex data structure that can be used to model relationships.
- The simplest key has a string kind value and either a numeric id value or a string name value.
- Multiple records can be found that match criteria
- Datastore entities of the same kind can have different properties
- Entity – single object (like row or document)
- Kind – category of object (Like table name)
- Property – individual data for an object(like column)
- Key – unique ID for each entity
- Different entities can have properties with the same name but different value types.
- All queries are served by previously built indexes,
- Datastore is schemaless.
- Has limited support for queries and transactions
- Does not support join, inequality filtering on multiple properties or aggregation operations
- Datastore is apt for
- applications that rely on highly available structured data at scale.
- Product catalogs for real-time inventory and product details for a retailer.
- User profiles giving a customized experience based on the user’s past activities and preferences.
- Transactions based on ACID properties, for example, transferring funds from one bank account to another.
### Queries
- A query retrieves entities that meet a specified set of conditions.
- The query operates on entities of a given kind
- Can specify filters on the entities’ property values, keys, and ancestors, and can return zero or more entities as results.
- sort orders can also be specified to sequence the results by their property values.
- query can return entire entities, projected entities, or just entity keys.
- Every query computes its results using one or more indexes
- When executed, the query retrieves all entities of the given kind satisfying given filters, sorted in specified order.
- Queries execute as read-only.
 

A typical query includes the following:

- An entity kind to which the query applies
- Zero or more filters based on the entities’ property values, keys, and ancestors
- Zero or more sort orders to sequence the results
 
### Indexing
An index is

- defined on a list of properties of a given entity kind,
- a order (ascending or descending) for each property is also defined
- Indexes – Created on every category which is not null
- Secondary and composite indexes – done using multiple fields
- by default, 1 index per column is created,
- restrictions with combining multiple columns.
- To use multiple columns as indexes, we need to create composite indexes.
- Creating composite index:
- Create index.yaml:
- Create index:
- gcloud datastore create-indexes index.yaml
 

An index table

- contains a column for every property named in the index’s definition.
- Each row represents an entity with a potential result for queries based on the index.

### Data Consistency
Selecting Specific Application

- For a relational database with full SQL support for an online transaction processing (OLTP) system, consider Cloud SQL.
- If data is not highly structured or no need for ACID transactions Cloud Bigtable is apt.
- For interactive querying in an OLAP system, BigQuery is suitable.
- For storing large immutable blobs, like large images or movies, Cloud Storage is suitable.
- Strong consistency – entity groups (this will slow down writes to 1 per second), regular read and write
- Eventual consistency – global entities, indexes
  
# 10. Bigtable
A wide-column NoSQL database
### Bigtable Overview
- Cloud Bigtable is a sparsely populated table
- Can scale to billions of rows and thousands of columns,
- Can store terabytes or even petabytes of data.
- A single value in each row is indexed called the row key.
- Good to store very large amounts of single-keyed data with very low latency.
- Supports high read and write throughput at low latency
- Ideal data source for MapReduce
- Supports client libraries, like  Apache HBase library for Java.
- Has Incredible scalability
- similar to hbase, cassandra, dynamodb.
- indexed by row key, column key, and timestamp
- Data can be streamed into bigtable
- No joins, transactions supported only within a single row
- Append only operation, no transactional.
- Cluster resizing without downtime
- Use cases
	- non-structured key/value data, but each value is no larger than 10 MB.
	- storage engine for batch MapReduce
	- stream processing/analytics
	- machine-learning applications
- Store and query following data
	- Time-series data
	- Marketing data like purchase histories
	- Financial data, like transaction histories
	- Internet of Things data, like usage reports
	- Graph data
### Cloud Bigtable architecture
- Data is stored as a sorted map structure.
- Data is indexed at the column level as a group of
	- row key
	- a column key
	- and a timestamp
- The index is the key mapping to the column’s actual value.
- Timestamp is for versioning.
- Data operations are conducted on a per-row basis so, all columns of a row are updated simultaneously.
- Automatic data compression is also done as applicable.
- Bigtable cluster may only operate within a single zone.
- For higher availability, configure with two separate clusters, each in a different zone of the same region.

Cloud Bigtable Architecture:

![image](https://github.com/user-attachments/assets/ece3ff1b-d81a-42dd-aa35-3b00a5ec3c21)


- Client requests go through a front-end server
- Nodes are organized into a Cloud Bigtable cluster of a Cloud Bigtable instance
- Each node in the cluster handles a subset of the requests to the cluster.
- Add nodes to increase the number of simultaneous requests to handle and maximum throughput
- Table is sharded into blocks of contiguous rows, called tablets similar to HBase regions. Tablets are stored on Colossus, Google’s file system, in SSTable format.
- An SSTable is a ordered immutable map from keys to values, and both are byte strings.
- Tablet is associated with a specific node.
- Writes are stored in Colossus’s shared log as acknowledged
- Data is never stored in nodes themselves;
- Node have pointers to a set of tablets stored on Colossus.
- Rebalancing tablets from one node to another is very fast
- Recovery from the failure of a node is very fast
- When a Cloud Bigtable node fails, no data is lost.
  
### Data Organization
- Every row in Bigtable is indexed by a single row key.
- Row keys are byte strings that may be up to 64 KB
- Row keys enables to retrieve several related rows quickly as a single, contiguous scan over the row key.
- Each row may contain thousands of columns
- Bigtable only scans the row key when performing lookups.
- Reads and writes are performed at the row level.
- Data is stored in scalable tables, each of which is a sorted key/value map.
- Each row describes a single entity,
- Columns contain individual values for each row.
- Each row is indexed by a single row key
- Columns if related are grouped into a column family.
- Column is identified by column family and a column qualifier.
- Each row/column intersection can contain multiple cells, or versions, at different timestamps
- Tables are sparse; if a cell does not contain any data, it does not take up any space.
For example, suppose you’re building a social network for United States presidents—let’s call it Prezzy. Each president can follow posts from other presidents. The following illustration shows a Cloud Bigtable table that tracks who each president is following on Prezzy:

![image](https://github.com/user-attachments/assets/2ffc06b6-149f-446e-9971-e660b4e429d4)

In above figure,

- The table has single column family – “follows” having many column qualifiers.
- Above, uses column qualifiers as data as Bigtable handles sparseness and will be able to add new ones quickly.
- Row key is username and assuming they are evenly spread, it gives quick access and update
### Load balancing
- Cloud Bigtable zone is managed by a master process
- The process balances workload and data volume within clusters.
- The master
	- splits busier/larger tablets in half
	- merges less-accessed/smaller tablets together and redistributes between nodes
	- In spike of traffic, master splits tablet in two and moves new tablets to another node.
- For write performance distribute writes as evenly as possible across nodes.
- Useful to group related rows for efficient read of several rows at same time.
  
### Columns
- They are stored as unstructured byte arrays
- For performance, column values be under 10 MB, with a combined size of 100 MB for all columns in a row.
- Best to keep all data about a entity in a single, flattened, potentially very wide row.
- Column families are defined at the table level and subsets of columns can be read.
- Best to group columns into families based on access patterns
  
### Supported data types
- It treats all data as raw byte strings
  
 ### Empty cells
 - Empty cells do not take any space
- the key/value entry is simply absent.
### Column qualifiers
- They take up space in a row
- It is efficient to use column qualifiers as data.
### Compactions
- Compaction or removal of deleted entries takes place automatically.
  
### Mutations and deletions
- Mutations, or changes, to a row take up extra storage space a it is done sequentially and - compaction is done only periodically.
- During compaction, values no longer needed are removed.
- During update in a cell, both the original and new value are stored till compacted.
- Deletions also take up extra storage space, until compaction
### Data compression
- Automatic compaction
- Cannot configure compression settings for table.
- Random data cannot be compressed
### Data durability
- Data is stored on Colossus, Google’s internal, highly durable file system
- HDFS cluster is not needed
- If using replication, one copy of data is in Colossus for each cluster in the instance.
- Each copy is located in a different zone or region
- Google uses proprietary storage methods to achieve data durability
### Security
- Access controlled by Google Cloud project and the Cloud IAM roles
- can manage security at the project, instance, and table levels.
- No support for row-level, column-level, or cell-level security restrictions.
### Instance Configuration
- Instance is a container for data.
- Instances have one or more clusters
- located in different zones.
- Each cluster has at least 1 node.
- An instance has properties –
	- The storage type (SSD or HDD)
	- The application profiles, which use replication
### Storage types
- Two types – solid-state drives (SSD) or hard disk drives (HDD).
- SSD storage is the most efficient and cost-effective choice for most use cases.
- HDD storage is sometimes appropriate for very large data sets (>10 TB) that are not latency-sensitive or are infrequently accessed.
- HDD use cases
- store at least 10 TB of data.
- not to be used for user-facing or latency-sensitive application.
- workload is Batch workloads or Data archival

###### Application profiles
- 
- Application profiles, or app profiles for instances using replication,
- app profiles control how applications connect to the instance’s clusters.
- Without replication, app profiles provide separate identifiers for each of applications
###### Clusters

- A cluster is a service in a specific location.
- Cluster belongs to a single instance
- An instance can have up to 4 clusters
- application requests are handled by one of the clusters in the instance.
- cluster is located in a single zone.
- An instance’s clusters must each be in unique zones.
- can create more cluster in any zone if Bigtable is available.
- instances with only 1 cluster do not use replication.
 

###### Nodes

- Each cluster in an instance has 1 or more nodes
- Nodes are compute resources to manage data.
- Bigtable splits all data from tables into smaller tablets.
- Tablets are stored on disk, separate from the nodes but in the same zone as the nodes.
- A tablet is associated with a single node.
- Each node
	- Keep track of specific tablets on disk.
	- Handle incoming reads and writes for its tablets.
	- Perform maintenance tasks on its tablets

Instance Creation Steps
- 
- Select or create a GCP project.
	- A project name must be between 4 and 30 characters.
	- A project ID is suggested which can be edited and is 6 to 30 characters, with a lowercase letter as the first character and last character cannot be a hyphen.
- Make sure billing is enabled for Google Cloud project.
- Enable the Cloud Bigtable and Cloud Bigtable Admin APIs.

Labels –

- a key-value pair
- helps you organize GCP resources
- Can attach a label to each resource
- filter the resources based on their labels.

###### Modifying Instance

- By default, can provision maximum thirty Cloud Bigtable nodes/zone in each Google Cloud project.
- For more use the node request form.
- After creating a Bigtable instance, can update following settings
	- number of nodes in each cluster
	- number of clusters in the instance
	- application profiles for the instance
	- labels for the instance
	- display name for the instance
###### Adding and deleting clusters

- can add clusters to an existing instance,
- a maximum of 4 clusters per instance can be present
- Clusters can be in any region if Bigtable is available
 

###### Deleting a cluster

- Can delete all but 1 of the clusters is needed
- Deleting all but 1 cluster automatically disables replication.
 

###### Monitoring

- monitor Bigtable instance using Cloud Console and Cloud Monitoring
- A high-level overview is given
- Key Visualizer tool gives drill down
### Data Management
- Bigtable supports a number of methods for interacting with data, as
	- HTTP API
	- the gRPC API
	- the cbt command-line tool
	- client libraries
	- an HBase client (Google HBase Java client library or the HBase shell)

Dataflow templates export data from Bigtable as
- 
- Avro files
- Parquet files
- SequenceFiles

###### Migrating the data from an Apache HBase cluster to a Cloud Bigtable cluster –

- Export the data as a series of Hadoop sequence files.
- Collect details from HBase.
- Export HBase tables to sequence files.
- Move the sequence files to Cloud Storage.
- Import the sequence files into Bigtable using Dataflow.
- Validate the move.
### cbt tool

In this, we will learn about the cbt tool of Google Professional Data Engineer GCP.

- A command-line interface
- perform operations on Bigtable.
- written in Go
- install the cbt tool as a Cloud SDK component or by using the standard go tool.
Usage:

		 cbt [-<option> <option-argument>] <command> <required-argument> [optional-argument]

The commands are:

		count – Count rows in a table
		createinstanceCreate an instance with an initial cluster
		createcluster – Create a cluster in the configured instance
		createfamily – Create a column family
		createtable – Create a table
		updatecluster – Update a cluster in the configured instance
		deleteinstanceDelete an instance
		deletecluster – Delete a cluster from the configured instance
		deletecolumn – Delete all cells in a column
		deletefamily – Delete a column family
		deleterow – Delete a row
		deleteallrows – Delete all rows
		deletetable – Delete a table
		doc – Print godoc-suitable documentation for cbt
		help – Print help text
		listinstances – List instances in a project
		listclusters – List clusters in an instance
		lookup -Read from a single row
		ls -List tables and column families
		mddoc – Print documentation for cbt in Markdown format
		read – Read rows
		set – Set value of a cell (write)
		setgcpolicy – Set the garbage-collection policy (age, versions) for a column family
		waitforreplicationBlock until all the completed writes have been replicated to all the clusters
		version – Print the current cbt version
		createappprofile Create app profile for an instance
		getappprofile – Read app profile for an instance
		listappprofileLists app profile for an instance
		updateappprofile Update app profile for an instance
		deleteappprofile Delete app profile for an instance
 

The options are:

-project string : project ID. If unset uses gcloud configured project
-instance string :Cloud Bigtable instance
-creds string: Path to the credentials file. If set, uses the application credentials in this file
### Best Practices
- Use Wide tables for dense data.
- Use Narrow tables for sparse data.
- Dont put sequential ids as key. Salting of ids can be used.
- Change schema to minimize data skew
- choose the right number of nodes
- use SSD
- Use key visualizer gives bigtable usage performance
- Row key needs to be chosen carefully so that contiguous rows are returned for queries. Row keys should also prevent hotspotting while writing.
- Spread load across multiple nodes(prevent hotspotting)

# 11. Cloud Spanner
A globally consistent, horizontally scalable database with full ACID compliance.

### Cloud Spanner Overview
- A fully managed service
- relational database service
- offers transactional consistency at global scale
- automatic synchronous replication for high availability
- Has interleaved schema – Group primary key and foreign keys together for faster access
- Cascade on delete can be done with interleave.
- Primary keys don’t have sequential keys and make sure its distributed
- Secondary indexes make the query efficient
 

CAP Theorem

The CAP theorem is for distributed system and they can guarantee at most two qualities only:

- Consistency: All observers see the most recent data and order of events is guaranteed
- Availability: The system is always online and able to handle all requests
- Partition tolerance: The system continues to operate during network disruptions
 

- RDBMS can best provide CP
- NoSQL can provide AP
- Spanner provides all three – CAP.
 

Comparison with other data models

				Cloud_Spanner	Traditional Relational	Traditional Non-Relational
	Schema			Yes				Yes						No
	SQL				Yes				Yes						No
	Consistency		Strong			Strong					Eventual
	Availability	High			Failover				High
	Scalability		Horizontal		Vertical				Horizontal
	Replication		Automatic		Configurable				Configurable
 

 

TrueTime

- Used For strong consistency
- Google datacenters have atomic clocks
- It gives Spanner nodes to determine the current time down to a very fine resolution. the margin of error in system time is about 7 ms.
 

Paxos consensus algorithm

- Allows consensus to be reached in very unreliable environments
- ideal for maintaining consensus across large bodies of data.
 

Read / Write

- queries are performed using strong reads that guarantee the most recent results
- queries may result in a slight performance hit.
- Clients can specify an exact staleness in queries
- the client provides a timestamp and Spanner executes the query on the most recent data relative to that timestamp.
- Spanner APIs provide write operation
- For write give a number of mutations to be executed,
- each mutation affects a single cell
- Spanner supports up to 20,000 mutations in a single transaction, and affected indexes are also counted.
- Cloud Spanner offers two types of transaction
- read-only transactions – non-locking operations and it ensures that the data being read is not updated from the observer’s point of view over the course of one or many reads. Any update during a read-only transaction are ignored
- read-write transactions – locking operations so, data will be blocked until the transaction is committed. It supports rollbacks.

### Schema and data model
- Can contain one or more tables
- Tables look like relational database tables
- Table structured with rows, columns, and values
- table have primary keys.
- Data is strongly typed
- must define a schema for each database and specify the data types of each column.
- Allowable data types include scalar and array types
- Avoid hot spotting like bigtable
- Use nested tables with primary keys called interleaving for faster access.
- Do not use sequential numbers, timestamps.
- If needed, store timestamps in descending order.
 

###### Parent-child table relationships

- Two ways to define parent-child relationships – table interleaving and foreign keys.
- Table interleaving is good if child table’s primary key includes the parent table’s primary key columns.
- Foreign keys
	- are not limited to primary key columns
	- tables can have multiple foreign key relationships
 

###### Primary keys

- Every table must have a primary key
- primary key can be composed of zero or more columns of that table.
- For child, the primary key column(s) of the parent table must be the prefix of the primary key of the child table.
- Spanner stores rows in sorted order by primary key values
- child rows also inserted between parent rows that share the same primary key prefix.
- Spanner can physically co-locate rows of related tables.

###### Choosing a primary key

- primary key uniquely identifies each row in a table.
- Options for primary key
	- Hash the key and store it in a column.
	- Use a Universally Unique Identifier (UUID).
	- Bit-reverse sequential values.
 

###### Database splits

- can define hierarchies of parent-child relationships between tables up to seven layers deep
- Spanner divides data into chunks called “splits”
- individual splits can move independently from each other and assigned to different servers
- A split is a range of rows in a top-level (in other words, non-interleaved) table, where the rows are ordered by primary key.
- The start and end keys of this range are called “split boundaries”.
- Spanner automatically adds and removes split boundaries
 

###### Key columns

- The keys of a table can’t change
- can’t add a key column to an existing table
- cannot remove a key column from an existing table.
 

###### Storing NULLs

- Primary key columns can be defined to store NULLs.
- to store NULLs in a primary key column, omit the NOT NULL clause
 

###### Disallowed types

These cannot be of type ARRAY:

- A table’s key columns.
- An index’s key columns.
###### Replication

- Spanner automatically gets replication at the byte level
- Spanner writes database mutations to files in this filesystem
- Spanner creates replicas of each database split
- 3 types of replicas: read-write replicas, read-only replicas, and witness replicas.
- Single-region instances use only read-write replicas,
- multi-region instance configurations use a combination of all three types
For multi-region

		Replica type	Can vote	Can become leader	Can serve reads
		Read-write		yes			yes					yes
		Read-only		no			no					yes
		Witness			yes			no					no
 


 

###### Schema Design Best Practices
- Design a schema that prevents hotspots and other performance issues.
- Place compute resources for write-heavy workloads within or close to the default leader region for optimal write latency
- Use staleness of at least 15 seconds for optimal read performance outside of the default leader region
- place critical compute resources in at least two regions to avoid single-region dependency
- keep high priority total CPU utilization under 45% in each region.
  
### Cloud Spanner Instances
- To use Cloud Spanner, first create a Cloud Spanner instance within Google Cloud project.
- instance allocates resources used by Cloud Spanner
- Instance creation includes instance configuration and the node count
- An instance configuration defines the geographic placement and replication of the databases in that instance.
- node count is the number of nodes to allocate to that instance.
- Each node provides up to 2 TB of storage.
- After instance creation, can add or remove nodes to the instance later.
- cannot remove nodes if
- If store more than 2 TB of data per node.
- Spanner has created a large number of splits for instance’s data
- To change nodes, use
	- Cloud Consol
	- the gcloud command-line tool
	- the client libraries
###### Nodes versus replicas

- To scale up the serving and storage resources in instance, add more nodes to that instance.
- Adding a node does not increase the number of replicas but increases the resources
- total number of servers in a Cloud Spanner instance is the number of nodes the instance has multiplied by the number of replicas in the instance.
###### Data Management

- To create, alter, and delete tables and indexes is done by using the default Database editor
- Use Cloud Console for inserting, editing, and deleting data.
- run DML statements using client libraries, the Google Cloud Console, and the gcloud command-line tool.
- execute DML statements inside read-write transactions.
- During data read, shared read locks is acquired on limited portions of the row ranges to read.
- During write using DML statements, exclusive locks is acquired
- Cloud Spanner sequentially executes all the SQL statements (SELECT, INSERT, UPDATE, and DELETE) within a transaction and not concurrently except multiple SELECT statements
- transaction with DML statements has the same limits as any other transaction.
- Use Partitioned DML for large-scale changes
- If transaction result in more than 20,000 mutations, a BadUsage error is given
- If a transaction result larger than 100 MB, a BadUsage error is given
- Partitioned DML is designed for bulk updates and deletes, particularly periodic cleanup and backfilling.
###### Query

- DQL statements is used to query
- A query execution plan is the set of steps for how the results are obtained.
- can retrieve a query plan using the Cloud Console, the client libraries, and the gcloud command-line tool.

###### Query Best Practices

- Use query parameters to speed up frequently executed queries
- Use secondary indexes to speed up common queries
- Avoid large reads inside read-write transactions
- Use ORDER BY to ensure the ordering of SQL results
- Use STARTS_WITH instead of LIKE to speed up parameterized SQL queries

# 12. Cloud Pub/Sub
 centralized storage and compute clusters.
- Centralized ownership
- Scalability bottlenecks
- Controlling network experience
- Business integration hiccups
- Streaming Data is Very Complex – continuously generate by an array of sources and devices in a wide variety of formats.

### Cloud Pub/Sub Overview
- use Pub/Sub as messaging-oriented middleware
- use as event ingestion and delivery for streaming analytics pipelines.
- offers durable message storage and real-time message delivery
- gives high availability and consistent performance at scale.
- It is a publish/subscribe (Pub/Sub) service
- senders of messages are decoupled from the receivers of messages
- Main terms
- Message: the data that moves through the service.
- Topic: a named entity that represents a feed of messages.
- Subscription: a named entity that represents an interest in receiving messages on a particular topic.
- Publisher (also called a producer): creates messages and sends (publishes) them to the messaging service on a specified topic.
- Subscriber (also called a consumer): receives messages on a specified subscription.
- publisher creates and sends messages to a topic.
- Subscriber applications create a subscription to a topic to receive messages from it.
- Communication can be
	- one-to-many (fan-out)
	- many-to-one (fan-in),
	- many-to-many.
 The flow of messages through Pub/Sub is as

![image](https://github.com/user-attachments/assets/8947de2b-3f81-4da3-8a95-1c907cd4ed2d)


In above figure

- There are two publishers publishing messages on a single topic.
- 2 subscriptions to the topic
- The first subscription has two subscribers, so messages will be load-balanced across them
- each subscriber receiving a subset of the messages
- The second subscription has one subscriber that will receive all of the messages.
- The bold letters are messages.
- Message A comes from Publisher 1 and sent to Subscriber 2 via Subscription 1, and to Subscriber 3 via Subscription 2.
- Message B comes from Publisher 2 and is sent to Subscriber 1 via Subscription 1 and to Subscriber 3 via Subscription 2.
###### Publisher and subscriber endpoints

- Publishers should make HTTPS requests to pubsub.googleapis.com
- It can be
	- an App Engine app
	- a web service hosted on Google Compute Engine
	- other third-party network, an app installed on a desktop or mobile device, or even a browser.
   
	![image](https://github.com/user-attachments/assets/43f1d955-09ba-4184-a005-307ce9018864)

	- Pull subscribers make HTTPS requests to pubsub.googleapis.com.
	- Push subscribers must be Webhook endpoints that can accept POST requests over HTTPS.
###### Common use cases

- Balancing workloads in network clusters.
- Implementing asynchronous workflows.
- Distributing event notifications.
- Refreshing distributed caches.
- Logging to multiple systems.
- Data streaming from various processes or devices.
###### Architecture

- Publisher and subscriber clients are not aware of the location of the servers to which they connect or how those services route the data.
- load balancing direct publisher traffic to the nearest GCP data center
- individual message is stored in a single region.
- topic may have messages stored in many regions.
- When a subscriber client requests messages published to this topic, it connects to the nearest server
- Pub/Sub is divided into two primary parts:
	- the data plane managing moving messages between publishers and subscribers,
	- the control plane, managing assignment of publishers and subscribers to servers on the data plane.
- data plane servers are called forwarders
- control plane servers are called routers
- publishers and subscribers are connected to their assigned forwarders
- so easily upgrade the control plane of Pub/Sub without affecting any clients
- All message is a base64-encoded message body and an arbitrary set of key-value pairs called attributes.
- There is no structure or context to the message so, JSON or XML entities must be enforced. Each message has a globally unique message ID, to identify if it has already been processed.
- Messages may be up to 10 MB in total size
- Two methods for message delivery: push subscriptions and pull subscriptions
	- In a push subscription, server sends a request to the subscriber app at a preconfigured URL endpoint.
	- In the pull model, the subscriber requests messages from the server and acknowledges receipt.
- Push subscriptions have a limits of 10,000 messages per second and 10,000 concurrent message deliveries.
- By default, subscriptions are created with an ack deadline of 10 seconds and the message deadline may be increased to up to 600 seconds.
- By default, subscriptions expire after 31 days of inactivity
- Using subscription expiration policies, can configure the inactivity duration
###### Topic and Message Management

- can create, delete, and view topics using
	- the API
	- the Google Cloud Console
	- the gcloud command-line tool
- must create a subscription to a topic before subscribers can receive messages published to the topic.
- create subscriptions with
	- the API
	- the Google Cloud Console
	- the gcloud command-line tool
 

###### Resource Name
 
- Resource name uniquely identifies a Pub/Sub resource
- Resource can be a subscription or topic
- must fit the following format: projects/project-identifier/collection/relative-name
- The project-identifier must be the project ID, available from the Google Cloud Console. For example, projects/myproject/topics/mytopic.
- The collection must be one of subscriptions or topics.
- The relative-name must:
	- Not begin with the string goog.
	- Start with a letter
	- Contain between 3 and 255 characters
	- Contain only the following characters:
	- Letters: [A-Za-z]
	- Numbers: [0-9]
	- Dashes: –
	- Underscores: _
	- Periods: .
	- Tildes: ~
	- Plus signs: +
	- Percent signs: %
 

###### Message Storage Security

- If publish messages to a global endpoint, automatic storage in the nearest Google Cloud region.
- topic message storage policy ensure all data published to a topic is persisted in a specific region or set of regions, regardless of the publish request’s origin.
- When multiple regions are allowed by the policy, Pub/Sub chooses the nearest allowed region.
	- To configure all of the topics in an organization-wide scope, use the Resource Location Restriction organization policy.
	- For fine-grained control, configure a topic’s message storage policy at topic creation, or via the UpdateTopic operation.
- You can configure the policy using the:
	- Topic details view
	- gcloud command-line tool
	- Service API (using client libraries)
###### Authentication and Access

- Following authentication methods allowed
	- Service accounts
	- User accounts – You can authenticate users directly to application, when the application needs to access resources on behalf of an end user.
- Uses Cloud IAM for access control
- access control can be configured at the project level and at the individual resource level.
### Monitoring
- The Pub/Sub API exports metrics via Cloud Monitoring.
- Cloud Monitoring can create monitoring dashboards and alerting policies or access the metrics programmatically.
###### Metrics –

- You can use these metrics to:
- Understand how data is distributed across the world.
- Optimize publisher and subscriber deployment location, based on that data.
- Counts of unacknowledged stored messages: subscription/num_unacked_messages_by_region
- Volume of stored data: subscription/unacked_bytes_by_region
- Age of oldest message: subscription/oldest_unacked_message_age_by_region
- For backlog : subscription/num_undelivered_messages and subscription/oldest_unacked_message_age
- Keeping publishers healthy monitor topic/send_request_count, grouped by response_code.
  
# 12. Cloud Dataflow
- It is a managed service
- executes data processing patterns.
- Uses Apache Beam SDK
- Can develop both batch and streaming pipelines.
###### Pipeline
- It manage data similar to a factory line
- Tasks include
	- Transforming data
	- Aggregating data and computing
	- Enriching data.
	- Moving data.
- Data Pipeline views all data as streaming
- It breaks dataflows into smaller units
- Tasks are written in Java or Python using beam sdk
- Jobs are executed in parallel
- Same code is used for streaming and batch
- Pipeline is a directed graph of steps
- Source/Sink can be filesystem, gcs, bigquery, pub/sub
- Runner can be local laptop, dataflow(in cloud)
- Output data written can be sharded or unsharded.
- Input and outputs are pcollection. Pcollection is not in-memory and can be unbounded.
- Each transform – give a name
- Read from source, write to sink
- Common tasks to do
- Convert incoming data to a common format.
- Prepare data for analysis and visualization.
- Migrate between databases.
- Share data processing logic across web apps, batch jobs, and APIs.
- Power data ingestion and integration tools.
- Consume large XML, CSV, and fixed-width files.
- Replace batch jobs with real-time data.
- pipeline components
- Data Nodes – for input data
- Activities – work definition to do
- Preconditions
- Resources
- Actions – An action that is triggered if conditions are met
-  
- 
###### Types

Types of pipelines are
 
	- useful for large volumes of data at a regular interval
	- no real-time processing needed
- Real-time
	- to process data in real time.
	- processing data from a streaming source
- Cloud native
	- optimized to work with cloud-based data, such as data from AWS buckets.
	- tools are hosted in the cloud
### Cloud Dataflow Overview

Google Cloud Dataflow is

- a managed data transformation service,
- has a unified data processing model to process both unbounded and bounded datasets.
- a serverless platform
- write code in the form of pipelines, and submit to CloudDataflow for execution.
- offers autoscaling workers and dynamically rebalancing workloads across those workers
- provides the open Apache Beam programming model as a managed service for
- process data in multiple ways as
	- batch operations
	- extract-transform-load (ETL) patterns
	- continuous, streaming computation.
- pipelines operate on data in terms of collections, using the abstract PCollection .
	- Each PCollection is a distributed set of homogeneous data as in the pipeline
	- can represent bounded data (CSV file in Cloud Storage) or unbounded data source, such (Cloud Pub/Sub topic).
	- PCollection is immutable.
	- each element in PCollection has an associated timestamp either from data’s source, or explicitly defined.


### Key Concepts
###### Pipelines

- encapsulates the all processes in reading input data, transforming that data, and writing output data.
- The input source and output sink can be the same or of different types
- Apache Beam programs start by constructing a Pipeline object
- then using that object as the basis for creating the pipeline’s datasets.
- Each pipeline represents a single, repeatable job.
###### PCollection

- It represents a distributed, multi-element dataset
- acts as the pipeline’s data.
- Apache Beam transforms use PCollection objects as inputs and outputs for each step in pipeline.
- A PCollection can hold a dataset of a fixed size or an unbounded dataset from a continuously updating data source.
###### Transforms

- Represent a processing operation that transforms data.
- takes one or more PCollections as input, performs an specified operation and produces one or more PCollections as output.
- can perform many kind of processing operation

###### ParDo
- 
- It is the core parallel processing operation in the Apache Beam SDKs,
- It invokes a user-specified function on each of the elements of the input PCollection.
- ParDo collects the zero or more output elements into an output PCollection.
- The ParDo transform processes elements independently and possibly in parallel.
###### Pipeline I/O

- let you read data into pipeline and write output data from pipeline.
- consists of a source and a sink.
- can also write a custom I/O connector.
###### Aggregation

- process of computing some value from multiple input elements.

###### Side input
 
- Can be static like constant
- Can also be a list or map. If side input is a pcollection, we first convert to list or map and pass that as side input.
- Call parDo.withsideInputs with the map or list

###### Mapreduce
 
- Map – operates in parallel, reduce – aggregates based on key
- parDo acts on one item at a time, similar to map operation in mapreduce, should not have state/history. Useful for filtering, mapping.
- In python, map done using map for 1:1, flatmap for non 1:1. In Java, done using parDo
###### User-defined functions (UDFs)
 
- Apache Beam allow executing user-defined code to configure the transform.
- For ParDo, user-defined code specifies the operation to apply to every element,
- UDFs can be written in a different language than the language of runner.
###### Runner
- 
- the software that accepts a pipeline and executes it.
- runners are translators or adapters to massively parallel big-data processing systems.
###### Event time
 
- The time a data event occurs,
- determined by the timestamp on the data element itself.
###### Windowing

- enables grouping operations over unbounded collections
- divides the collection into windows of finite collections
###### Watermarks

- Apache Beam tracks a watermark, all data in a certain window to have arrived in the pipeline.

###### Trigger

- Triggers determine when to emit aggregated results as data arrives.
- For bounded data, results are emitted after all of the input has been processed.
- For unbounded data, results are emitted when the watermark passes the end of the window

### Pipeline Design
When designing Beam pipeline, consider a few basic questions:

- Where is input data stored? How many sets of input data do you have?
- What does data look like? It might be plaintext, formatted log files, or rows in a database table.
- What do you want to do with data? The core transforms in the Beam SDKs are general purpose.
- What does output data look like, and where should it go?
- Transforms do not consume PCollections
### Pipeline Lifecycle, creation and Transform
###### Pipelien Creation

To construct a pipeline using the Beam SDKs

- Create a Pipeline object.
- Use a Read or Create transform to create one or more PCollections for pipeline data.
- Apply transforms to each PCollection.
- Write or otherwise output the final, transformed PCollections.
- Run the pipeline.
- Pipeline execution is separate from Apache Beam program’s execution; and is executed by a pipeline runner.
- can specify the pipeline runner and other execution options
###### Transforms

- Element-wise transforms operate on individual elements within PCollection .
- Similar to MapReduce.
- execute transformations by invoking a ParDo operation
### Cloud Dataflow templates
- Dataflow templates enables staging of pipelines on Cloud Storage
- run them from a variety of environments. You can use one of the Google-provided templates or create own.
- Templates benefits as:
- Running pipeline does not require you to recompile code every time.
- can run pipelines without the development environment and dependencies
- Runtime parameters can customize the execution of the pipeline.
- Non-technical users can run templates with the Google Cloud Console, gcloud command-line tool, or the REST API.
- runtime parameters accept values only during pipeline execution.
### Streaming Pipeline
In this, we will learn the concepts of Streaming Pipeline for Google Professional Data Engineer GCP exam.

###### Streaming pipelines
In streaming pipelines, unbounded PCollections, or unbounded collections, represent data. Data from a continually changing data source, such as Pub/Sub, is stored in an unbounded collection. In an unlimited collection, you can’t just use a key to organize elements. Because the data source is continually adding new components, there might be an endless number of elements for a particular key in streaming data. To aggregate elements in unbounded collections, you can utilize windows, watermarks, and triggers. Bounded PCollections that represent data in batch pipelines are also considered windows.

###### Windows and windowing functions
Unbounded collections are divided into logical components, or windows, using windowing techniques. Windowing functions use the timestamps of individual elements to organize unbounded collections. There are a limited amount of items in each window.

With the Apache Beam SDK or Dataflow SQL streaming extensions, you may specify the following windows:

- Tumbling windows (called fixed windows in Apache Beam): In the data stream, a tumbling window represents a consistent, discontinuous temporal span.
- Hopping windows (called sliding windows in Apache Beam): In the data stream, a hopping window indicates a continuous time interval. Tumbling windows are discontinuous, whereas hopping windows might overlap.
- Sessions Windows: A session window is made up of items that are separated by a time gap. A data stream’s gap duration is the time between new data. Data is allocated to a new window if it comes after the gap time.
###### Watermarks
A watermark is a threshold that tells Dataflow when all of the data in a window is expected to arrive. The data is considered late if it comes with a timestamp that is inside the timeframe but older than the watermark.

Watermarks are tracked by Dataflow for the following reasons:

- Data does not always come in the same sequence or at consistent intervals.
- The order in which data events are created does not ensure that they will appear in pipelines in the same order in which they were generated.
###### Triggers
As data enters, triggers determine when to emit aggregated findings. By default, when the watermark reaches the edge of the window, the results are emitted. Create or edit triggers for each collection in a streaming pipeline using the Apache Beam SDK. Dataflow SQL does not allow you to create triggers. The Apache Beam SDK allows you to create triggers based on any combination of the following criteria:

- The timestamp on each data piece indicates the event time.
- Processing time refers to the amount of time it takes for a data element to be processed at each stage of the pipeline.
- A collection’s number of data components.
### Best Practices
- Using composable transforms having business logic creates pipelines to easily maintain, troubleshoot and develop with.
- Ensure they have a clear owner
- Have a clear way to understand and document how changes to those transforms will affect all pipelines that use them.
- Always use the name field to assign a useful, at-a-glance name to the transform.
- Ensure that all transforms have versions and that all pipelines also have versions.
- Ensure you have a consistent policy to deal with errors and issues across all of transforms.
- End-to-end data pipeline testing should include lifecycle testing, particularly analyzing and testing all the different update/drain/cancel options.
- In addition to the standard metrics, build custom metrics into pipeline as per
- Create backups of pipelines
- Create multiple replica pipelines
# 13. Dataproc
- A open source data and analytics processing service
- Offers Resizable clusters
- Gives Autoscaling clusters
- Cloud integrated with GCP
- Provides Versioning
- Is Highly available
- Has automatic or manual configuration option
- Provides developer tools
- Optional components to install and configure additional components on the cluster.
- Store Custom images
- Dataproc allows specifying custom machine types
- standard mode has 1 master, multiple workers
- HA mode has 3 masters, multiple workers
- Provides Component Gateway and notebook access
- Has workflow templates
### Dataproc Overview

- A managed Spark and Hadoop service
- Use for batch processing, querying, streaming, and machine learning.
- automation helps you
	- create clusters quickly
	- manage them easily
	- save money by turning clusters off when you don’t need them.
- Use cases –
	- Move Hadoop and Spark clusters to the cloud
	- Data science on Dataproc
- Apache Hadoop ecosystem components are automatically installed on the cluster.
- initialization actions provide faster cluster startup times
- clusters can be provisioned with a custom image
- Dataproc manages preemptible node addition and deletion
	- Atleast single regular worker is needed.
	- Workers can be preemptible.
	- preemptible worker nodes will not have hdfs storage,
	- preemptible has same config as regular worker nodes.
- Web ports used tcp port 8088 which is Hadoop, 9870 which is HDFS and 8080 which is Datalab
- access Dataproc from
- Through the REST API
- Using the Cloud SDK
- Using the Dataproc UI
- Through the Cloud Client Libraries

### Configure Dataproc Cluster and Submit Job
Configuration terms

Cluster Region:

- specify a global region or a specific region for cluster.
- The global region is a special multi-region endpoint to deploy instances into any user-specified Compute Engine zone.
- can also specify distinct regions
 

Compute Engine Virtual Machine instances (VMs)

- consist of master and worker VMs,
- require full internal IP networking access to each other.
- Default network available to create a cluster helps ensure this access.

Labels –

- apply user labels to cluster and job resources
- to group resources and related operations for later filtering and listing.
- associate labels when resource is created, at cluster creation or job submission.
- label is propagated to operations performed on the resource
 

Cluster Update / Delete

- can update a cluster by Dataproc API, gcloud, or from Configuration tab of Cluster details page for the cluster in the Google Cloud Console.
- Following can be updated
	- the number of standard worker nodes in a cluster
	- the number of secondary worker nodes in a cluster
	- whether to use graceful decommissioning to control shutting down a worker after its jobs are completed
	- adding or deleting cluster labels
Deleting a cluster –

- delete a cluster by
	- Dataproc API
	- gcloud
	- Google Cloud Console.
Submit a job

- Submit a job to an existing cluster by Dataproc API, gcloud or Google Cloud Console
- can also SSH into the master instance in cluster, and then run a job
Log and Monitor

- job and cluster logs can be viewed, searched, filtered, and archived in Cloud Logging.
  
### Migrating to Google Cloud
two migration models to transferring HDFS data

##### push

simplest model
the source cluster runs the distcp jobs on its data nodes and pushes files directly to Cloud Storage.

![image](https://github.com/user-attachments/assets/bc8a80dc-8a70-4c5a-87ad-95939af18b87)

##### Pull

is complex
An ephemeral Dataproc cluster runs the distcp jobs on its data nodes,
pulls files from the source cluster, and copies them to Cloud Storage.

![image](https://github.com/user-attachments/assets/a35af540-b7d9-4107-93e8-e53407e737b4)


### Best Practices
- Specify cluster image versions.
- Know when to use custom images.
- Use the Jobs API for submissions.
- Control the location of initialization actions.
- Keep an eye on Dataproc release notes.
- Know how to investigate failures.
- Use Google Cloud Storage as primary data source and sink
- Persist information on how to build clusters
- Identify a source control mechanism
- Externalize the Hive metastore database with Cloud SQL
- Use cloud authentication and authorization policies
- Knows way around Stackdriver
- Transform YARN queues into workflow templates
- Start small and enable autoscaling
- Consolidate job history across multiple clusters
- Take advantage of GCP services
  
# 14. BigQuery
A serverless, highly scalable, and cost-effective cloud data warehouse
- analyze gigabytes to petabytes of data using ANSI SQL
- Efficiently run analytics at scale
### BigQuery Overview
- fully managed, petabyte scale, low cost analytics data warehouse.
- It is NoOps—no infrastructure to manage
- Functions to be done on BigQuery
	- Loading and exporting data
	- Querying and viewing data
	- Managing data
- Access by
	- The BigQuery web UI in the Cloud Console
	- The BigQuery classic web UI
	- The BigQuery command-line tool
	- The BigQuery REST API or client libraries
##### Cost Control

For cost control costs

- Estimate cost of a query before execution
- Estimate storage costs
- Set custom cost controls using custom quotas
- Analyze audit logs to monitor query costs and BigQuery usage
 

##### Access Control

- Access control by Cloud Identity and Access Management
- For access to BigQuery resource, assign roles to a user, group, or service account.
- If roles given at organization and project level, then can run BigQuery jobs or manage all of a project’s BigQuery resources.
- Roles at the dataset level provide access only to one or more datasets.
- Datasets are child resources of projects.
- Tables and views are child resources of datasets —inherit permissions from their parent dataset.
- It automatically encrypts all data before it is written to disk.
- Also automatically decrypted when read by an authorized user.
- By default, Google manages the key encryption keys used to protect data.
- Option to use customer-managed encryption keys
### Interacting with BigQuery
##### Web UI in the Cloud Console
- graphical web UI in the Cloud Console
- to create and manage BigQuery resources
- to run SQL queries.
- has three main sections: navigation panel for viewing, details panel for more details and query editor to make queries
##### BigQuery classic web UI
classic web UI can do tasks like
- running queries
- loading data
- exporting data.
 

##### bq command-line tool
- A python-based, command-line tool
- supports two kinds of flags — global flags and command flags.
Flags to be used as

		> bq –global_flag argument bq_command –command-specific_flag argument

- Global flags (or common flags) can be used in all commands.
- Command-specific flags apply to a specific command.
 

Separate multiple global or command-specific flags using a space. For example:

		bq \
		
		–global_flag argument \
		
		–global_flag argument \
		
		bq_command \
		
		–command-specific_flag argument \
		
		–command-specific_flag argument
		
 

Specify command arguments as

- –flag=argument
- –flag=’argument’
- –flag=”argument”
- –flag argument
- –flag ‘argument’
- –flag “argument”
 

For single or double quotes around arguments –

		> bq query –nouse_legacy_sql \‘SELECT COUNT(*) FROM `bigquery-public-data`.samples.shakespeare’
### Loading Data
- load data from
	- From Cloud Storage
	- From other Google services
	- From a readable data source
- By inserting individual records using streaming inserts
- Using DML statements to perform bulk inserts
- Using a BigQuery I/O transform in a Dataflow pipeline to write data to BigQuery
- can load data into a new table or partition
- can also append data to an existing table or partition
- can overwrite a table or partition.
- method for ingesting data into BigQuery:
	- the BigQuery Jobs API
	- streaming writes
	- writing query results into a table
	- loading CSV files from Cloud Storage
	- using BigQuery as a Cloud Dataflow sink
- The default source format for loading data is CSV.
- Also supports streaming inserts by BigQuery API and BigQuery buffers records before insertion.
 

Load data from Cloud Storage and readable data sources in the following formats:

Cloud Storage:

- Avro
- CSV
- JSON (newline delimited only)
- ORC
- Parquet
- Datastore exports
- Firestore exports
Readable data source (such as local machine):

- Avro
- CSV
- JSON (newline delimited only)
- ORC
- Parquet
 

Choosing a data ingestion format

- can load data into variety of formats.
- Loaded data is converted into columnar format for Capacitor (BigQuery’s storage format).
- During loading select data ingestion format based on
	- data’s schema
	- Embedded newlines
	- External limitations

Loading encoded data

- BigQuery supports UTF-8 encoding
- for both nested or repeated and flat data.
- ISO-8859-1 encoding for flat data only for CSV files.
- By default, the BigQuery service expects all source data to be UTF-8 encoded.

Loading compressed and uncompressed data

- The Avro binary format is the preferred for loading both compressed and uncompressed data.

Loading denormalized, nested, and repeated data

- BigQuery performs best when data is denormalized.
 

Schema auto-detection

- available when you load data into BigQuery
- Also when you query an external data source.
- Steps
	- BigQuery starts inference process by selecting a random file in the data source and scanning up to 100 rows of data to use as sample.
	- then examines each field and attempts to assign a data type to that field based on the values in the sample.
- use schema auto-detection for JSON or CSV files.
- not available for Avro files, ORC files, Parquet files, Datastore exports, or Firestore exports
 

BigQuery Data Transfer Service

It automates loading data into BigQuery from these services:

Google Software as a Service (SaaS) apps

- Campaign Manager
- Cloud Storage
- Google Ad Manager
- Google Ads
- Google Merchant Center (beta)
- Google Play
- Search Ads 360 (beta)
- YouTube Channel reports
- YouTube Content Owner reports

External cloud storage providers
- Amazon S3

Data warehouses

- Teradata
- Amazon Redshift
### Exporting Data
- can export the data in several formats.
- can export up to 1 GB of data to a single file.
- If exporting more than 1 GB of data, export to multiple files.
- need permissions to access the BigQuery table for export
 

Export limitations

- cannot export table data to a local file, Google Sheets, or to Google Drive.
- can export up to 1 GB of table data to a single file.
- cannot export nested and repeated data in CSV format.
- For nested and repeated data use Avro and JSON exports.
- If export in JSON format, INT64 (integer) data types are encoded as JSON strings.
- cannot export data from multiple tables in a single export job.
- cannot choose a compression type other than GZIP if exporting by Cloud Console or the classic BigQuery web UI.

You cannot change the location of a dataset after it is created, but you can make a copy of the dataset. You cannot move a dataset from one location to another, but you can manually move (recreate) a dataset.

##### Data format and compression

Data formats and compression types for exported data, are

 ![image](https://github.com/user-attachments/assets/ece906df-8f19-45f1-9aaa-9a4efc12b0de)


Exporting data stored in BigQuery

export table data by:

- Using the Cloud Console or the classic BigQuery web UI
- Using the bq extract CLI command
- Submitting an extract job via the API or client libraries

Exporting data into one or more files

- The destinationUris property indicates the location(s) and file name(s)
- BigQuery supports a single wildcard operator (*) in each URI.
- The wildcard can appear anywhere in the URI except as part of the bucket name.
- With wildcard BigQuery creates multiple sharded files based on the supplied pattern.
- wildcard is replaced with a number (starting at 0), left-padded to 12 digits.
### Optimize for Performance and Cost
Partitioned table

- a special table that is divided into segments, called partitions,
- make it easier to manage and query data.
- By dividing a large table improve query performance, and control costs
- partition tables by:
	- Ingestion time
	- Date/timestamp

Clustered tables

- table data is automatically organized based on the contents of one or more columns in the table’s schema.
- The columns specified are used to colocate related data.
- order of columns is important for the sort order of the data.
- Clustering improve the performance of queries
- During write data is sorted using the values in clustering columns.
- clustering is allowed over a partitioned table.
- Use clustering if
- data is already partitioned on a date, timestamp, or integer column.
- using filters or aggregation against particular columns in queries.
- clustering is based on ingestion time
	- date/timestamp
	- integer range
 

Views

- a virtual table defined by a SQL query.
- A view is queried it in the same way you query a table.
- query results of view contain data only from the tables and fields specified in the query that defines the view.
- can query views in BigQuery by
	- Query editor box in the Cloud Console
	- Compose Query option in the classic BigQuery web UI
	- BigQuery command-line tool’s bq query command
	- BigQuery REST API to programmatically call the jobs.query or query-type jobs.insert methods
	- BigQuery client libraries
- Also use view as a data source for a visualization
- views limitations
	- The dataset that contains view and the dataset that contains the tables referenced by the view must be in the same location.
	- cannot run a BigQuery job that exports data from a view.
	- cannot use the TableDataList JSON API method to retrieve data from a view.
	- cannot reference query parameters in views.
	- If schema change after view is created, the reported schema will be inaccurate
	- cannot include a user-defined function in the SQL query that defines a view.
	- cannot reference a view in a wildcard table query.
 

Reservations

- two pricing models
- On-demand pricing: You pay only for the data scanned by queries.
- Flat-rate pricing: Offers predictable and consistent month-to-month costs.
- By default, billed as per on-demand pricing model.
- With BigQuery Reservations, can switch to the flat-rate pricing model by purchasing commitments
- commitments are dedicated portions of query processing capacity measured in slots with cost of all bytes processed is included in the flat-rate price.
 

INFORMATION_SCHEMA

- For on-demand pricing, queries against INFORMATION_SCHEMA views 10 MB is the minimum billing amount
- For flat-rate pricing, queries against INFORMATION_SCHEMA views and tables consume purchased BigQuery slots.
- INFORMATION_SCHEMA queries are not cached
- charged each time you run an INFORMATION_SCHEMA query,
- not charged storage fees for the INFORMATION_SCHEMA views.
### Queries
- BigQuery supports two types of queries:
	- Interactive queries
	- Batch queries
- By default, BigQuery runs interactive queries, or query is executed as soon as possible.
- BigQuery queues each batch query on behalf and starts the query as soon as idle resources are available
- Run queries by
	- Query editor in the Cloud Console
	- Compose Query option in the BigQuery web UI
	- BigQuery command-line tool’s bq query command
	- BigQuery REST API to programmatically call the jobs.query or query-type jobs.insert methods
	- BigQuery client libraries
- Query execution involves root servers which interpret the query and send it to intermediate servers, which orchestrate the execution to many leaf servers. Leaf servers read from disk and execute.
- Analytical window functions:
	- Aggregate – sum, count
	- Navigation – lead, lag
	- Ranking, numbering – rank, cume_dist
	- “Partition by” is similar to “group by” but doesnt aggregate. This is different from bq partitions how data is stored.
- Data Types – struct, array, timestamp, int64, float64, string
- Inner table can be using WITH
- ARRAY_AGG – creates array. UNNEST – break array.
- STRUCT – creates struct
- User defined functions – sql udf as well as javascript udfs is possible
- Udf has constraints – size of udf output is limited, native javascript not supported
- Unnest – takes an array and returns table


Query jobs

- Jobs are actions that BigQuery runs on behalf to
	- load data
	- export data
	- query data
	- copy data.
- With Cloud Console, the classic BigQuery web UI, or the CLI for above jobs, a job resource is automatically created, scheduled, and run.
- If create a job programmatically, BigQuery schedules and runs the job for you.
- jobs execute asynchronously
- jobs can be polled for their status.

Saving and sharing queries

- If save a query, it can be
- private (visible only to you)
- shared at the project level (visible to project members)
- public (anyone can view it).
### BigQuery Logging and Monitoring
- use Cloud Monitoring to monitor BigQuery project:
- Display the metrics collected by Cloud Monitoring in own charts and dashboards.
- Create an alert for any thresholds.

Useful Metrics –
  
![image](https://github.com/user-attachments/assets/3400ff6a-620e-4e5b-9017-c830461de023)

- Use Cloud Audit Logs for audit log messages
- BigQuery service has 3 distinct messages:
	- AuditData
	- BigQueryAuditMetadata
	- AuditLog
- Go to the Logs Viewer page in the Cloud Console for viewing logs for policy tag events

### BigQuery Best Practices
For Controlling costs

- Avoid SELECT *
- Sample data using preview options
- Price queries before running them
- Limit query costs by restricting the number of bytes billed
- LIMIT doesn’t affect cost
- View costs using a dashboard and query audit logs
- Partition data by date
- Materialize query results in stages
- Consider the cost of large result sets
- Use streaming inserts with caution
 
For Query

- Avoid repeated joins and subqueries
- Carefully consider materializing large result sets
- Use a LIMIT clause with large sorts
- Denormalize data whenever possible
- Avoid excessive wildcard tables
- Reduce data before using a JOIN
- Do not treat WITH clauses as prepared statements
- Avoid tables sharded by date
 
For Storage

- Use the expiration settings to remove unneeded tables and partitions
- Take advantage of long-term storage
- Use the pricing calculator to estimate storage costs
# 15. Google Stackdriver
- provides dashboards and alerts for cloud-powered applications.
- Can configure Stackdriver Monitoring using the Stackdriver Monitoring Console.
- Can review performance metrics for cloud services, VMs, etc
- Can take a Debug Snapshot in applications running on App Engine, Compute Engine and Container Engine.
- Can view Application Logs.
- Setup Metrics, Monitor them and get alerts.
- Trace API calls and get a breakdown on response times and potential bottlenecks in code.
- Add log points to a running application, without the need to deploy app. This is a truly unique (and hopefully useful) feature.
  
### Monitoring
- Stackdriver Monitoring measures the health of cloud resources and applications by providing visibility into metrics
- Stackdriver Error Reporting identifies and analyzes cloud application errors.
- Stackdriver Debugger inspects the state of an application, deployed in Google App Engine or Google Compute Engine,
- Stackdriver Trace collects network latency data from applications deployed in Google App Engine.
- Stackdriver Logging provides real-time log management and analysis
- It supports default metrics such as CPU utilization, disk I/O, memory utilization, network traffic, and uptime
- it needs an agent to be installed in each VM for monitoring workload specific metrics.
- Supports custom metrics by Stackdriver API.
- Stackdriver Monitoring is based on collectd
  
### Logging
- collect and store logs from workloads deployed in GCP or AWS
- can gather logs from
	- Compute Engine
	- App Engine
	- EC2,
	- Google Cloud Audit Logs
- Based on Fluentd
- relies on the google-fluentd logging agent installed in each VM.
- logs can be viewed in the Stackdriver Log Viewer.
- can also use the Logging API to programmatically send the logs.
- Can export logs to external services

### Error Reporting
- service that aggregates, stores and displays errors in a central location.
- can show time charts, occurrences, affected user counts, first and last seen dates, and cleaned exception stack traces.
- supports applications deployed in App Engine and Compute Engine.
- can configure the service to send emails when a new error occurs.
- Errors can also be retrieved via REST API.
### Debugging
- Earlier called as Cloud Debugger
- Stackdriver Debugger lets developers inspect the state of the code of a Java, Python, or Go application in App Engine or Compute Engine.
- service doesn’t interfere with the performance of application.
- state of an application can be viewed without adding logging statements explicitly.
- works only with applications whose source code is stored in Google Cloud Source Repository, Github or Bitbucket.
### Tracing
- It is the distributed tracing system for applications deployed in App Engine.
- collects latency data from applications
- displays data in near real time in the console.
- investigate the latency impacting the application performance.
- can trace the latency data for requests to App Engine URIs and RPC calls.
  
# 16. Machine Learning
### What is Machine Learning?
- an application of artificial intelligence
- where a computer/machine learns from the past experiences (input data)
- and makes future predictions.
- The system performance should be at least human level.
- ML provides enables machines to learn autonomously based on experiences, observations and analysing patterns within a given data set without explicitly programming.
- Process – we input a data set, machine will learn by identifying and analysing patterns and learn to take decisions autonomously
- Example – Facebook’s facial recognition algorithm

Components

All ML algorithm have three components:

- Representation: how to represent knowledge like decision trees, sets of rules, etc.
- Evaluation: how to evaluate candidate programs (hypotheses) like accuracy, prediction and recall, likelihood, etc
- Optimization: how candidate programs are generated or the search process like combinatorial optimization, convex optimization, constrained optimization.

##### Types of Learning

There are four types of machine learning:

- Supervised learning: (or inductive learning) Training data includes desired outputs like identify spam, learning is supervised. It is most mature and  Defined as – if data is (x) and the output is (f(x)), goal is to learn the function for new data (x). Techniques include
	- Classification: when the function being learned is discrete.
	- Regression: when the function being learned is continuous.
	- Probability Estimation: when the output of the function is a probability.
- Unsupervised learning: Training data does not include desired outputs like clustering.
- Semi-supervised learning: Training data includes a few desired outputs.
- Reinforcement learning: Rewards from a sequence of actions.
### Inductive Learning
Used if
- If no human expert.
- no one can describe how to do it.
- If desired function changes frequently.
- If each user needs a custom function.
### Machine Learning Algorithms
##### Under-fitting & Over-fitting

We try to make the machine learning algorithm fit the input data by increasing or decreasing the models capacity. In linear regression problems, we increase or decrease the degree of the polynomials.

- Under-fitting: When the model has fewer features and hence not able to learn from the data very well. This model has high bias.
- Over-fitting: When the model has complex functions and hence able to fit the data very well but is not able to generalize to predict new data. This model has high variance.
 

##### Machine Learning Terminology

Labels

- It is the thing we’re predicting—the y variable in simple linear regression.
- Like future price, kind of animal shown in a picture, the meaning of an audio clip, etc.

Features

- It is an input variable—the x variable in simple linear regression.
- ML project can have a single feature or millions of features, specified as: x1,x2,…xn
- In a spam detector, the features could include the following:
- words in the email text
- sender’s address
- time of day the email was sent
- email contains the phrase “one weird trick.”

Examples

- It is a particular instance of data, x.
- two categories: labelled examples and unlabeled examples
- A labelled example includes both feature(s) and the label or – labelled examples: {features, label}: (x, y)
- Use labelled examples to train the model.
- An unlabeled example contains features but not the label. That is: unlabeled examples: {features, ?}: (x, ?)
 

##### Models

- It defines the relationship between features and label.
- two phases of a model’s life:
	- Training means creating or learning the model or show the model labelled examples and enable the model to gradually learn the relationships between features and label.
	- Inference means applying the trained model to unlabeled examples.
 

##### Bias

- A ML model has low bias if its predictability level is high.
- Hence, fewer mistakes when it is working on a dataset.
 

##### Cross-validation bias

Technique that provides an accurate measure of the performance of ML model.

##### Epoch

1 traversal thru entire dataset. Traversal is called evaluation 

##### Underfitting

- If ML model is not able to predict with a decent level of accuracy, then the model underfits.
- Due to
	- not selecting the correct features for the prediction
	- the problem statement is too complex
 

##### Overfitting

- It occurs when the model fits the data too well.
- Overfitting model learns the detail and noise in the training data so as to negatively impacts performance
- can be solved by decreasing the number of features/inputs or by increasing the number of training examples
 

##### 3 ML approaches

- Tensorflow
- ML engine
- prebuilt models
 

##### Tensorflow

- Has estimator api
- model abstraction layer(layers, error function)
- python low level library
- c++ low level library
- hardware(cpu, gpu, tpu)
- Execution
	- There is a build and run stage.
	- Build stage builds the graphs.
	- Run stage runs the tensor in a distributed manner.
- Placeholder and feed_dict is a dynamic way of passing values
- Data types are inferred implicitly
- eager allows you to avoid the build-then-run stages. Used only for testing purposes.
- Model types:
	- Linear regressor
	- DNregressor – deep neural network
	- Linear classifier
	- DNclassifier
 

##### ML engine

- Does both training and prediction
- Supports tensorflow, xgboost, scikit learn, keras in beta
 

##### Other terms

- Training example: a sample from x including its output from the target function
- Target function: the mapping function f from x to f(x)
- Hypothesis: approximation of f, a candidate function.
- Concept: A boolean target function, positive examples and negative examples for the 1/0 class values.
- Classifier: Learning program outputs a classifier that can be used to classify.
- Learner: Process that creates the classifier.
- Hypothesis space: set of possible approximations of f that the algorithm can create.
- Version space: subset of the hypothesis space that is consistent with the observed data.
### Neural Networks
In this, we will learn about the concepts of Neural Networks.

##### What are Neural Networks?
- It has multiple nodes that interconnects to each other,
- mimics the neurons in our brain.
- Each neuron inputs from another neuron, performs tasks, and transfers to another as output.

![image](https://github.com/user-attachments/assets/b33a658a-0ea5-4381-b94d-baa096ab3726)


In figure

- Each circular node is an artificial neuron
- arrow represents a connection from the output of one neuron to the input of another.

##### Layers
- As per diagram, there are 4 layers present – Layer 1, Layer 2, Layer 3 and Layer 4.
- Every deep neural network consists of three types of layers, which are: Neural Networks

![image](https://github.com/user-attachments/assets/8b871431-2ffb-4013-97a7-f165526cc0ec)

  
- Input Layer (Layer 1): provides the input parameters and passes parameters to further layers without any computation at this layer.
- Hidden Layers (Layers 2 and 3): Perform the computations on the inputs receiving from the previous layers and pass on the result to the next layer. More the number of hidden layers, deeper is the network.
- Output Layer (Layer 4): gives final output after receiving the results from the previous layers.

###### Weights

- This attaches some weightage to a certain feature.
- Some features might be more important than others
- weights calculate the weighted sum for each neuron. x1, x2, x3, x4 represent the weights associated with the corresponding connections in the deep neural network.

Activation Function

- decide if a neuron to activate or not depending on their weight sum.
- hidden layer has an activation function associated with it.

Backpropagation

![image](https://github.com/user-attachments/assets/47c347a6-02c7-4e48-8278-1b8a4e5eedbf)


- This is for neural net training.
- For fine-tuning weights of a neural net based on the error rate obtained in the previous epoch (i.e., iteration).
- Proper tuning of weights reduce error rates and make model reliable.
- Backpropagation is a short form for “backward propagation of errors.”
- standard method of training artificial neural networks.
- calculate the gradient of a loss function with respects to all the weights in the network.
- Backpropagation
- Inputs X, arrive through the preconnected path
- Input is modeled using real weights W, randomly selected.
- Calculate the output for every neuron from the input layer, to the hidden layers, to the output layer.
- Calculate the error in the outputs: ErrorB= Actual Output – Desired Output
- Travel back from the output layer to the hidden layer to adjust the weights such that the error is decreased.
- Keep repeating the process until the desired output is achieved


Backpropagation Networks Types:

- Static back-propagation: produces mapping of a static input for static output.
- Recurrent Backpropagation: It is fed forward until a fixed value is achieved. After that, the error is computed and propagated backward.
- Feature requirements for feature engineering
- should be reasonably related

##### Feature value should be known at the time of prediction without latency

- Numeric with range of meaningful magnitude.
- Difficult for categorical inputs.
- Need to find vector/bitmask representation(1 hot encoding), for NL, we can use wordtovec.
- Need to have enough examples of each feature value.
- For continuous numbers, use windows.
- Feature crosses can be done using human sights, this will simplify ml model.

##### Model architecture

- Linear models work well for sparse features(like employee id).
- Neural network model works well for dense features(like price, color(rgb))
- Regressor – linear, sparse features, specific, many features, memorization, employee id, nlp
- DNN – non-linear, dense features, generalization, color, price
- Wide and linear – combination of both, recommendation, search and ranking

##### Hypertuning

- Changing model parameters to find the right set of parameters for a particular result.
- evaluate rmse with the parameter and keep tuning to lower rmse.
- define what metric we want for evaluation like rmse.

##### Reinforcement Machine Learning Algorithms

- A type of Machine Learning where machine is required to determine the ideal behaviour within a specific context, in order to maximize its rewards.
- It works on the rewards and punishment principle
- for any decision which a machine takes, it will be either be rewarded for correct or punished.
- So machine will learn to take the correct decisions to maximize the reward in the long run.
- Can focus on long-term rewards or the short-term rewards.
- If machine is in a specific state and has to be the action for the next state in order to achieve the reward, it is called the Markov Decision Process.
- The environment is modelled as a stochastic finite state machine with
- inputs (actions sent from the agent)
- outputs (observations and rewards sent to the agent)
- It requires clever exploration mechanisms.
- Selection of actions with careful reference to the probability of an event
- It is memory expensive to store the values of each state

##### Important terms

- Agent: It is an assumed entity which performs actions in an environment to gain some reward.
- Environment (e): A scenario that an agent has to face.
- Reward (R): An immediate return given to an agent when he or she performs specific action or task.
- State (s): State refers to the current situation returned by the environment.
- Policy (π): It is a strategy which applies by the agent to decide the next action based on the current state.
- Value (V): It is expected long-term return with discount, as compared to the short-term reward.
- Value Function: It specifies the value of a state that is the total amount of reward. It is an agent which should be expected beginning from that state.
- Model of the environment: This mimics the behavior of the environment. It helps you to make inferences to be made and also determine how the environment will behave.
- Model based methods: It is a method for solving reinforcement learning problems which use model-based methods.
- Q value or action value (Q): Q value is quite similar to value. The only difference between the two is that it takes an additional parameter as a current action.

Example:

Example of cat training

- cat is an agent that is exposed to the environment. In this case, it is house. An example of a state could be cat sitting, and you use a specific word in for cat to walk.
- Our agent reacts by performing an action transition from one “state” to another “state.”
- For example, cat goes from sitting to walking.
- The reaction of an agent is an action, and the policy is a method of selecting an action given a state in expectation of better outcomes.
- After the transition, they may get a reward or penalty in return.


##### Approaches to implement a Reinforcement Learning algorithm.
- Value-Based: try to maximize a value function V(s).
- Policy-based: try to come up with such a policy that the action performed in every state helps you to gain maximum reward in the future.
- Model-Based: need to create a virtual model for each environment.
# 17. Google AI Platform (Formerly Cloud ML Engine)

### AI Platform Overview
### AI Platform Training
### AI Platform Pipelines

# 18. Pre-trained Machine Learning API’s
### Pre-trained ML API’s
### Cloud Vision Product Search
### Vision API
### NL API

# 20. Datalab
### Datalab Overview
### Running Datalab

# 21. Dataprep
### Dataprep Overview

# 22. DataStudio
### DataStudio Basics
### Steps to use the tool

# 23. Cloud Composer
### Cloud Composer Overview

# 24. Security and Compliance
### Google Security Culture
### Operational Security
### Technology with Security at Its Core
### Independent Third-Party Certifications
### Regulatory compliance
### General Data Protection Regulation (GDPR)
### The Health Insurance Portability and Accountability Act of 1996 (HIPAA)
### Cloud Data Loss Prevention (DLP)
### Encryption Basics
### Cloud Key Management Service

# 25. Cloud IAM
### Access management
### Cloud IAM policy
### Cloud IAM working
