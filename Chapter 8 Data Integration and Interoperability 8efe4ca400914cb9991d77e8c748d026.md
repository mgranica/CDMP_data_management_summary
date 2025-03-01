# Chapter 8: Data Integration and Interoperability

# 1. Introduction

<aside>
💡 **DII** describes processes relating to the movement and consolidation of data within and between data stores, applications and organisations. 
**Data integration** consolidates data into consistent forms. 
**Data interoperability** is the ability for multiples systems to communicate.

</aside>

- **DII provides**
    - Data migration and conversion
    - Data consolidation into hubs or marts
    - Integration of vendor packages into organisation
    - Data sharing across applications or organisations
    - Distributing data across data stores and data centers
    - Archiving data
    - Managing data interfaces
    - Obtaining and ingesting external data
    - Integrating structured and unstructured data
    - Providing operational intelligence and management decision support
- **DII depend on these areas of data management**
    - **Data governance**
        - The transformation rules and message structures
    - **Data architecture**
        - Design solutions
    - **Data security**
        - Ensuring solutions protect the security of data
    - **Metadata**
        - Tracking technical inventory of data (persistent, virtual and in motion)
        - Business meaning of data
        - Business rules of transforming data
        - Operational history and lineage of the data
    - **Data storage and operations**
        - Managing the physical instantiation of the solutions
    - **Data modelling and design**
        - Design the physical and virtual data structures, and messages passing information between applications and organisations

<aside>
💡 DII is critically important to **Data warehousing and business intelligence** as well as **reference data and master data management**

</aside>

![Screenshot 2024-06-10 at 13.58.21.png](Chapter%208%20Data%20Integration%20and%20Interoperability%208efe4ca400914cb9991d77e8c748d026/Screenshot_2024-06-10_at_13.58.21.png)

## 1.1 Business Drivers

- the need to manage data movement efficiently
- purchased applications come with its own data stores that must integrate with the other data store in the organisation
- An enterprise view of data integration is more cost effective than point to point solution
- Data hubs such as data warehouse and master data solutions
- managing the cost of support by using standard tools and reducing the complexity of interface management
- DII supports the organisation’s ability to comply with data handling standards and regulations to publish data

## 1.2 Goals and Principles

- **Goals**
    - provide data securely, with regulatory compliance in the format and timeframe needed
    - lower cost and complexity of managing solutions by developing shared models and interfaces
    - identify meaningful events and automatically trigger alerts and actions
    - support business intelligence, analytics, master data management, and operational efficiency efforts
- When implementing DII follow these principles
    - Design should take an enterprise perspective (for future extensibility), but implement iteratively and incrementally
    - balance local data needs with enterprise data needs, including support and maintenance
    - ensuring business accountability for DII design and activity

### 1.3 Essential concepts

<aside>
💡 essential to successful integration of data is to undertand data content and structure

</aside>

- **Essential steps in moving data around**
    - **Extract:** Select required data and extract it from its source, and stage it physically or in memory, determining valid links or equivalences between data elements
    - **Transform: make data compatible with the structure of the target store. may be done in batch or in real time**
        - **Format changes:** Technical format e.g., EBCDIC to ASCII
        - **Structure changes:** e.g., Denormalised to normalised
        - **Semantic conversion:** Conversion of values to maintain consistent semantic representation
        - **De-duping:** If rules require unique values, scan target and remove duplicate rows
        - **Re-ordering:** Change to order of the file data elements to fit a pattern
    - **Load**: Physically store the results of the transformations in the target system
- **ETL**
    
    ![Screenshot 2024-06-10 at 14.14.19.png](Chapter%208%20Data%20Integration%20and%20Interoperability%208efe4ca400914cb9991d77e8c748d026/Screenshot_2024-06-10_at_14.14.19.png)
    
- **ELT**
    
    <aside>
    💡 Used if the target system has more transformation capability. also allows data to be instantiated on the target as raw data
    
    </aside>
    
    ![Screenshot 2024-06-10 at 14.14.52.png](Chapter%208%20Data%20Integration%20and%20Interoperability%208efe4ca400914cb9991d77e8c748d026/Screenshot_2024-06-10_at_14.14.52.png)
    
- **Mapping**
    
    <aside>
    💡 A synonim for transformation, the process of developing a lookup matrix from source to target structures and the result of that process
    
    </aside>
    

### 1.3.2 Latency

<aside>
💡 The time difference between when data is generated in the source system and when it is available in the target system. Can be high (batch), low (event driven) to very-low(real-time sybchronous).

</aside>

- **Batch:** Data moving in clumps or files periodically. ****Called a **batch** or **ETL**
    - **Snapshot:** Full set of data at a point in time
    - **Delta:** Data that has changed values since the last time data was sent
    - High latency
    - Used for data conversions, migrations, archiving and extracting from and loading data warehouses and marts
- **Change data capture:**
    - filter data to include only data that has changed in a given timeframe (the delta) and passes it on to data consumers
    - data integration approach that updates a data warehouse. with small changes from operational systems
- **Near-real-time and event driven**:
    - Data is processed in smaller sets spread across the day, or when an event such as an update occurs. Lower latency than batch
- **Asyncronous:**
    - The source does not wait for the target to acknowledge before continuing processing. the target need not be available
- **Real time, synchronous:**
    - no time delay or other differences between source and target are acceptable. the executing process waits for confirmation before executing its transaction
- **Low latency or streaming:**
    - Extra hardware cost. need extremely fast transfer of large amounts of data over large distances

### 1.3.3 Replication

<aside>
💡 Applications maintain exact copies of data sets on multiple physical locations. Better response times for international users. Use DBMS replication utilities. Not recommended if changes to the data occur at more than one site.

</aside>

### 1.3.4 Archiving

<aside>
💡 ETL functions can transport and possibly transform infrequently used data to a cheaper storage solution.

</aside>

### 1.3.5 Enterprise Message Format / Canonical Model

<aside>
💡 A canonical model is the common model used by an organisation to standardise the format in which data will be shared.
Transformations need only be done to and from the canonical model

</aside>

- Hub-and-spoke
- All systems interact with central information hub
- Data is transformed based on the enterprise message format of the organisation
- Reduces transformations as each system only needs to transform data to and from the central canonical model
- Reduces complexity of DII in the enterprise
- Lowers cost of support
- Complex to develop
- Justified in managing more than 3 systems and critical for more than 100

### 1.3.6 Interaction Models

<aside>
💡 Describe ways to make connections between systems:

</aside>

- **Point-to-point**
    - systems pass data directly to each other
    - suitable in small systems
    - can impact processing
    - many interfaces to manage
    - multiple interfaces can lead to inconsistent data
    - used by the vast majority of systems in which data is shared
    - lower latency than hub-and-spoke
- **hub-and-spoke**
    - Consolidates shared data in a central hub
    - Examples are data warehouses, data marts, operational data stores and master data managements hubs
    - easy to add more systems
    - **Enterprise Service Buses** (ESB) - near real time sharing of data where the hub is a virtual canonical model
- **Publisher-suscriber**
    - systems push out data: publish
    - systems pull data in: subscribe
    - interaction method used by DaaS

### 1.3.7 DII architecture concepts

- **Application coupling**
    - **tight coupling**
        - synchronous interface, one waits for the other to respond
    - **loose coupling**
        - preferred interface design as data is passed without waiting for a response and without causing both systems to be unavailable if one is unavailable
            - e.g. Service Oriented Architecture using an Enterprise Service Bus
        
        ![Screenshot 2024-06-10 at 15.45.04.png](Chapter%208%20Data%20Integration%20and%20Interoperability%208efe4ca400914cb9991d77e8c748d026/Screenshot_2024-06-10_at_15.45.04.png)
        
- **Orchestation and Process Control**
    - **Orchestation**: How multiples processes are organised and executed in a system. All systems handling messages must be able to manage the order of those processes
    - **Process Control** The components that ensure, delivery, extraction and loading of data is complete. Include
        - Database activity logs
        - Batch job logs
        - Alerts
        - Exception logs
        - Job dependence charts with remediation options, standard responses
        - Job clock information – length of jobs and computing window time
- **Enterprise Application Integration EAI**
    - Software modules only interacts with each other through APIs
- **Enterprise Service Bus ESB** an intermediary system passing messages between other systems
    
    ![Screenshot 2024-06-10 at 16.03.15.png](Chapter%208%20Data%20Integration%20and%20Interoperability%208efe4ca400914cb9991d77e8c748d026/Screenshot_2024-06-10_at_16.03.15.png)
    
- **Service Oriented Architecture SOA**
    - The functionality of providing data or updating data. is provided through well-defined service calls between applications enabling application independence. Usually implemented through APIs
- **Complex Event Processing (CEP):** Tracks and analyses data about events from multiple sources to predict meaningful events (threats, opportunities) to predict behaviour or automatically trigger a response
- **Data Federation and Virtualisation:** Provides access to a combination of individual data stores. Virtualisation enables distributed databases to be accessed as a single database
- **Data-as-a-Service (DaaS):** Data licensed from a vendor and provided on demand
- **Cloud-based Integration:** Also called Integration Platform-as-a-service (IPaaS) and are usually run as SaaS applications at the data centres of vendors

### 1.3.8 Data Exchange Standards

<aside>
💡 Data Exchange Standards are formal rules for the structure of data elements. ISO ar any common model used by an organisation or data exchange group. It simplifies data interoperability, lowers support costs and increases understanding of the data

</aside>

# 2. Data Integration Activities

<aside>
💡 Data integration activities follow a development lifecycle (plan, design, development, testing and implementation)

</aside>

## 2.1 Plan and Analyse

- Define data integration and lifecycle requirements:
    - Data and technology required to meet business objectives
    - Laws and restrictions on data contents
    - Defined by Business Analysts, data stewards and various architects
    - Creates and uncovers valuable Metadata – manage throughout lifecycle
- Perform Data Discovery:
    - Identify potential sources of data for the integration effort
    - High level assessment of data quality
    - Maintain the inventory of organisational data in a Metadata repository
    - Plan for acquiring and integrating external data
- Document Data Lineage:
    - How data under analysis is acquired or created by the organisation, where it moves, how it is changed, how it is used by the organisation for analytics, decision making or triggering
    - expected to be done during Planning phase??
- Profile Data:
    - Data profiles reveals actual data structure and contents
    - Assess the quality of the data
    - Can reveal differences from what is assumed leading to early intervention
    - Basic profiling involves analysis of:
        - Data format (data structures and inferred from actual data)
        - Data population (NULLS, blanks and defaults)
        - How data values correspond to a set of valid values
        - Patterns and relationships internal to the data set
        - Relationships to other data sets
    - The requirement to profile data must be balanced with an organisation’s privacy and security rules (see Chapter 13)
- Collect Business Rules: rules harvesting or mining
    - **A Business Rule is a statement that defines or constrains and aspect of business processing → define constraints on what can and cannot be done**
    - Four categories:
        - Definition of business terms
        - facts relating terms to each other
        - Constraints or action assertions
        - Derivations
    - Use business rules to support DII to:
        - Assess data in potential source and target data sets
        - Direct the flow of data in the organisation
        - Direct when to automatically trigger events and alerts

## 2.2 Design Data Integration Solutions

### 2.2.1 Design Data integration Architecture

<aside>
💡 DI solutions should be specified at both enterprise and individual solution level. Enterprise standards save time as planning has been done and group licenses and resources sharing and reusing DII components saves money

</aside>

- **Solution architecture indicates**
    - Techniques and Technologies to be used
    - Inventory of involve data structures
    - Orchestation and frequency of data flow
    - Regulatory and security concerns and remediation
    - Operating concerns around backup and recovery
- **Select interaction model**
    - hub-and-spoke, point-to-point or published subscriber

### 2.2.2 Model Data hubs, Interfaces, Messages and Data services

<aside>
💡 Molde persistent and transient datatypes

</aside>

### 2.2.3 Map data Sources to target

<aside>
💡 Specify the rules for transforming data from one location and format to another. for each attribute mapped specify:

</aside>

- technical format and source target → determining valid links or equivalences between data elements
- Transformation required for intermediate staging points
- how each attribute in the final or intermediate data store should be populated
- whether data values need to be transformed
- calculations required

### 2.2.4 Design Data Orchestation

<aside>
💡 Pattern of data flows form start to finish, including intermediate steps

</aside>

- **Batch**: Frequency of data movement and transformation is usually coded into a scheduler
- **Real-time**: Usually triggered by an event such as an update

## 2.3 Develop data Integration Solutions

- **Develop Data Services:** Can be tools or vendor suites
- **Develop data flows:**
    - ETL flows developed in a tool such as a scheduler for batch which manages the order, frequency and dependency of executing the data pieces
    - Real-time: Monitor for events that trigger services to acquire, transform or publish data
- **Develop data migration approach:** Moving data needs proper analysis and testing
- **Develop a publication approach:** Push changed data using common message definitions (canonical model) and notify the recipients
- **Develop complex event processing flows:**
    - Preparing historical data needed for the predictive model
    - Pre-populate predictive model and identify meaningful events
    - Executing triggered action in response to a prediction
- **Maintain DII Metadata:**
    - Manage Metadata uncovered during the development of DII solutions
    - Document all data structures involved
    - ETL vendors have Metadata repositories
    - Service-Oriented Architecture registry

## 2.4 Implementation and Monitoring

- activate the data services that have been developed and tested
- Real-time data processing needs real-time monitoring for issues, human or automated
- Monitor and service at the level of the most demanding target application or consumer

# 3. Tools

- **Data Transformation Engine/ETL Tool:** Primary tool that supports operation and design
- **Data Virtualisation Server:** Perform data extract, transform and integrate virtually. A data warehouse is often input to a data virtualisation server
- **Enterprise Service Bus:** Middleware to support near real-time messaging between heterogeneous sources in the same enterprise
- **Business Rules Engine:** Allows non-technical users to manage business rules implemented by software
- **Data and Process Modelling Tools:** Used to design target and intermediate data structures
- **Data Profiling tool:** Use a tool to analyse large amounts of data to determine if it meets requirements
- **Metadata Repository:** Tools have Metadata repositories which store the rules for transformation, lineage and processing, as well as the instructions for scheduled processes and triggers

# 4. Techniques

<aside>
💡 described in [essential concepts](Chapter%208%20Data%20Integration%20and%20Interoperability%208efe4ca400914cb9991d77e8c748d026.md)

</aside>

# 5. Implementation Guidelines

## 5.1 Readiness Assessment / Risk Assessment

<aside>
💡 as all organisations already have DII in place assess for readiness/risk around tool implementation or interoperability. An enterprise data integration solution supports the movement of data between many applications and organisations

</aside>

- Working DII solutions shouldn’t be replaced. Focus on where none exists. Additional use of data integration adds to the investment in a data warehouse to master data management hub
- It is necessary to sponsor the implementation of an enterprise data integration program by a high level of authority over solution design and technology purchase, to prevent local data integration solutions from developing. It may be perceived the cost of these is less than the enterprise wide solution
- don’t become too focussed on the tool and lose focus on the business needs

## 5.2 Organisation and Cultural Change

- Local teams understand data in their applications
- Central teams know tools and techniques
- Enterprise solutions should be overseen by a Centre of Excellence
- Although technical, data integration solutions must be based on deep business knowledge to successfully deliver value
- Modelling and data analysis should be done by business resources
- Canonical message model (consistent standard for how data is shared in the organisation) development requires technical and business resources
- Business SMEs review transformation mapping design and changes

# 6 DII Governance

- business is responsible for:
    - Decisions about the design of data messages, data models and data transformation rules
    - Defining the rules for loading and transforming data
    - Approve changes to these rules (which are captured as Metadata for cross enterprise analysis)
    - Identifying and verifying predictive models and defining the actions they trigger
- Governance controls to support trust that the DII will perform as promised:
    - Determine what events trigger governance reviews (exceptions or critical events)
    - Map each trigger to reviews that engage with governance bodies
    - Event triggers may be part of SDLC at Stage Gates or part of User Stories

<aside>
💡 Controls come from governance-driven management routines such as mandated review of models, Metadata audits, gating of deliverables or required approval changes to the transformations rules

</aside>

Include real-time operational data integration solutions in SLAs and Business Continuity/Disaster Recovery plans on the same tier as the most critical system to which they provide data.

Policies need to be established to ensure the organisation benefits from an enterprise approach to DII.

## 6.1 Data Sharing Agreements

<aside>
💡 A data sharing agreement or memorandum of understanding MOU must be put in place before developing interfaces, and be approved by business data stewards, which stipulates:

</aside>

- Responsibilities
- Acceptable use of data to be exchanged
- Anticipated use and access to the data
- Restriction on use
- Expected service levels
- Required system up times and response times

## 6.2 DII and Data Linage

Governance to ensure that knowledge of data origins and movement is documented. Data lineage must be managed as it is critical Metadata.

Compliance standards require an organisation be able to describe where its data originated, and how it has changed as it moves through systems.

Impact analysis when making changes to data structures, data flows or data processing requires forward and backward data lineage.

## 6.3 Data integration metrics

To measure scale and benefits of DII solutions:

- Data Availability (of data requested)
- Data volumes and speed
    - Volumes of data transported and transformed
    - Volumes of data analysed
    - Speed of transmission
    - Latency between update and availability
    - Latency between event and triggered action
    - Time to availability of new data sources
- Solution costs and complexity
    - Cost of developing and managing solutions
    - Ease of acquiring new data
    - Complexity of solutions and operations
    - Number of systems using data integration solutions

# 7 . Bonus

- Non value added information
    - the policies are unclear of what is defined as non-value-added, storage is cheap so there is no cost drivers and it takes more effort to dispose that to keep
- What is **not** part of data integration and interoperability
    - Enterprise application integration
    - **Data quality monitoring**
    - integration structured and unstructured data
    - archiving data
    - data consolidation into hubs or marts