# Chapter 6: Data Storage and Operations

# 1. Introduction

<aside>
💡 Data Storage and Operations includes the design, implementation and support of stored data to maximise its value through the lifecycle, from creation/acquisition to disposal.

</aside>

2 sub activities:

- **Database support**
    - Activities related to the data lifecycle from implementation of a database environment, through obtaining, backing up and purging data. it includes ensuring the database performs well, monitoring and tuning
- **Database technology support**
    - Includes defining technical requirements that will meet organizational needs, defining technical architecture, installing and administering technology, and resolving issues related to technology.
    
    Note → DBA: Database Administrator
    

(2024, revised version):

![image.png](Chapter%206%20Data%20Storage%20and%20Operations%20c2225ba7767d4bee865015173b0765b2/image.png)

- (Original version diagram)
    
    ![Screenshot 2024-06-05 at 16.59.55.png](Chapter%206%20Data%20Storage%20and%20Operations%20c2225ba7767d4bee865015173b0765b2/Screenshot_2024-06-05_at_16.59.55.png)
    

## 1.1 Business Drivers

<aside>
💡 A reliable data storage infrastructure minimizes the risk of disruption and unavailability, which is key for business continuity (especially for organisations that rely on data).

</aside>

## 1.2 Business Goals

1. Manage availability of data throughout the data lifecycle
2. Ensure the integrity of data assets
3. Manage performance of data transactions

**Data Storage and Operations represent a highly technical side of data management.** Guiding principles:

- **Identify and act on automation opportunities**
    - automate database processes,
    - develop tools and processes that shorten cycles,
    - reduce errors and rework,
    - minimize the impact on the development team,
    - do collaboration with data modelling and data architecture
- **Build with reuse in mind**
    - develop abstract and reusable data objects
- **Understand and appropriately apply best practices**
- **Connect database standards to support requirements**
    - SLAs reflect DBA-recommended and developer-accepted methods of ensuring integrity and data security
- **Set expectation for the DBA role in project work**
    - include the DBA in all SDLC phases of a project

## 1.3 Essential Concepts

### 1.3.1 Database Terms

![Screenshot 2024-06-05 at 17.00.55.png](Chapter%206%20Data%20Storage%20and%20Operations%20c2225ba7767d4bee865015173b0765b2/Screenshot_2024-06-05_at_17.00.55.png)

- **Database:** Any collection of stored data, regardless of structure or content
- **Instance:** An execution ****of database software controlling access to a certain area of storage
- **Schema:** A subset of database objects contained within a database or instance, usually with something in common. Used to isolate sensitive data from general user base
- **Node:** An individual computer part of a distributes database
- **Database abstraction:** An API (common Application Interface) is used to call database functions

### 1.3.2 Data Lifecycle Management

<aside>
💡

Data lifecycle management includes implementing policies and procedures for acquisition, migration, retention, exporation, and disposition of data.

</aside>

<aside>
💡 The Database Administrator (DBA) is the custodian of all database changes. The DBA defines, implements and controls all the changes. The DBA must have a plan to roll back the changes if necessary.

</aside>

### 1.3.3 Administrators

Many DBAs specialize as Production, Application, Procedural or Development DBAs. Some organisations also have Network Storage Administrators (NSA), who specialize in supporting the data storage system separately from the data storage applications and structures.

- **Production DBA**
    
    <aside>
    💡 Responsible for data operations management
    
    </aside>
    
    - Ensures performance and reliability of the database through performance tuning, monitoring, error reporting, and other activities.
    - Implement Backup and recovery mechanisms
    - Implement clustering and failover of the database if continual data availability is required
    - Other database maintenance activities such as mechanisms for archiving
    - Deliverables of Production DBAs:
        - A production database environment
        - Mechanisms and processes for controlled implementation of changes to databases in the production environment
        - Mechanisms for ensuring availability, integrity and recoverability of data in response to all circumstances that could result in loss or corruption of data.
        - Mechanisms for detecting and reporting database errors
        - Data availability, recovery and performance in accordance with SLAs
        - Mechanisms and processes for monitoring database performance
- **Application DBA**
    
    <aside>
    💡 Responsible for one or more databases in **all** environments (DEV/TEST, QA, and PROD), as opposed to database systems administration for any of these environments.
    
    </aside>
    
    - Application DBAs are integral members of an application support team.
- **Procedural and Development DBA**

<aside>
💡

Procedural DBAs lead the administration and development of procedural database objects (stored procedures, triggers, and user-defined functions).

</aside>

<aside>
💡

Development DBAs focus on data design activities, including creating and managing special use databases (e.g., sandbox database).

</aside>

- **NSA** Network storage administrator
    - support data storage arrays (software and hardware).

### 1.3.4 Database Architecture Types

![Screenshot 2024-06-05 at 17.14.23.png](Chapter%206%20Data%20Storage%20and%20Operations%20c2225ba7767d4bee865015173b0765b2/Screenshot_2024-06-05_at_17.14.23.png)

**Centralized databases**

- A centralized database manages a single database

<aside>
💡 all the data in one system in one place. all users come to one system, no alternatives if it is unavailable

</aside>

- ideal for restricted data, but not useful for data that needs to be widely available.

**Distributed Database**

- A distributed database manages multiple databases on multiple systems
- Depending on the autonomy of the component systems, these can be classified as: federated (autonomous) or non-federated (non-autonomous)

<aside>
💡 **Quick access to data over many of nodes, each offering local computation and storage.** DBMS replicates across nodes, and can detect and handle failures. MapReduce divides a data request into small fragments over the nodes.

</aside>

**Federated Database**

<aside>
💡 A federated database system maps multiple autonomous database systems into a single federated database, connected via a network. Remain autonomous but allow sharing of data (federation, which is an alternative to merging disparate data).

</aside>

![Screenshot 2024-06-05 at 17.19.05.png](Chapter%206%20Data%20Storage%20and%20Operations%20c2225ba7767d4bee865015173b0765b2/Screenshot_2024-06-05_at_17.19.05.png)

A FDBMS can be loosely or tightly coupled:

- **Loosely coupled**: Component databases construct their own federated schema.
- **Tightly coupled**: Component systems use independent processes to construct and publish an integrated federated schema

![image.png](Chapter%206%20Data%20Storage%20and%20Operations%20c2225ba7767d4bee865015173b0765b2/image%201.png)

Blockchain database

<aside>
💡 A **type of federated database** used to securely manage non-fungible transactions. There are two types of structures: individual records and blocks. Each transaction has a record. The database creates chains of time-bound groups of transactions (blocks) that also contain information from the previous block in the chain. Hash algorithms create information on the transactions which can never change. Tampering is evident if the hash values no longer match.

</aside>

Virtualization / Cloud Platform 

<aside>
💡 Virtualisation (Cloud computing) provides computation, software, data access and storage without end-user knowledge of the physical location or configuration of the system.

</aside>

- **Virtual machine image:** Users purchase virtual machine instances for a limited time. Either load own database or use an optimised installation of the database
- **Database-as-a-service (DaaS):** Database service provider installs and maintains the database and application owners pay according to their usage
- **Managed database hosting in the cloud:** The cloud provider hosts the database and manages it on the application owner’s behalf

DBAs and Network and System Administrators need to establish a systematic project approach to the following functions (as well as the security aspects):

- **Standardisation/consolidation:** Based on Data Governance policy, consolidation reduces the number of data storage locations and standard procedures are developed by DBAs and Data Architects
- **Server virtualisation:** Enables reduction of cost in infrastructure management
- **Automation** of data tasks
- **Security:** Integrate security of virtual systems with security of physical infrastructures

### 1.3.5 Database Processing Types

![Screenshot 2024-06-05 at 17.40.22.png](Chapter%206%20Data%20Storage%20and%20Operations%20c2225ba7767d4bee865015173b0765b2/Screenshot_2024-06-05_at_17.40.22.png)

- **ACID**
    
    <aside>
    💡 reliability within database transactions. Relational - SQL Server
    
    </aside>
    
    - **Atomicity:** All operations are performed, or none are. If one fails, the entire transaction fails
    - **Consistency:** The transaction must meet all rules defined by the system at all times and must void a half-completed transaction
    - **Isolation:** Each transaction is independent
    - **Durability:** Once complete, the transaction cannot be undone
- **BASE**
    
    <aside>
    💡 Increase in volume and variability of data, the need to document and store less structured data, read-optimised data workloads, greater flexibility of scaling and design. Common in big data environments.
    
    </aside>
    
    - **Basically Available:** System guarantees some level of data availability even if there are node failures
    - **Soft state:** System in constant state of flux. Data may be available but not current
    - **Eventual consistency:** Data eventually becomes consistent through nodes
- **CAP Theorem**
    
    <aside>
    💡 CAP Theorem (or Brewer’s Theorem) – **the larger the distributed system, the lower the compliance to ACID**. There is a trade-off between the following properties and at most 2 of the following 3 properties can exist in a shared-data system:
    
    </aside>
    
    - **Consistency:** The system must operate as designed and expected at all times
    - **Availability:** The system must be available and respond to each request
    - **Partition Tolerance:** The system must be able to continue operations during occasions of data loss or partial system failure
    
    ![Screenshot 2024-06-05 at 17.42.07.png](Chapter%206%20Data%20Storage%20and%20Operations%20c2225ba7767d4bee865015173b0765b2/Screenshot_2024-06-05_at_17.42.07.png)
    
    Used to drive Lambda Architecture for big data, which uses two paths for data: (refers to Chapter 14 where it appears as 14.1.3.7 Services-Based Architecture (SBA)):
    
    - Speed path: Availability and Partition Tolerance are most important
    - Batch path: Consistency and Availability are most important

### 1.3.6 Data Storage Media

- **Disk and Storage Area Networks (SAN):** Disk arrays and SAN. Persistent storage
- **In-Memory:** In-Memory Databases (IMDB) are loaded into volatile memory where all processing takes place. Faster response than disk
- **Columnar Compression Solution:** For data sets where data values are repeated to a large extent and may be compressed. Reduces I/O time
- **Flash Memory:** Solid stat

### 1.3.7 Database Environment

<aside>
💡 There are various environments used during the system development lifecycle

</aside>

- **Production Environments:** The technical environment where all business processes occur. The DBA team should be the only team implementing changes, adhering strictly to standards and procedures
- **Pre-Production Environments:**
    - **Development:** Slimmer version of production for developers to test new code or patches
    - **Test:** Used for**:**
        - Quality Assurance testing (QA)
            - test a system's functionality against the requirements
        - Integration testing
        - User Acceptance Testing (UAT)
        - Performance Testing
    - **Sandboxes or Experimental Environments:** Can be read only access to production data for experimentation

### 1.3.8 Database Organisation

![Screenshot 2024-06-05 at 17.45.34.png](Chapter%206%20Data%20Storage%20and%20Operations%20c2225ba7767d4bee865015173b0765b2/Screenshot_2024-06-05_at_17.45.34.png)

- **Hierarchical**
    
    <aside>
    💡 oldest database model. Tree structures with one-to-many parent-child relationship. Example directory, trees and XML
    
    </aside>
    
- **Relational**
    
    <aside>
    💡 Based on set theory and relational algebra. Set operations (union, intersection, minus) in the form of SQL (Structured Query Language) are used to retrieve data. To write data the schema must be known (**schema on write**). Relational databases are row-oriented. The database management system is called RDBMS
    
    </aside>
    
    - Tables are sets or relations
    - Attributes (columns)
    - Tuples (Rows)
    
    **Variations on relational databases**
    
    - **Multidimensional:** Allows searching using several data element filters simultaneously. Uses a type of SQL called MDX (Multidimensional eXpression)
    - **Temporal:** Built in support for handling time
- **Non-Relational (NotOnly SQL)**
    - **Schema-on-read** allows data to be read in different ways. NoSQL means the storage structure is not bound by tabular design. NoSQL databases are used in Big Data and real-time web applications as they are optimised for retrieval and appending operations.
    - **Column-oriented:** Used in BI applications as redundant data can be compressed. Difference between column-oriented and row-oriented (usually relational):
        - **Column-oriented is more efficient when:**
            - Aggregating over many rows
            - New values for that column are applied at once as there is no need to touch columns for the other rows
            - Online Analytical Processing (OLAP)
        - **Row-oriented is more efficient when:**
            - Many columns of a single row required at once
            - Writing a whole row of new data
            - Online Transaction Processing (OLTP)
- **Spatial:** Store and query data that represents objects defined in geometrical space. Use special indexes to perform database operations. Open Geospatial Consortium standard
- **Object/Multi-media:** Hierarchical storage Management System manages the media objects
- **Flat File Database:** Data in rows and columns as a single file. Used by Hadoop databases
- **Key-Value Pair:** A key identifier and a value:
    - **Document Databases:** Each document has a key. Use XML or JSON (Java Script Object Notation) structures
    - **Graph Databases:** Key-value pairs where the focus is on the relationship between nodes rather than the nodes themselves
- **Triplestore:** A data entity composed of subject-predicate-object. Best for taxonomy and thesaurus management. Resource Description Framework (RDF):
    - **Subject:** a resource
    - **Predicate:** relationship between the subject and object
    - **Object:** the object

### 1.3.9 Specialised Databases

- Computer Assisted Design and Manufacturing (CAD/CAM): Object database
- Geographical Information Systems (GIS): Geospatial databases
- Shopping-cart applications: XML databases to store customer order data

### 1.3.10 Common Database Practices

- **Archiving**
    
    <aside>
    💡 The process of moving data off immediately accessible media onto less expensive media with lower retrieval performance. Schedule regular restoration tests
    
    </aside>
    
    Archival processes must be aligned with the partitioning strategy to ensure optimal availability and retention:
    
    - Create a secondary area on a secondary database server
    - Partition database tables into archival blocks
    - Replicate to the separate database
    - Create backups (tape or disk)
    - Create jobs that periodically purge unneeded data
- **Capacity and growth projections**
    
    <aside>
    💡 Decide how much storage is needed, and work out expansion needs.
    
    </aside>
    
- **Change Data Capture (CDC)**
    
    <aside>
    💡 Detecting that data has changed and ensure information relevant to the change is stored appropriately. Log-based replication
    
    </aside>
    
- **Purging**
    
    <aside>
    💡 Purging is the process of completely removing data from media so that it cannot be retrieved.
    
    </aside>
    
- **Replication**
    - **Replication transparency:** The same data is stored on multiple storage devices and is consistent throughout the database system, so that users cannot tell which database copy they are using.
        - **Active replication:** Create and store the same data at every replica from every other replica
        - **Passive replication:** recreating and storing data on the primary, then transferring it to secondary replicas
    - Replication has 2 dimensions of scaling
        - Horizontal: More data replicas
        - Vertical: Data replicas located geographically further away
    - Multimaster replication
        - Update any node and ripples through other servers
        - Often desired, but increases complexity and cost
    - two primary replication patterns
        - **Mirroring:** Updates to the primary are replicated immediately to the secondary as part of a two-phase commit**.**
        - **Log Shipping:** The secondary receives and applies copies of the primary database’s transaction log at regular intervals
        
        ![Screenshot 2024-06-06 at 09.36.41.png](Chapter%206%20Data%20Storage%20and%20Operations%20c2225ba7767d4bee865015173b0765b2/Screenshot_2024-06-06_at_09.36.41.png)
        
- **Resilience and Recovery**
    
    <aside>
    💡 Resiliency is a measure of how tolerant a system is to error conditions, and how well it recovers
    
    </aside>
    
    - Three recovery types:
        - **Immediate recovery:** Predicting and automatically resolving issues
        - **Critical recovery:** Plan to restore the system quickly to minimise delays to business processes
        - **Non-critical recovery**: Restoration can be delayed until critical systems have been restored
- **Retention**
    
    <aside>
    💡 How long data is kept available. Affects capacity planning. Data retention plans are also affected by Data Security, as some data has legal requirements to be retained a specific time.
    
    </aside>
    
- **Sharding**
    
    <aside>
    💡 Small chunks of the database are isolated so replication is merely a file copy.
    
    </aside>
    

## 2. Activities

<aside>
💡 Data Technology Support (selecting and maintaining the software that stores and manages the data) and Data Operations Support (the data and processes that the software manages).

</aside>

## 2.1 Manage Database Technology

<aside>
💡 The **information technology infrastructure library (ITIL)** is the leading reference model

</aside>

### 2.1.1 Understand Database technology Characteristics

<aside>
💡 DBAs and Data Architects combine their knowledge of available tools with business requirements to suggest the best technology.

</aside>

### 2.1.2 Evaluate Database Technology

Some of the factors to consider when selecting a DBMS:

- Product architecture and complexity
- Volume and velocity limits
- Application profile such as transaction processing and BI
- Hardware platform and operating system support
- Availability of supporting software tools
- Performance benchmarks
- Scalability
- Software, memory and storage requirements
- Resiliency, including error handling and reporting

### 2.1.3 Manage and Monitor Database Technology

DBAs need to be trained to function as Level 2 technical support. They need to have a working knowledge of application development skills. DBAs work with business users and application developers to ensure the most effective use of technology.

## 2.2 Manage Databases

<aside>
💡 Database support is provided by DBAs and NSAs (Network Storage Administrators).

</aside>

### 2.2.1 Understand Requirements

- **Define storage requirements** initial capacity estimate for first year and growth projection for next few year. take data, storage, indexes, logs and mirrors into account
- **identify. usage patterns** databases have predictable usage patterns
    - transactional based
    - large data set write or retrieval
    - time based: month-end, lighter on weekends
    - location based - more populated areas have more transactions
    - priority based - some departments or batch IDs have higher prioriy
- **Define access requirements**: the authorisation to access different data files and the standard languages and methods to do it

### 2.2.2 Plan for business continuity

<aside>
💡 Recovery plan for all databases and database servers in the event of a disaster which could result in loss or corruption of data. Identify critical databases which need to be restored first.

</aside>

<aside>
💡 consider written policies and procedures, impact mitigating measures, required recovery time and acceptable amount of disruption, the criticality of the documents

</aside>

- **Make back ups**
    - Back up databases and transaction logs
    - Backup frequency determined by SLA.
    - Incremental and complete backups
    - Keep backups on a separate file system
- **Recover data:** DBA executes restoration of data. Test recovery periodically

### 2.2.3 Develop Database instances

- Installing and updating DBMS software
- Maintaining multiple environment installations, including different DBMS versions
- Installing and administering related data technology

**Manage the physical Storage Environment**

<aside>
💡 Storage environment management needs to follow Software Configuration Management (SCM) processes or ITIL methods to record modification to the database configuration

</aside>

- 4 processes:
    - **Configuration Identification:** DBAs with Data Stewards, Data Architects and Data Modellers to identify attributes that define end-user configuration. These must be baselined, recorded and only changed with formal change control
    - **Configuration change control:** Processes and approval stages to change the above attributes
    - **Configuration status accounting:** Report on the configuration at any point in time
    - **Configuration audits:**
        - Physical configuration audit: an item is installed in accordance with design documentation
        - Functional configuration audit: Performance attributes of an item are achieved
    
    DBAs must communicate any changes to the physical attributes to modellers, developers and Metadata managers.
    
    DBAs also maintain metrics on data volume, capacity projections, query performance and statistics on the physical objects.
    

**Manage Database Access Controls**

- DBAs oversee the following functions to protect data assets:
    - **Controlled Environment:** DBAs and NSAs. Network roles and permissions, 24/7 monitoring, firewall management, patch management
    - **Physical security:** Simple Network Management Protocol (SNMP)-based monitoring, data audit logging, disaster management and database backup plans
    - **Monitoring:** Continuous monitoring of servers
    - **Controls:** Access controls, database auditing, intrusion detection and vulnerability assessment tools

**Create Storage Containers**

<aside>
💡 all data must be stored on the physical drive and organised for ease of load, search and retrieval

</aside>

**Implement Physical Data Models**

<aside>
💡 DBAs implement the physical layout of the data model in storage. The physical data model includes storage objects, indexing objects, and any encapsulated code objects required to enforce quality rules, connect database objects and achieve database performance.

</aside>

**load data**

- DBMS should have a bulk load facility to load data into a new database. Data must be in the right format for the target object.
- Third party data can be updated regularly by the service. DBAs must be aware of any legal restrictions before loading third party data.
- DBAs may load data manually, or automate and schedule loading.
- Responsibility for data acquisition services in a managed environment is centralised with data analysts who document it in the logical data model. Developers create scripts if necessary. DBA implements the processes to load the data into the database.

**Manage data replication**

- DBAs advise data replication decisions on:
    - Active or passive replicating
    - Distributed concurrency control from distributed data systems
    - The appropriate methods to identify updates to data under the Change Data Control process:
        - Timestamp
        - Version numbers

### 2.2.4 Manage Database Performance

<aside>
💡 Database performance depends on availability and speed. Availability of space and query optimisation are part of performance.

</aside>

- **Set database performance service levels**
    
    <aside>
    💡 System performance, data availability and recovery expectations, and expectations for teams to respond are governed by Service Level Agreements (SLAs) between IT data management services and data owners.
    
    </aside>
    
    ![Screenshot 2024-06-06 at 11.27.23.png](Chapter%206%20Data%20Storage%20and%20Operations%20c2225ba7767d4bee865015173b0765b2/Screenshot_2024-06-06_at_11.27.23.png)
    
- **Manage database Availability**
    
    <aside>
    💡 **Availability** is the percentage of time that a system or database is available for productive work
    
    </aside>
    
    - 4 factors affect availability:
        - **Manageability:** The ability to create and maintain an environment
        - **Recoverability:** Establish service after interruption, and correct the errors caused
        - **Reliability:** Ability to deliver service at specified levels for a stated period
        - **Serviceability:** Identify and diagnose problems and solve them
    - things that prevent databases from being available
        - Planned outages
        - Unplanned outages
        - Application problems
        - Data problems
        - Human error
    - DBAs are responsible for doing everything possible to ensure databases stay online and operational:
        - Run database backup utilities
        - Run database reorganisation utilities
        - Run statistics gathering utilities
        - Run integrity gathering utilities
        - Automating the above utilities
        - Exploiting table clustering and partitioning
        - Replicating data across mirror databases to ensure high availability
- **Manage database execution**
    
    <aside>
    💡 DBAs manage database execution, logging and log sizes and synchronisation
    
    </aside>
    
- **Maintain database performance service levels**
    
    <aside>
    💡 DBAs generate performance analysis reports regularly and compare them with previous reports to identify negative trends and analyse problems over time.
    
    </aside>
    
    - **Transaction performance vs Batch performance**: Batch jobs must complete within a batch window
    - **Issue remediation:** Common reasons for poor database performance are:
        - Memory allocation or contention
        - Locking and blocking
        - Inaccurate database statistics
        - Poor coding
        - Inefficient complex table joins
        - Insufficient indexing
        - Application activity
        - Overloaded servers
        - Database volatility
        - Runaway queries
- **Maintain alternate environments**
    - Types of alternate environments:
        - **Development:** Test changes that will be implemented in production
        - **Test:** QA, Integration testing, UAT and performance testing
        - **Sandboxes:** Experimental environments
        - **Alternate production environments:** Support failover, offline backups and resiliency support systems

### 2.2.5 Manage Test data Sets

<aside>
💡 Efficient testing requires high quality test data to be generated and managed.

</aside>

### 2.2.6 Manage Data Migration

<aside>
💡 Data Migration is the process of transferring data between storage types, formats or computer systems with as little change as possible. Usually performed programmatically, automated based on rules.

</aside>

# 3 Tools

- Data modelling tools
- Database monitoring tools
- Database Management tools
- Developer support tools

# 4. Techniques

- **Test in lower environments:**
    - Test upgrades and patches on the lowest level first, development
    - Then install and test on higher levels, production last
- **Physical Naming Standards:** ISO/IEC 11179 – Metadata Registries (MDR) Part 5
- **Script Usage for All Changes:** Test any change scripts in non-production before applying

# 5. Implementation Guidelines

## 5.1 Readiness assessment / risk assessment

- **Data Loss**: SLAs specify general requirements for protection. Ongoing assessment to ensure robust technical responses to cyber threat are in place
- **Technology readiness**: Does the organisation have the skill set to implement newer technology?

## 5.2 Organisational and Cultural Change

- **Proactively communicate**: DBAs should be in close communication with project teams at all stages of the project, to detect and resolve issues as early as possible
- **Communicate with people on their level and in their terms**
- **Stay business focused:** Objective is to meet business requirements and derive maximum value
- **Be helpful:** Not helping may force people to ignore standards and find another way
- **Learn continually:** Setbacks and problems are lessons which can be applied later

<aside>
💡 Understand stakeholders and their needs. Develop clear, concise, practical, business focused standards for doing the best possible work in the best possible way. Teach and implement those standards in a way that provides maximum value to stakeholders and earns their respect.

</aside>

# 6. Data Storage and Operations Governance

## 6.1 Metrics

**Storage metrics** may include:

- Count of databases by type
- Aggregated transaction stats
- Capacity metrics
- Storage service usage
- Requests made against storage services
- Performance improvements of applications using service

**Performance metrics:**

- Transaction frequency and quantity
- Query performance
- API service performance

**Operational metrics:**

- Aggregated statistics about data’s retrieval times
- Backup size
- Data quality measurement
- Availability

**Service metrics:**

- Issue submission, resolution and escalation count by type
- Issue resolution time

## 6.2 Information Asset Tracking

- Ensure organisation complies with **software licensing and annual support agreements**
- Determine **TCO (total cost to ownership)** for each technology product

## 6.3 Data Audits and Data Validation

A **data audit** is the evaluation of data based on defined criteria, typically performed to investigate specific concerns about the data. A data audit includes:

- Project specific checklist
- Comprehensive checklist
- Required deliverables
- Quality control criteria

**Data validation** is the process of evaluating stored data against established acceptance criteria (from the Data Quality team or customer specifications) to determine its quality and usability.

DBAs support data audits and validation by:

- Help develop and review the approach
- Perform preliminary data screening and review
- Develop data monitoring methods
- Applying statistical, geo-statistical and bio-statistical techniques to optimise the data
- Support sampling and analysis
- Review data
- Provide support for data discovery
- Act as the SME for questions related to database administration