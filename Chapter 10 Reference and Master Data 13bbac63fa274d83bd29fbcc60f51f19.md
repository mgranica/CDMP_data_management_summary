# Chapter 10: Reference and Master Data

# 1. Introduction

<aside>
💡 **Reference and Master Data** refers to the reconciliation and integration of data through stewardship and semantic consistency in support of enterprise-wide needs to share its data assets.

</aside>

- An organisation and its customers benefit if the data required across business areas, processes and systems is **shared**. allowing the same customer lists, geographic codes, parts codes etc. to be accessed, to produce a level of consistency
- Systems and data evolve organically, resulting in multiples systems executing similar functions isolated from each other, leading to inconsistencies in data structure and values and increased costs and risks. Both can be reduced through the management of reference data and master data
- (2024, revised version diagram)
    
    ![image.png](Chapter%2010%20Reference%20and%20Master%20Data%2013bbac63fa274d83bd29fbcc60f51f19/image.png)
    
- (original v2 diagram)
    
    ![Screenshot 2024-06-27 at 16.47.32.png](Chapter%2010%20Reference%20and%20Master%20Data%2013bbac63fa274d83bd29fbcc60f51f19/Screenshot_2024-06-27_at_16.47.32.png)
    

## 1.1 Business Drivers

- Master data management program:
    - **Meeting organisational data requirements**: Multiple areas need to access same data sets, which confidence that they are **complete, current and consistent**
    - **Managing data quality**: MDM enables a consistent representation of critical entities
    - **Managing the costs of data integration:** Master Data reduces variation in identification and definition of critical data entities
    - **Reducing risk:** Simplifies the data sharing environment
- Managed Reference Data enables the organisation to:
    - Meet the data requirements for multiples initiatives, reduce costs and risks of data integration
    - Manage quality of Reference data

## 1.2 Goals and Principles

- Goals:
    1. ensuring the organisation has complete, consistent, current, authoritative Master and Reference Data across organisational processes.
    2. enabling MRD to be shared across the enterprise functions and applications
    3. Lowering the cost and reducing the complexity of data usage and integration trhough standards, common data models, and integration processes.
    4. Provide authoritative source of reconciled and quality-assessed master and reference data
    5. lower cost and complexity through use of standards, common data models and integration patterns
- Reference and MDM guiding principles:
    - **Shared data:**
        - Managed to be sharable across organisation
    - **Ownership**:
        - Belong to the organisation. Require high level of stewardship
    - **Quality**:
        - Require ongoing monitoring and governance
    - **Stewardship**:
        - Business data stewards responsible
    - **Controlled Change**:
        - **Master Data**:
            - Represents the best view of currency and accuracy at any point in time. Caution when matching rules that change values. Should be reversible
            - best version of the truth: golden record
            - organisation best understanding of what is accurate and current
        - **Reference Data**:
            - Change follows defined process. Approve and communicate before implementing
            - limited to predefined domain values
    - **Authority**: Master data values should be replicated only from the **system of record**

## 1.3 Essential concepts

### 1.3.1 Differences between Master and Reference data

- Malcolm Chisholm proposed a six layer taxonomy of data 2008
    - Metadata
    - Reference data
    - Enterprise Structure data
    - Transaction Structure data
    - Transaction Activity data
    - Transaction Audit data

<aside>
💡 **Chisholm’s definition of Master Data (within the above taxonomy)** 
an aggregation of: 
- reference data 
- enterprise structure data 
- transaction structure data

</aside>

- **Reference data**
    - Code and description tables used to categorise other data in the organisation,
    - Relates data in the database to information outside the organisation
    - data used to classify or categorise other data
    - **usually has fewer attributes than master data**
- **Enterprise Structure data**
    - Business activity data e.g. chart of accounts
- **Transaction structure data**
    - Describes things that must be present for a transaction to occur .e.g. products, customers, vendors

<aside>
💡 **DAMA Dictionary Definition (2009)**: Master Data is the data that provides the context for business activity data in the form of common and abstract concepts that relate to the activity. 
It includes the details (definition and identifiers) of internal and external objects involved in business transactions, such as customers, products, employees, vendors and controlled domains (code values).

</aside>

<aside>
💡 **David Loshin** describes Master Data objects as core business objects used in different applications across the organisation along with their associated Metadata, attributes, definitions, roles, connections and taxonomies. 
Master Data objects represent those things that matter most to the organisation, that are logged in transaction, reported on, measured and analysed.

</aside>

- Master Data Management works to resolve the differences in associations between data in different systems and processes to consistently identify individual entity instances in different contexts.
- This process must be managed over time so that the identifiers for these Master Data entity instances remain consistent, it includes **sophisticated integration capability**.
    - Shared purposes of Reference and Master Data:
        - Provide context to the creation and use of transactional data
        - Reference data provides context for Master Data
        - Enable data to be meaningfully understood
        - Shared resources managed at the enterprise level
    - Reference Data compared to Master Data sets:
        - Less volatile
        - Fewer columns and rows than Transactional or Master Data sets
        - No entity resolution challenges
- **Different focus on Data management:**
    - **Master Data Management (MDM):**
        - Controls the definition of business entities:
            - Control over Master Data values and identifiers that enable consistent use of the most accurate and timely data about essential business entities.
        - Ensure availability of accurate current values while reducing risks of ambiguity
        - require techniques for splitting or merging an instance of a business entity
    - **Reference Data Management (RDM):**
        - Control over defined domain values and their definitions.
        - Ensure the organisation has access to a complete set of accurate and current values for each concept represented
    
    <aside>
    💡 RDM is responsible for obtaining data and managing updates, as reference data con originate inside or outside the organisation
    
    </aside>
    

### 1.3.2 Reference data

<aside>
💡 **Reference data** is any data used to characterise or classify other data, or to relate data to information external to an organisation (Chisholm, 2001). Can be codes and descriptions or more complex hierarchies and mappings.

</aside>

- Common Storage techniques:
    - Code tables in relational databases linked by foreign keys
    - Reference Data Management systems
    - Object attribute specific Metadata to specify permissible values for APIs or user interface access

<aside>
💡 **Reference Data Management** entails control and maintenance of defined domain values, definitions and the relationships with and across domain values. The goal is to ensure values are consistent, current and accessible to the organisation.

</aside>

- **1.3.2.1 Reference Data structure**

<aside>
💡 depends on the granularity and complexity.

</aside>

- 1.3.2.1.1 Lists

<aside>
💡 code value and description which can be used in a drop down

</aside>

![Screenshot 2024-06-13 at 16.04.39.png](Chapter%2010%20Reference%20and%20Master%20Data%2013bbac63fa274d83bd29fbcc60f51f19/Screenshot_2024-06-13_at_16.04.39.png)

![Screenshot 2024-06-13 at 16.06.01.png](Chapter%2010%20Reference%20and%20Master%20Data%2013bbac63fa274d83bd29fbcc60f51f19/Screenshot_2024-06-13_at_16.06.01.png)

- **1.3.2.1.2 Cross-Reference Lists**

<aside>
💡 Used to translate. code values of the same concept. May be at different granularities or same granularity with different values.

</aside>

![Screenshot 2024-06-27 at 17.07.43.png](Chapter%2010%20Reference%20and%20Master%20Data%2013bbac63fa274d83bd29fbcc60f51f19/Screenshot_2024-06-27_at_17.07.43.png)

- **1.3.2.1.3 Taxonomies**

<aside>
💡 Taxonomic reference data structures capture information at different levels of specificity support multifaceted navigation required by business intelligence

- Taxonomies enable content classification and multi-faceted navigation to support Business Intelligence.
- Taxonomic Reference Data can be stored in a recursive relationship
</aside>

![Screenshot 2024-06-13 at 16.24.42.png](Chapter%2010%20Reference%20and%20Master%20Data%2013bbac63fa274d83bd29fbcc60f51f19/Screenshot_2024-06-13_at_16.24.42.png)

- **1.3.2.1.4 Ontologies**

<aside>
💡 Ontologies used to manage web content can be part of Reference Data, as they are used to characterise other data or relate organisational data to information beyond the boundaries of the organisation.

- Ontologies may also be considered Metadata.
</aside>

- **1.3.2.2 Proprietary or internal reference data**
    
    <aside>
    💡 Reference data created within the organisation to support internal systems. 
    RDM consists of managing them and ensuring consistency.
    
    </aside>
    
- **1.3.2.3 Industry Reference data**
    
    <aside>
    💡 Industry Reference Data describes data sets which are created and maintained by industry associations and government bodies in order to provide a standard for codifying important concepts.
    
    </aside>
    
- **1.3.2.4 Geographic or Geo-statistical data**
    
    <aside>
    💡 enables classification or analysis based on geography
    
    </aside>
    
- **1.3.2.5 Computational reference data**
    
    <aside>
    💡 Used for common, consistent calculations. This data may change frequently, such as foreign exchange values.
    
    </aside>
    
- **1.3.2.6 Standard Reference data set Metadata**
    
    <aside>
    💡 Maintain key Metadata about Reference Data sets to ensure their lineage and currency are understood and maintained.
    
    </aside>
    
    ![Screenshot 2024-06-13 at 16.25.03.png](Chapter%2010%20Reference%20and%20Master%20Data%2013bbac63fa274d83bd29fbcc60f51f19/Screenshot_2024-06-13_at_16.25.03.png)
    

### 1.3.3 Master Data

<aside>
💡 Master data is about  **the key business entities** and should represent the **authoritative most accurate data available**, which can be trusted and used with confidence. Business rules dictate the format and allowable values

</aside>

<aside>
💡 Controls the definitions of business entities

</aside>

<aside>
💡 Master data values should represent the organisations best understanding of what is accurate and current

</aside>

- Common organisational Master Data is data about:
    - **Parties:** Individuals, organisations and their roles
    - **Products and services:** Internal and external
    - **Financial structures:** e.g., contracts, general ledger accounts
    - **Locations:** e.g., addresses and GPS coordinates
- **1.3.3.1 System of record, System of reference**
    
    <aside>
    💡 Where there are potentially different versions of the truth. best version of the master data.
    
    </aside>
    
    - need to know more about the data to distinguish between them:
        - **A System of Record** is an authoritative system where data is created/captured and maintained through a defined set of rules and expectations
        - **A System of Reference** is an authoritative system where data consumers can obtain reliable data to support transactions and analysis. Examples are MDM applications, Data Sharing Hubs and Data Warehouses
- **1.3.3.2 Trusted source, golden record**
    - A **Trusted Source** is recognised as the “**best version of the truth**” based on a combination of automated rules and manual stewardship. (Any Master Data Management system)
    - A **Golden Record** represents 100% accurate data about an entity, also referred to as a “single version of the truth”. Not always possible for multiple systems to have one version of the truth as there are usually multiple SOR. Promising data is Golden can be misleading, and can undermine confidence.
- **1.3.3.3 Master data management**
    
    <aside>
    💡 **Gartner’s Definition**: A **technology-enabled discipline** in which business and IT work together to ensure the **uniformity, accuracy, stewardship, semantic consistency** and **accountability** of the enterprise’s official shared Master Data assets. Master Data is the **consistent and uniform set of identifiers and extended** attributes that describes the core entities of the enterprise, including customers, prospects, citizens, suppliers, sites, hierarchies and chart of accounts.
    
    </aside>
    
    - Criteria to assess MDM requirements:
        - Which roles, organisations, places and things are referenced repeatedly
        - What data is used to describe people, places and things
        - How the data is defined, structured, and the granularity
        - Where data is created/sourced, stored, made available and accessed
        - How it changes as it moves through systems
        - Who uses the data, and for what purposes
        - Criteria used to understand the quality and reliability of the data and its sources
    - Planning for Master Data Management within a domain:
        - Identify candidate sources that will provide a comprehensive view of Master Data entities
        - Develop rules for accurately matching and merging entity instances
        - Establish an approach to identify and restore inappropriately matched and merged data
        - Establish an approach to distribute trusted data systems across the enterprise
- **1.3.3.4 Master Data Management key Processing**
    
    ![Screenshot 2024-06-13 at 17.03.10.png](Chapter%2010%20Reference%20and%20Master%20Data%2013bbac63fa274d83bd29fbcc60f51f19/Screenshot_2024-06-13_at_17.03.10.png)
    
    - **Data Model Management:**
        - Clear and consistent definitions make sense to business at the enterprise level
    - **Data Acquisition:**
        
        ![Screenshot 2024-06-27 at 17.22.54.png](Chapter%2010%20Reference%20and%20Master%20Data%2013bbac63fa274d83bd29fbcc60f51f19/Screenshot_2024-06-27_at_17.22.54.png)
        
        - Data representing the same entity can look different. Plan for acquiring new data as a reliable repeatable process.
        - High level cleansing tools, and matching rules, then perform data quality on the new data
    - **Data Validation, Standardisation and Enrichment:**
        
        ![Screenshot 2024-06-27 at 17.23.08.png](Chapter%2010%20Reference%20and%20Master%20Data%2013bbac63fa274d83bd29fbcc60f51f19/Screenshot_2024-06-27_at_17.23.08.png)
        
        - Reduce variation in format and reconcile values:
            - **Validation:** Identify clearly incorrect or defaulted data
            - **Standardisation:** Data conforms to standard Reference Data values and formats
            - **Enrichment:** Add attributes that improve entity resolution services
    - **Entity Resolution and Identifier Management:**
        
        <aside>
        💡 **Entity resolution** is the process of determining whether two references to real world objects refer to the same object or different objects.
        
        </aside>
        
        ![Screenshot 2024-06-27 at 17.23.37.png](Chapter%2010%20Reference%20and%20Master%20Data%2013bbac63fa274d83bd29fbcc60f51f19/Screenshot_2024-06-27_at_17.23.37.png)
        
        - **Activities:**
            - **Matching:** or candidate identification is the process of identifying how different records relate to a single entity. Use similarity analysis to avoid false positives or negatives
                - **Deterministic Algorithms:** Parsing and standardisation rely on patterns
                - **Probabilistic Algorithms:** Rely on statistical techniques
            - **Identity Resolution:**
                - Keep a history of matches so that those less confident matches due to conflicting values can be undone if found to be incorrect
            - **Matching Workflows / Reconciliation Types:**
                - **Duplicate identification match rules:**
                    - Specific set of data elements that uniquely identify an entity and identify merge opportunities
                - **Match-link rules:**
                    - Identify and cross-reference records that appear to relate to the master record without updating the content of the cross-referenced record
                - **Match-merge rules:**
                    - Match records and merge data into a single unified and comprehensive record. Complex
            - **Master Data ID Management:** Two types of identifiers managed in an MDM environment:
                - **Global ID** is the MDM solution assigned unique identifier attached to reconciled records. Should be automatically generated
                - **X-Ref Management** is management of the relationship between source IDs and the Global ID
            - **Affiliation Management:** Establishing and maintaining relationships between Master Data records of entities that have real-world relationships. ****Data Architecture design of the MDM system which kind of relationship to leverage between entities:
                - **Affiliation relationships** are programmed and are the most flexible
                - **Parent-child relationships** have implied hierarchical navigation structure
            - **Data Sharing and Stewardship:** Data Stewards resolve incorrectly matched situations and improve matching algorithms
- **1.3.3.5 Party master data**
    
    <aside>
    💡 Data about individuals, organisations and the role they play in business relationships. examples from differents environments
    
    </aside>
    
    - **Commercial:** Customers, employees, vendors, partners, competitors
    - **Public sector:** Citizens
    - **Law enforcement:** Suspects, witnesses, victims
    - **Not for profit:** Members, donors
    - **Healthcare:** Patients, providers
    - **Education:** Students, faculty
    
    Customer Relationship Management (CRM) systems manage Master Data about customers.
    
    Master Data is challenging for parties playing more than one role in an organisation.
    
- **1.3.3.6 Financial Master data**
    
    <aside>
    💡 Data about business units, cost centres, profit centres, general ledger accounts, budgets, projections and projects. The central hub of financial master data is an enterprise resource planning ERP system
    
    </aside>
    
- **1.3.3.7 Legal master data**
    
    <aside>
    💡 Data about contracts, regulations and other legal matters
    
    </aside>
    
- **1.3.3.8 Product master data**
    
    <aside>
    💡 Can focus on the organisation’s product and services or on industrywide products and services. different types of product master data solutions:
    
    </aside>
    
    - **Product Lifecycle Management (PLM):** Managing the lifecycle of a product/service from conception to disposal
    - **Product Data Management (PDM):** Engineering and manufacturing. Enables secure sharing of product information such as design drawings (CAD)
    - **Product Data in Enterprise Resource Planning (ERP):** SKUs to support order entry to inventory
    - **Product Data in Manufacturing Execution Systems (MES):** Raw inventory to finished goods
    - **Product Data in Customer Relationship Management (CRM):** Marketing, sales and support interactions
- **1.3.3.9 Location Master data**
    
    <aside>
    💡 The ability to track and share geographic information and to create hierarchical relationships based on geographic information
    
    </aside>
    
    - **Location Reference Data** is usually geopolitical data handled by external organisations
    - **Location Master Data** are address related to parties and businesses
- **1.3.3.10 Industry Master data - Reference dictionary**
    
    <aside>
    💡 Authoritative listings of Master Data entries that can be purchased. They can be licensed and can provide a starting point for matching and linking new records.
    
    </aside>
    

- **1.3.4 Data Sharing Architecture**
    
    <aside>
    💡 Each Master Data subject area usually has its own system of record e.g., CRM or ERP systems
    
    </aside>
    
    ![Screenshot 2024-06-13 at 17.19.55.png](Chapter%2010%20Reference%20and%20Master%20Data%2013bbac63fa274d83bd29fbcc60f51f19/Screenshot_2024-06-13_at_17.19.55.png)
    
    - The Master Data hub can handle interactions with spoke items such as source systems, business applications, and data stores while minimizing the number of integration points.
    - three approaches to implement master datahub environment:
        - **Registry**
            - An index that points to Master Data in various systems of record
            - Manage Master Data local to their applications
            - Easy to implement, but complex queries are challenging
            - Multiple business rules need to be implemented
        - **Transaction hub**
            - Applications interface with the hub to access and update Master Data which exists **only** within the Transaction Hub and not in the applications
            - The Hub is the **system of record** for Master Data
            - Better governance and consistency, but costly
            - Business rules are implemented in the Hub
        - **Consolidated approach**
            - Systems of record manage Master Data for their applications
            - It is also consolidated within a common repository (replication)
            - There is no need to access directly from the systems of record
            - There will be latency between the Hub and SOR
    - Types of master data architecture:
        - Hybrid
        - Repository
        - Registry
        - Virtualised

# 2. Activities

## 2.1 MDM Activities

- **Define MDM Drivers and Requirements:**
    - Easier to define requirements for an application than the whole enterprise
    - Prioritise Master Data efforts on cost benefit of the proposed improvements
    - Start with simplest category to learn from the process
- **Evaluate and Assess Data Sources**
    - Understand the structure of existing data and how it is collected or created
    - Understand the quality of the data, as poor quality data complicates a Master Data project
    - Assess disparity between sources
    - May be able to purchase standardised data such as Reference Directories
- **Define Architectural Approach:**
    - Depends on business strategy, the platforms for existing sources and the lineage and volatility of the data
- **Model Master Data:**
    - As Master Data is an integration process, model data within subject areas. A logical or canonical model
- **Define Stewardship and Maintenance Processes:**
    - Technical solutions still require the oversight of Data Stewards to address records that fall out of the process and why
- **Establish Governance Policies to enforce use of Master Data:**
    - The benefits come once people start using the Master Data

## 2.2 Reference Data Activities

- **Define Drivers and Requirements:**
    - **Drivers:** Operational efficiency and higher data quality
    - **Requirements:** Driven by the most important Reference Data sets
- **Evaluate and Assess Data Sources:**
    - **External:**
        - Vendor that guarantees updates on a schedule and ensures quality data
    - **Internal:**
        - Owners should understand the benefits of central management of their data sets
- **Define Architectural Approach:**
    - Tool should allow for manual updates
- **Model Reference Data sets:**
    - Models are Metadata which helps consumers understand the relationships within the Reference Data sets, and the data quality rules
- **Define Stewardship and Maintenance Processes:**
    - Capture Metadata about reference data sets
- **Establish Reference Data Governance Policies:**
    - Govern quality and mandate use of RD

# 3. Tools and Techniques

- MDM requires identity management enabled tools:
    - Data integration tools
    - Data remediation tools
    - Operational data stores (ODS)
    - Data sharing hubs (DSH)
    - Specialised MDM applications

# 4. Implementation Guidelines

## 4.1 Adhere to master data architecture

- The integration process should take into account:
    - The organisational structure of the business
    - The number of distinct systems of record
    - The data governance implementation
    - The importance of access and latency of data values
    - The number of consuming systems and applications

## 4.2 Monitor data movement

- Monitor data as it flows within the Reference or Master Data sharing environment to:
    - Show how data is used across the organisation
    - Identify data lineage from/to administrative systems and applications
    - Assist root cause analysis of issues
    - Show effectiveness of data ingestion and consumption integration techniques
    - Denote latency of data values from source systems through consumption
    - Determine validity of business rules and transformations executed within integration components

## 4.3 Manage reference data change

<aside>
💡 Reference Data is a shared resource, therefore it should not be locally controlled, but channels to receive and respond to change requests must be provided according to policies and procedures put in place by the Governance Council.

</aside>

- Planned/scheduled changes such as periodic updates to industry codes require less governance than ad hoc changes.

## 4.4 Data sharing agreements

<aside>
💡 Data sharing agreements stipulate what data can be shared and under what conditions. Helps when issues regarding quality of data brought in or availability arise. Driven by the Data Governance program and involves Data Architects, Data Providers, Data Stewards, Application Developers, Business Analysts, Compliance/Privacy Officers and Security Officers.

</aside>

- SLAs should be in place so that the quality data can be provided to downstream consumers.

# 5. Organisation and cultural change

<aside>
💡 It is not easy for people to relinquish control of their data to create shared resources. People may perceive MDM and RDM efforts as adding complications to their processes.

</aside>

- The most challenging cultural change is determining which individuals are accountable for which decisions.

# 6. Reference and Master Data Governance

- Because they are shared resources, Reference and Master Data require governance and stewardship.
- Governance processes will determine:
    - The data sources to be integrated
    - Data quality rules to be enforced
    - Conditions of use rules
    - Activities to be monitored and the frequency of monitoring
    - Priority and response levels of stewardship efforts
    - How information is represented to meet stakeholder needs
    - Standard approval gates, expectations in RDM and MDM deployment

Governance processes bring compliance and legal stakeholders together with information consumers to ensure risks are mitigated through definition and incorporation of privacy, security and retention policies.

Data Governance must have the ability to review, receive and consider new requirements and changes. Make principles, rules and guidelines available to all using Reference and Master Data.

<aside>
💡 Consumer of master data management can also be referred to as a Subscriber

</aside>

## 6.1 Metrics

- **Data quality and compliance:** DQ dashboards
- **Data change activity:**
    - Metrics denote rate of change of data values
    - Provide insight to systems providing data to sharing environment
    - Used to tune algorithms in MDM process
- **Data ingestion and consumption:** Denote and track data contributing systems and what business areas are subscribing to shared data
- **Service Level Agreements:** Level of adherence to SLAs provides insight to data and technical problems
- **Data Steward coverage:** Used to identify gaps in support
- **Total cost of ownership:** Must be consistently applied across the organisation to be effective
- **Data sharing volume and usage:** The volume and velocity of data defined, ingested and subscribed to and from the data sharing environment