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
