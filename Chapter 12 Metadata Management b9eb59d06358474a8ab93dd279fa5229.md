# Chapter 12: Metadata Management

# 1. Introduction

<aside>
💡 Planning, implementation and control activities to enable access to high quality integrated metadata

</aside>

- Metadata helps an organisation understand its data, systems and workflows.
- Metadata includes information about:
    - Technical and business process
    - Data rules and constraints
    - Logical and physical data structures
    - Describes the data(databases, data elements, data models)
    - concepts the data represents
    - relationships between data and concepts

![Screenshot 2024-06-18 at 16.04.29.png](Chapter%2012%20Metadata%20Management%20b9eb59d06358474a8ab93dd279fa5229/Screenshot_2024-06-18_at_16.04.29.png)

## 1.1 Business Drivers

<aside>
💡

Data cannot be managed without metadata, which must be managed as well.

</aside>

- Metadata helps:
    - Increase confidence in data by providing context, and measurement of the data quality
    - Operational efficiency by identifying redundant data and process
    - Prevent the use of out of date or incorrect data
    - Reduce data-oriented research time
    - Improve communication between business and IT
    - Creates accurate impact analysis
    - Reduce system development lifecycle time
    - Support regulatory compliance

## 1.2 Goals and principles

- **GOALS**
    - Provide organisational understanding go business terms and usage
    - Collect and integrate metadata from diverse sources
    - Provide a standard way to access metadata
    - Ensure metadata quality and security
- **Implementation principles of a Metadata solution depends on the following principles**
    - **Organisational commitment**
        - Senior management support.
        - Metadata management  is an enterprise program
    - **Strategy**
        - how metadata will be created, maintained, integrated and accessed.
        - Metadata strategy must align with business priorities
    - **Enterprise perspective**
        - Ensure future extensibility but implement iteratively and incrementally
    - **Socialisation**
        - communicate the necessity and purpose of each type of metadata
    - **Access**
        - Ensure staff members know how to access and use metadata
    - **Quality**
        - Process owners accountable for quality of metadata produced
    - **Audit**
        - Set, enforce and audit standards for metadata
    - **Improvement**
        - Feedback mechanism for consumers

## 1.3 Essential Concepts

### 1.3.1 Metadata vs. Data

<aside>
💡 Organisations should define metadata requirements and what they need it for. What is data and what is metadata, depends on the organisation
Metadata is the *Who, What, Where, Why, When* and *How* of data

</aside>

### 1.3.2 Types of metadata

![Screenshot 2024-06-18 at 17.22.28.png](Chapter%2012%20Metadata%20Management%20b9eb59d06358474a8ab93dd279fa5229/Screenshot_2024-06-18_at_17.22.28.png)

- **Business metadata**:
    
    <aside>
    💡 focus on the content and condition of data, and includes details related to data governance.
    
    </aside>
    
    - Examples:
        - Definitions and descriptions of data sets
        - Business rules, transformation rules, calculations
        - Data models
        - Data quality rules
        - Update schedules
        - Provenance and data lineage
        - Data standards
        - Stakeholder contact details
        - Security/privacy level
        - Data usage notes
- **Technical Metadata**:
    
    <aside>
    💡 Provides information about **technical details of data**, systems that **store it** and the processes that **move it**.
    
    </aside>
    
    - Examples
        - Physical database table and column names
        - Column properties
        - Database object properties
        - Access permissions
        - Data CRUD rules
        - Physical data models
        - Relationships between data models and physical assets
        - ETL job details
- **Operational Metadata**:
    
    <aside>
    💡 Describes **details of the processing and accessing of data**. created during the **Use and Enhance phases** of the Data Lifecycle
    
    </aside>
    
    - examples
        - Logs of job execution of batch jobs
        - History of extracts and results
        - Error logs
        - Schedule anomalies
        - Results of audit, balance, control measurements
        - Reports and query access patterns, frequency, and execution time
        - Patches and Version maintenance plan and execution, current patching level
        - Backup, retention, date created, disaster recovery provisions
        - SLA requirements and provisions
        - Volumetric and usage patterns
        - Data archiving and retention rules, related archives
        - Data sharing rules and agreements
        - Purge criteria
        - Technical roles and responsibilities
- **Process Metadata**
    - examples
        - data store & Data Involved
        - Government / regulatory Bodies
        - roles & responsabilities
        - Process dependencies and de composition

### 1.3.3 ISO / IEC Metadata registry standard

<aside>
💡 ISO /IEC 11179 is structured in 6 parts

</aside>

- Part 1: Framework for the generation and standardisation of Data Elements
- Part 3: Basic Attributes of Data Elements
- Part 4: Rules and Guidelines for the Formulation of Data Elements
- Part 5: Naming and Identification Principles for Data Elements
- Part 6: Registration of Data Elements

### 1.3.4 Metadata for Unstructured Data

- **Types of metadata for unstructured data** (stored with the document)
    - **Descriptive:** Catalogue information and thesauri keywords
    - **Structural:** Tags, field structures, format, terms on the Business Glossary
    - **Administrative:** Sources, update schedules, access rights, navigation information
    - **Bibliographic:** Library catalogue entries
    - **Record keeping Metadata:** Retention policies
    - **Preservation Metadata:** Storage, archival condition, rules for conservation, e-discovery, **focused on documents**

### 1.3.5 Sources of Metadata

- **Application Metadata Repositories**
    - the physical tables where the metadata is stored
- **Business glossary**
    - A document of the organisation’s business concepts and terminology, definitions and the relationships between those terms. accounts for hardware, software, database processes and different user roles and responsabilities:
        - **Business users:** Data analysts, research analysts, management to understand terminology
        - **Data Stewards:** Manage the lifecycle of terms and definitions
        - **Technical users:** Use glossary terms to make design decisions
    - Business glossary should capture business terms attributes such as:
        - Term name, definition
        - Ownership and stewardship
        - 🚨**not from the book**
            - Term name, definition, acronym or abbreviation, and any synonyms
            - Business unit and or application responsible for managing the data associated with the terminology
            - Name of the person identifying the term, and date updated
            - Categorization or taxonomy association for the term (business functional association)
            - Conflicting definitions that need resolution, nature of the problem, action timeline
            - Common misunderstandings in terms
            - Algorithms supporting definitions
            - Lineage
            - Official or authoritative source for the data supporting the term
- **Business Intelligence (BI) Tools:**
    - Overview information, classes, objects, derived and calculated items
- **Configuration Management Tools or Databases:**
    - CMDB manage Metadata related to IT assets. Each asset is a Configuration Item (CI)
- **Data Dictionaries:**
    - Defines the contents and structure of data sets. This Metadata is embedded in database/modelling tools, and must be extracted to use
    - can be used to manage the names, descriptions, structure, characteristics, storage requirements, default values and other attributes of every data element
- **Data Integration Tools:**
    - Lineage Metadata, movement of data
- **Database Management and System Catalogues:**
    - Describe the content, sizing information, software version, deployment status, network and infrastructure uptime, availability etc.
    - database tables names, column names and indexes
- **Data Mapping Management Tools:**
    - Mapping tools and data integration tools can exchange data with Metadata repositories
- **Data Quality Tools:**
    - Can share quality scores and patterns with Metadata repositories
- **Directories and Catalogues:**
    - Contains information about systems, sources and locations of data in the organisation. It is useful for developers and super users
- **Event Messaging Tools:**
    - Require a lot of Metadata to move messages between diverse systems
- **Modelling Tools and Repositories:**
    - Produce Metadata relevant to the design of the application or system model
- **Service Registries:**
    - Technical information about services and service end points e.g., APIs
- **Other Metadata Stores:**
    - Specialised lists, repositories of repositories and business rules
- **database catalog**
    - best place to find database table name, column names, and indexes

### 1.3.6 Types of Metadata Architecture

<aside>
💡 all metadata management solutions include architectural layers which correspond to points in the metadata lifecycle:

- Metadata Creation and sourcing
- Metadata storage in one or more repositories
- Metadata integration: bring together metadata from various repositories
- Metadata delivery: Formats for delivery to another system
- Metadata usage: Searching
- Metadata control and management
</aside>

- **Centralised Metadata Architecture**
    
    <aside>
    💡
    
    A single metadata repository containing copies of Metadata from the various sources
    
    </aside>
    
    ![Screenshot 2024-06-19 at 08.33.26.png](Chapter%2012%20Metadata%20Management%20b9eb59d06358474a8ab93dd279fa5229/Screenshot_2024-06-19_at_08.33.26.png)
    
    | Advantages of a centralised repository | Limitations of a centralised repository |
    | --- | --- |
    | High availability: independent of source systems | Complex processes to ensure changes to source metadata are quickly replicated into the repository |
    | Quick retrieval as repository and query reside together | Maintenance can be costly |
    | Resolved database structure not affected by proprietary | Extraction may require custom modules or middleware |
    | Quality is improved as extracted Metadata may be enhanced with metadata from else where | Increased demands on IT and vendor staff to maintain customised code |
- **Distributed Metadata Architecture**
    
    <aside>
    💡 No persistent repository, 
    The portal passes user requests to the appropriate tool to execute. 
    The Metadata retrieval engine retrieves data from source systems in real time. 
    The Metadata management environment maintains source system catalogs and lookup information.
    
    </aside>
    
    ![Screenshot 2024-06-19 at 08.33.43.png](Chapter%2012%20Metadata%20Management%20b9eb59d06358474a8ab93dd279fa5229/Screenshot_2024-06-19_at_08.33.43.png)
    
    | Advantages of the distributed Metadata architecture | Limitations of distributed architecture |
    | --- | --- |
    | Metadata is current and valid as it is retrieved from the source | Not able to support user-added metadata entries as there is no repository to put them |
    | queries are distributed - improved process and response time | standardisation of persisting metadata from various systems |
    | Implementation and maintenance effort minimised as Metadata requests from proprietary systems are queries, so no understanding of proprietary data structures is required | query capabilities depend on the availability of the source systems |
    | Automated metadata query processing is simpler | quality of metadata depends on the source systems |
    | reduced batch processing |  |
- **Hybrid Metadata Architecture**
    
    <aside>
    💡 Combines the Centralised and Distributed. The repository design only accounts for the user-added Metadata, critical standardised items and the additions from manual sources. Near real-time retrieval of Metadata from source and enhanced Metadata when needed.
    
    </aside>
    
    ![Screenshot 2024-06-19 at 08.34.55.png](Chapter%2012%20Metadata%20Management%20b9eb59d06358474a8ab93dd279fa5229/Screenshot_2024-06-19_at_08.34.55.png)
    
- **Bi-Direccional Metadata Architecture**
    
    <aside>
    💡 Allows Metadata to change in any part of the architecture and then feedback is coordinated from the repository to the original source. The repository is forced to contain the latest version of the Metadata source, and must manage changes to the source as well.
    
    </aside>
    

# 2. Activities

## 2.1 Define metadata strategy

- **Define the future state enterprise Metadata architecture and the implementation phases:**
    - **Initiate Metadata strategy planning:** Key stakeholders involved in planning
        - Short- and long-term goals
        - Charter, scope, objectives and communications plan
    - **Conduct key stakeholder interviews:** To provide foundational knowledge
    - **Assess existing Metadata sources and information architecture:** Assess difficulty of project
        - Interview IT staff
        - Review system architecture and model documentation
    - **Develop future Metadata architecture:** Develop long term architecture for the managed Metadata environment
    - **Develop a phased implementation plan:** Prioritise findings from the interviews and data analyses to define a phased implementation plan

## 2.2 Understand Metadata Requirements

- **What Metadata is needed and at what level. functionallity focussed requirements:**
    - **Volatillity**: update frequency
    - **Synchronisation:** Timing of updates in relation to source changes
    - **History:** Do historical versions need to be retained?
    - **Access rights:** Who, how and interface functionality
    - **Structure:** Metadata model for storage
    - **Integration:** Degree of and rules for integration
    - **Maintenance:** Processes and rules for updating
    - **Management:** Roles and responsibilities
    - **Quality:** Metadata quality requirement
    - **Security:** Some Metadata cannot be exposed as it will reveal sensitive data

## 2.3 Define Metadata Architecture

<aside>
💡 Metadata management system must be able to extract metadata from **multiples sources** by scanning the sources and updating the repository, while supporting manual updates, searches and lookups by various user groups. single access point for the metadata repository which is transparent to users

</aside>

<aside>
💡 integrating multiples source system difficulties are determining a valid link or equivalences between data elements

</aside>

### 2.3.1 Create MetaModel

- **Data model for the metadata repository**
    - High-level conceptual model – relationships between systems
    - Lower level metamodel that describes the elements and processes
    - The metamodel is a planning tool, and Metadata itself
    
    ![Screenshot 2024-06-19 at 08.47.39.png](Chapter%2012%20Metadata%20Management%20b9eb59d06358474a8ab93dd279fa5229/Screenshot_2024-06-19_at_08.47.39.png)
    

### 2.3.2 Apply metadata standards

- **Governance monitors for compliance**
    - international initiative established a Metadata Standard
        - Internal standards such as naming conventions (ISO 11179 for naming conventions - BASEL II)
    - External standards such as data exchange formats
    - Industry Metadata Standards essential
        - EDI

### 2.3.3 Manage Metadata Stores

- **Control activities should have governance oversight and include:**
    - Job scheduling and monitoring
    - load statistical analysis
    - back up, recovery, archive, purging
    - configuration modification
    - performance tuning
    - query statistics analysis
    - query and report generation
    - security management
- **quality control activities**
    - QA, quality control
    - Matching update sets to timeframes
    - Missing Metadata reports
- **Metadata management activities**
    - Loading, scanning, importing and tagging assets
    - Source mapping and movement
    - Versioning
    - User interface management
    - Linking data sets Metadata maintenance – for NoSQL provisioning
    - Linking data sets to internal data acquisition – custom links and job Metadata
    - Licensing for external data sources and feeds
    - Data enhancement Metadata e.g., Link to GIS
- **Training**
    - Education and training of users and data stewards
    - Management metrics generation and analysis
    - Training on the control activities and query and reporting

## 2.4 Create and Maintain Metadata

<aside>
💡 metadata should be planned and created as a product. Profile and inspect for quality. Schedule maintenance

</aside>

- General principles for Metadata Management:
    - **Accountability:** Metadata is often produced through existing processes – hold those process owners accountable for quality of Metadata
    - **Standards:** Set, enforce and audit Metadata standards
    - **Improvement:** Create a consumer feedback mechanism

### 2.4.1 Integrate Metadata

<aside>
💡 As Metadata is gathered from many sources, and integrated into the metadata repository, challenges arise which require governance

</aside>

- **Two approaches for repository scanning**
    - **Proprietary interface:** Collection and loading of Metadata occurs in single step. No format specific file output
    - **Semi-proprietary interface:** Two step process where scanner collects Metadata from a source and outputs it to a format specific data file

### 2.4.2 Distribute and Deliver Metadata

- Metadata is delivered to consumers/applications/tools requiring metadata feeds
    - Metadata intranet websites
    - Reports, glossaries and other documents
    - Data warehouses, data marts and BI tools
    - Modelling and software development tools
    - Messaging and transactions
    - Web services and APIs
    - External organisation interface solutions

<aside>
💡 Metadata is exchanged with external organisations using files (XLM, JSON..) or web services

</aside>

## 2.5 Query, Report and Analyse Metadata

<aside>
💡 A Metadata repository has a front-end application for search and retrieval as Metadata guides the use of data assets.

</aside>

# 3. Tools

<aside>
💡 The Metadata repository is the primary tool used to manage Metadata. It has an integration layer and an interface for manual updates. Metadata repository management tools are also a source of Metadata.

</aside>

# 4. Techniques

## 4.1 Data Lineage and impact Analysis

<aside>
💡 Metadata about the physical assets provides information about how the data is transformed as it moves between systems. Limited to the scope of the metadata management system

</aside>

- **As Implemented Lineage**:
    - Current version of lineage based on programming code
    - Imported from various tools
- **As Designed Lineage**:
    - Lineage described in mapping specification documents
    - Not extractable by Metadata management system
- **Stitching**: The process whereby the Metadata management system augments the ‘As Implemented’ data lineage with the ‘As Designed’
    
    ![Screenshot 2024-06-19 at 11.07.01.png](Chapter%2012%20Metadata%20Management%20b9eb59d06358474a8ab93dd279fa5229/Screenshot_2024-06-19_at_11.07.01.png)
    
    ![Screenshot 2024-06-19 at 11.07.17.png](Chapter%2012%20Metadata%20Management%20b9eb59d06358474a8ab93dd279fa5229/Screenshot_2024-06-19_at_11.07.17.png)
    
- Successful lineage discovery needs to account for both business and technical focus:
    - **Business focus:** Data elements prioritised by business
        - Start at target and trace back to source
        - Gives business understanding what happens to a data element as it moves
        - DQ measurements with lineage can pinpoint where system design impacts quality
    - **Technical focus:**
        - Start at source systems
        - Identify immediate consumers, then next sets of consumers until all systems are identified

## 4.2 Metadata for big data ingest

<aside>
💡 Metadata tags should be applied to data on ingestion to the data lake. Ingestion engines can profile data as it is ingested to identify data domains, relationships and DQ issues. PPI and sensitive data can be tagged, as well as codes and confidence tags for data science.

</aside>

# 5. Implementations Guidelines

<aside>
💡 Implement the Metadata environment in incremental steps to minimise risks and facilitate acceptance. Use a relational database platform. Contents should be generic in design and should be integrated so that consumers can see across different data sources. Should house current, planned and historical versions of Metadata.

</aside>

## 5.1 Readiness assessment

- People should be aware of the risks of not managing Metadata:
    - Errors in judgement due to lack of knowledge of the context of data
    - Exposure of sensitive data
    - Risk that SMEs will leave and take their knowledge of the data with them
- A formal assessment of the current maturity of Metadata activities includes:
    - Critical data elements
    - Available Metadata glossaries
    - Lineage
    - Data profiling and data quality processes
    - MDM maturity

## 5.2 Organisational and cultural change

<aside>
💡 Metadata efforts often meet with resistance. Needs senior management support and engagement. Business and technical staff work closely in a cross-functional manner.

</aside>

# 6. Metadata Governance

<aside>
💡 Determine the specific requirements for the management of the Metadata lifecycle, and establish governance processes. Formal roles and responsibilities need to be assigned to dedicated resources.

</aside>

## 6.1 **Process Controls**

- Governance team responsible for:
    - Defining standards
    - Managing status changes for Metadata
    - Promotion of Metadata
    - Training
    - Management of business terms

<aside>
💡 Metadata strategy should be integrated into the SDLC to ensure Metadata is collected and remains current.

</aside>

## 6.2 Documentation of Metadata solutions

A master catalogue of Metadata of the sources and targets currently on scope. It is a ‘what-is-where’ guide for the user community and includes:

- Metadata implementation status
- Source and target Metadata store
- Schedule information for updates
- Retention and versions kept
- Contents
- Quality statements or warnings
- System of record or other data source statuses
- Tools, architecture and people involved
- Sensitive information and removal or masking for the source

## 6.3 Metadata Standards and Guidelines

- Metadata standards are required in the exchange of data with operational trading partners.
    - Use industry-based Metadata standards early
    - Industry metadata == consensus metadata
    - Tool vendors provide XML, JSON or REST support to exchange their data
    - Tools offer import/export capabilities using XML
    - Templates and examples
    - ISO standards

## 6.4 Metrics

- **Metadata repository completeness:** Ideal coverage compared to actual coverage
- **Metadata Management Maturity:** Based on the Capability Maturity Model (CMM-DMM) assessment approach
- **Steward representation:** Coverage across enterprise for stewardship
- **Metadata usage:** User uptake measured in logins
- **Business Glossary activity:** Usage, update, resolution of definitions, coverage
- **Metadata documentation quality:** Assess automatically and manually
- **Metadata repository availability:** Uptime, processing time (batch and query)