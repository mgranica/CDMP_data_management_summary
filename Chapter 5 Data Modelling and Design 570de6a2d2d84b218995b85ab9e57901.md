# Chapter 5: Data Modelling and Design

# 1. Introduction

<aside>
💡 Data Modeling is the process of **discovering, analysing, and scoping** data requirements, and then representing them and communicating these data requirements in a precise form called the data model. This process is iterative and involves **conceptual, logical and physical models**.

</aside>

- **Most commonly used schemas to represent data:**
    - Relational
    - Dimensional
    - Object-Oriented
    - Fact-Based
    - Time-Based
    - NoSQL
- **Levels of detail**
    - Conceptual: CDM
    - Logical: LDM
    - Physical: PDM
- **Models Components**
    - entities
    - relationships
    - attributes
    - facts
    - keys

<aside>
💡 Data models comprise and contain **Metadata uncovered** during the modelling process which is essential to other data management functions. **Data models are an important form of metadata**

</aside>

(2024, revised version):

![image.png](Chapter%205%20Data%20Modelling%20and%20Design%20570de6a2d2d84b218995b85ab9e57901/image.png)

- (Original version diagram)
    
    ![Screenshot 2024-06-04 at 14.52.29.png](Chapter%205%20Data%20Modelling%20and%20Design%20570de6a2d2d84b218995b85ab9e57901/Screenshot_2024-06-04_at_14.52.29.png)
    

## 1.1 Data models Business Drivers

Data models do:

- Provide common vocabulary around data
- Capture and document explicit knowledge about the organisation’s data and system
- Serve as primary communication tool during projects
- Provide the starting point for customization, integration or replacement of an application

## 1.2 Goals And Principles

<aside>
💡 The goal of data modelling is to confirm and document an **understanding of different perspectives**, which leads to applications that more closely **align with current and future business requirements**, and creates a **foundation to successfully complete broad-scoped initiatives** such as master data management and data governance

</aside>

**Confirming and documenting understanding from different perspectives facilitates:**

- **Formalisation**
    - A concise **definition of data structures and relationships**, how data is affected by implemented business rules.
    - A disciplined structure reduces the occurrences of data anomalies
- **Scope definition**
    - Explain boundaries for data context in packages, projects or existing systems
- **Knowledge retention/documentation**
    - Preserves corporate memory regarding a system by capturing knowledge in an explicit form.
    - Documentation for future projects. Understand the implications of modifications. Data models are reusable maps

## 1.3 Essential concepts

### 1.3.1 Data Modeling and Data Models

Data modelling is most frequently performed in the context of systems development and maintenance efforts, known as the system development lifecycle (SDLC).

<aside>
💡 A data model is the representation/simplification/abstraction (set of entities, relationships, attributes, and domains; often built as a diagram with a graphical representation) of an organisation’s data as it is understood or as it is expected to be. Data models are the main medium to communicate data requirements from business to IT and within it.

</aside>

### 1.3.2 Types of data that are modeled

- **Category Information**:
    - Data used to classify and define things (customers classified by market segment or products classified by color)
- **Resource Information**:
    - Master and Reference Data:
        - objects needed to conduct operational processes such as Product, Customer, Supplier, Facility, Organization, and Account, Countries, Currencies
- **Business Event Information**:
    - Transaction Data created while operational processes are in progress.
    - Examples include Customer Orders, Supplier Invoices, Cash Withdrawal, and Business Meetings
- **Detail Transaction Information**:
    - POS, Social Media, Clickstream, IoT event.
    - Large volume and rapidly changing. Usually referred to as Big Data. Internet of Things – sensors etc.

### 1.3.3 Data Model Components

**1.3.3.1** Entity

<aside>
💡 An entity is a thing that exists separate from other things; within data modelling, an entity is a thing about which an organisation collects information.

</aside>

| Category | Definition | Examples |
| --- | --- | --- |
| Who | Person or organization of interest. That is, *Who* is
important to the business? Often a ‘who’ is associated
with a party generalization, or role such as Customer or
Vendor. Persons or organizations can have multiple
roles or be included in multiple parties. | Employee, Patient, Player, Suspect,
Customer, Vendor, Student,
Passenger, Competitor, Author |
| What | Product or service of interest to the enterprise. It often
refers to what the organization makes or what service it
provides. That is, What is important to the business?
Attributes for categories, types, etc. are very important
here. | Product, Service, Raw Material,
Finished Good, Course, Song,
Photograph, Book |
| When | Calendar or time interval of interest to the enterprise.
That is, When is the business in operation? | Time, Date, Month, Quarter, Year,
Calendar, Semester, Fiscal Period,
Minute, Departure Time |
| Where | Location of interest to the enterprise. Location can refer
to actual places as well as electronic places. That is,
Where is business conducted? | Mailing Address, Distribution
Point, Website URL, IP Address |
| Why | Event or transaction of interest to the enterprise. These
events keep the business afloat. That is, Why is the
business in business? | Order, Return, Complaint,
Withdrawal, Deposit, Compliment,
Inquiry, Trade, Claim |
| How | Documentation of the event of interest to the enterprise.
Documents provide the evidence that the events
occurred, such as a Purchase Order recording an Order
event. That is, How do we know that an event occurred? | Invoice, Contract, Agreement,
Account, Purchase Order, Speeding
Ticket, Packing Slip, Trade
Confirmation |
| Measurement | Counts, sums, etc. of the other categories (what, where)
at or over points in time (when). | Sales, Item Count, Payments,
Balance |

<aside>
💡 An **entity instance** is a particular occurrence of an **entity (type).**

</aside>

![Screenshot 2024-06-04 at 15.37.45.png](Chapter%205%20Data%20Modelling%20and%20Design%20570de6a2d2d84b218995b85ab9e57901/Screenshot_2024-06-04_at_15.37.45.png)

<aside>
💡 Definition of entities: (Important as they are core metadata). Definitions clarify the meaning of business vocabulary and provide rigor to the business rules governing entity relationships

</aside>

entities are represented graphically by **rectangles**

![Screenshot 2024-06-27 at 12.54.00.png](Chapter%205%20Data%20Modelling%20and%20Design%20570de6a2d2d84b218995b85ab9e57901/Screenshot_2024-06-27_at_12.54.00.png)

- **Clarity:** Easy to read and grasp
- **Accuracy:** Precise and correct description of the entity
- **Completeness**: All parts of the definition are present. The scope of uniqueness is in the definition. e.g., examples of code values for a code entity

**1.3.3.2 Relationships**

<aside>
💡 Association between entities

</aside>

- aliases based on scheme:
    - **Dimensional**: Navigation path
    - **NoSQL**: Edge (graph database) or Link (Anchor Modelling)
    - **Relational on the physical level**: Constraint or Reference

**relationships graphical representation**

![Screenshot 2024-06-04 at 15.58.56.png](Chapter%205%20Data%20Modelling%20and%20Design%20570de6a2d2d84b218995b85ab9e57901/Screenshot_2024-06-04_at_15.58.56.png)

![Screenshot 2024-06-04 at 16.01.49.png](Chapter%205%20Data%20Modelling%20and%20Design%20570de6a2d2d84b218995b85ab9e57901/Screenshot_2024-06-04_at_16.01.49.png)

<aside>
💡 Relationship cardinality: Data rules on how entities are connected are enforced. An instance of an entity may have a relationship with 0, 1 or many instances of another entity

</aside>

**Arity of relationships**

<aside>
💡 **Cardinality** captures how many entity instances participate in the relationship, and 
**arity** captures how many entities participate in the relationship

</aside>

- **Unary (Recursive or self-referencing) relationship:**
    - This is a **nonidentifying**, nonmandatory relationship in which the same entity is both the parent and the child. There is only one entity.
    - **A Foreign Key is used to distinguish between the roles or instances**.
        
        ![Screenshot 2024-06-04 at 16.05.57.png](Chapter%205%20Data%20Modelling%20and%20Design%20570de6a2d2d84b218995b85ab9e57901/Screenshot_2024-06-04_at_16.05.57.png)
        
    - **Hierarchy**
        - **One to many recursive relationship.**
        - **child entity has at most one parent**
        
        ![Screenshot 2024-06-04 at 16.13.26.png](Chapter%205%20Data%20Modelling%20and%20Design%20570de6a2d2d84b218995b85ab9e57901/Screenshot_2024-06-04_at_16.13.26.png)
        
    - **Network**
        - Many to many recursive relationship.
        - Entity instance can have more than one parent
        
        ![Screenshot 2024-06-04 at 16.14.41.png](Chapter%205%20Data%20Modelling%20and%20Design%20570de6a2d2d84b218995b85ab9e57901/Screenshot_2024-06-04_at_16.14.41.png)
        
- **Binary Relationship: 2 entities**
    
    ![Screenshot 2024-06-04 at 16.16.44.png](Chapter%205%20Data%20Modelling%20and%20Design%20570de6a2d2d84b218995b85ab9e57901/Screenshot_2024-06-04_at_16.16.44.png)
    
- **Ternary Relationship**
    - used in **Fact Based Modelling** for ontologies
    
    ![Screenshot 2024-06-04 at 16.17.18.png](Chapter%205%20Data%20Modelling%20and%20Design%20570de6a2d2d84b218995b85ab9e57901/Screenshot_2024-06-04_at_16.17.18.png)
    

**Foreign Key**

<aside>
💡 Used in logical an physical data models to represent a relationship

</aside>

![Screenshot 2024-06-27 at 12.57.53.png](Chapter%205%20Data%20Modelling%20and%20Design%20570de6a2d2d84b218995b85ab9e57901/Screenshot_2024-06-27_at_12.57.53.png)

**Attribute**

- property that identifies, describes or measures an entity
- column in a table. may have domains
- Graphical representation of attributes: a list within the entity rectangle

![Screenshot 2024-06-27 at 12.58.12.png](Chapter%205%20Data%20Modelling%20and%20Design%20570de6a2d2d84b218995b85ab9e57901/Screenshot_2024-06-27_at_12.58.12.png)

**Identifiers KEY**

<aside>
💡 Set of one or more attributes that uniquely identifies and instance of an entity

</aside>

- Types of keys
    - Construction-type keys:
        - **Simple**:
            - One attribute e.g., Vehicles Identification Number
        - **Surrogate:**
            - Unique identifier, often a counter and always system generated, without intelligence and not visible to end users
        - **Compound:**
            - A set of ****2 or more attributes together uniquely identify and entity instance e.g. *areacode+exchange+localnumber=phone number IssuerID+AccountID+Check digit = Credit card number*
            - Each attribute is FK as for an associative entity or the PK on a Fact Table
                - describes a many-to-many relationship
            - Come from different tables
        - **Composite:**
            - One compound key and at least one other simple or compound key or non-key attribute.
            - key on a multidimensional fact table: which may contain several compound keys, simple keys, and optionally a load timestamp.
            - 2 or more attributes that identify an entity occurrence
    - function type keys:
        - **Super Key**:
            - any set of attributes that uniquely identify an instance
        - **Candidate key**:
            - Minimal set of attributes (simple or compound) that uniquely identifies an entity instance. Also called **Business** or **Natural** keys
        - **Primary** **key**:
            - The candidate key chosen to be the unique identifier. Often a surrogate key
        - **Alternate key**:
            - Unique candidate key, but not chosen for primary. Usually a business key. Note: Alternate keys enforce the Data Quality dimension Uniqueness)
    - Identifying vs non-identifying relationships
        
        <aside>
        💡 In the student example shown in Figure 38, **Student** and **Course** are independent entities and **Registration** is a dependent entity.
        
        </aside>
        
        ![Screenshot 2024-06-27 at 13.03.40.png](Chapter%205%20Data%20Modelling%20and%20Design%20570de6a2d2d84b218995b85ab9e57901/Screenshot_2024-06-27_at_13.03.40.png)
        
        - **Independent Entity**:
            - Primary key contains only attributes belonging to that entity
            - Non-identifying (weak) relationship ---------
            - FK non-primary key attribute
        - **Dependent Entity:**
            
            <aside>
            💡 Dependent entities have at least one identifying relationship. An identifying relationship is one where the primary key of the parent (the entity on the one side of the relationship) is migrated as a foreign key to the
            child’s primary key,
            
            </aside>
            
            - The primary key contains at least one attribute from another entity
            - Rectangles with rounded corners
            - Identifying (strong) relationship ______
- **Domain**
    
    <aside>
    💡 A domain is a complete set of possible values that an attribute can be assigned. it is used to standardise the characteristics of the attributes
    
    </aside>
    
    - Domains can be restricted by adding constraints. constraints can relate format and/or logic
    - Defining domains:
        - **Data type:** Standard type of data in an attribute assigned to that domain
        - **Data Format:** Domains using templates and character limitations
        - **List:** Finite set of values
        - **Range:** Values of same data type between max and min values or can be open ended
        - **Rule-based**: e.g., Compare values to a calculated value

### 1.3.4 Data Modelling Schemes and Notations

| Scheme | Sample Notations |
| --- | --- |
| Relational | Information engineering IE
Integration Definition for Information Modeling (IDEFIX)
Barker Notation
Chen |
| Dimensional | Dimensional |
| Object-Oriented | Unified Modeling Language UML |
| Fact-Based | Object Role Modeling ORM
Fully communication Oriented Modeling FCO-IM |
| Time-Based | Data Vault
Anchor Modeling |
| NoSQL | Document
Column
Graph
Key-Value |

![Screenshot 2024-06-04 at 17.02.54.png](Chapter%205%20Data%20Modelling%20and%20Design%20570de6a2d2d84b218995b85ab9e57901/Screenshot_2024-06-04_at_17.02.54.png)

- **Relational**
    
    <aside>
    💡 Dr Edgar F. Codd (1970) proposed that data could be managed most effectively in terms of two dimensional relations, reducing redundancy and data storage. This approach was based on the mathematics of set theory. (Note: DMBOK erroneously refers to Dr Codd as Edward)
    
    </aside>
    
    ![Screenshot 2024-06-27 at 13.09.18.png](Chapter%205%20Data%20Modelling%20and%20Design%20570de6a2d2d84b218995b85ab9e57901/Screenshot_2024-06-27_at_13.09.18.png)
    
    - **Relationships captures business rules**
        - Exact expression of business data, and have one fact in one place (removal of redundancy ).
        - Ideal for operational systems requireing quick data entry, individuals transaction processing and accurate storage
        
        ![Screenshot 2024-06-04 at 17.05.01.png](Chapter%205%20Data%20Modelling%20and%20Design%20570de6a2d2d84b218995b85ab9e57901/Screenshot_2024-06-04_at_17.05.01.png)
        
- **Dimensional**
    
    <aside>
    💡 General Mills and Dartmouth College in the 1960s. Data is structured to optimise query and analysis of large amounts of data. Batch processing.
    
    </aside>
    
    - **Dimensional models capture business questions**
        - Focused on a particular business process. Relationships capture **navigation paths** to answer the business question
        
        ![Screenshot 2024-07-03 at 15.31.04.png](Chapter%205%20Data%20Modelling%20and%20Design%20570de6a2d2d84b218995b85ab9e57901/Screenshot_2024-07-03_at_15.31.04.png)
        
        - **Fact Tables:**
            - The measurement, result of calculations or algorithms
            - Numeric
            - Metadata is critical for proper understanding and usage
            - **Fact tables consist of a large number of rows and few columns**
            - Takes up approximately **90% of space in dimensional databases**
        - **Dimension Tables:**
            - Mostly textual
            - Used for querying
            - **Highly denormalised** (Note: Correct term is flattened. Normalisation is a Relational term)
            - **have many columns but few rows**
            - Must have a unique identifier for each row
            - **Slowly Changing Dimensions** (SCDs) manage changes of attributes based on the rate and type of change:
                - **Overwrite (Type 1):** New value overwrites the old value in place
                - **New Row (Type 2):** New values written a new row, old row marked as not current
                - **New Column (Type 3):** Multiple instances of a value are listed in columns in the same row
        - **Snowflaking:**
            - Normalising the star schema (Note: This process is not relational normalisation, but rather the separation of levels in the dimension)
        - **Grain:**
            - The most detail a row in the fact table can have
        - **Conformed Dimensions:**
            - Built with the entire organisation in mind and shared across dimensional models
        - **Conformed Facts:**
            - Use standardised definitions of terms across marts
        - measures
            - are found in fact tables
            - quantitative columnnumerical format ≠ all numeric columns are measures
            - can not alway be added across all the dimensions
- **Object Oriented UML**
    
    <aside>
    💡 Unified Modeling Language class model is used for object oriented databases. Specifies classes (entity types) and their relationship types
    
    </aside>
    
    ![Screenshot 2024-06-04 at 17.08.53.png](Chapter%205%20Data%20Modelling%20and%20Design%20570de6a2d2d84b218995b85ab9e57901/Screenshot_2024-06-04_at_17.08.53.png)
    
- **Fact-Based Modeling**
    
    <aside>
    💡 Based on the analysis of natural verbalisation in the business domain
    
    </aside>
    
    - **Object Role Modelling ORM**
        - Model driven engineering approach which verbalises required information at a conceptual level in a controlled and unambiguous natural language
        
        ![Screenshot 2024-06-04 at 17.16.08.png](Chapter%205%20Data%20Modelling%20and%20Design%20570de6a2d2d84b218995b85ab9e57901/Screenshot_2024-06-04_at_17.16.08.png)
        
    - **Fully Communication Oriented Modeling FCO-IM**
    
    ![Screenshot 2024-06-04 at 17.16.52.png](Chapter%205%20Data%20Modelling%20and%20Design%20570de6a2d2d84b218995b85ab9e57901/Screenshot_2024-06-04_at_17.16.52.png)
    
- **Time Based**
    
    <aside>
    💡 Time-based patterns are used when data values must be in chronological order and with time values. Used for data warehouses in a RDBMS environment.
    
    </aside>
    
    - **Data Vault**:
        - Detail oriented, time-based, normalised tables that support one or more functional areas of the business.
        - Between 3NF and Star schema to meet needs of enterprise data warehouses
        - 3 types of entities:
            - **Hubs**: the primary key
            - **Links**: provide transaction integration between hubs
            - **Satellites**: provide the context of the hub primary key
                
                ![Screenshot 2024-06-04 at 17.18.11.png](Chapter%205%20Data%20Modelling%20and%20Design%20570de6a2d2d84b218995b85ab9e57901/Screenshot_2024-06-04_at_17.18.11.png)
                
    - **Anchor Modelling**:
        - **Graphical notation** for information that changes over time in both structure and content.
        - Similar to traditional data modelling but with extensions for temporal data.
        - **4 basic concepts**:
            - **Anchors**: model entities and events
            - **Attributes**: model properties of anchors
            - **Ties**: model the relationship between anchors
            - **Knots**: model shared properties such as states
                
                ![Screenshot 2024-06-04 at 17.19.11.png](Chapter%205%20Data%20Modelling%20and%20Design%20570de6a2d2d84b218995b85ab9e57901/Screenshot_2024-06-04_at_17.19.11.png)
                
                <aside>
                💡 Student, Course and Attendance are anchors, the gray diamonds represent ties, and the circles represent attributes
                
                </aside>
                
- **NoSQL**
    
    <aside>
    💡 NoSQL is the name for databases built on non-relational technology. There are four types of NoSQL databases:
    
    </aside>
    
    - **Document:**
        - Store the business subject in one structure called a document
        - For example, instead of storing Student, Course, and Registration information in three distinct relational structures, properties from all three will exist in a **single document** called Registration
    - **Key-value:**
        - Key-value databases allow an application to store its data in only two columns (‘key’ and ‘value’)
        - Value column can store anything (such as simple information, unformatted text, images, audio, and video)
    - **Column-oriented:**
        - RDBMSs work with a predefined structure and simple data types, such as amounts and dates, whereas column-oriented databases, such as Cassandra, can work with more complex data types including unformatted text and imagery
        - Store each column in its own structure
    - **Graph**:
        - o A graph database is designed for data whose relations are well represented as a set of nodes with an undetermined number of connections between these nodes

### 1.3.5 Data Model Levels of Detail

- **Conceptual** – "Real world" view of the enterprise modelled in the database
- **External** – Subsets of the enterprise model which represent the data requirements in a specific usage context, independent of technology. **Usually maps to Logical**
- **Internal** – Internal or machine view. Describes the stored representation of the enterprise’s data. **(Physical)**

**Conceptual CDM**

<aside>
💡 The conceptual data model captures the high-level data requirements as a collection of related concepts. Basic Business entities and the relationships between them (business rules) are described

</aside>

![Screenshot 2024-06-04 at 17.22.19.png](Chapter%205%20Data%20Modelling%20and%20Design%20570de6a2d2d84b218995b85ab9e57901/Screenshot_2024-06-04_at_17.22.19.png)

**Logical LDM**

<aside>
💡 A detailed, technology independent representation in a specific usage context. An extension of conceptual model. Attributes are assigned by applying normalisation.

</aside>

- In a relational logical data model, the conceptual data model is extended by adding attributes.

![Screenshot 2024-06-04 at 17.23.35.png](Chapter%205%20Data%20Modelling%20and%20Design%20570de6a2d2d84b218995b85ab9e57901/Screenshot_2024-06-04_at_17.23.35.png)

**Physical PDM**

<aside>
💡 Detailed technical solution using the logical data model. Built for a particular technology of DBMS. responsability of the DB administrator

</aside>

- Often using the logical data model as a starting point and then adapted to work within a set of hardware, software, and network tools
    
    ![Screenshot 2024-06-27 at 13.24.58.png](Chapter%205%20Data%20Modelling%20and%20Design%20570de6a2d2d84b218995b85ab9e57901/Screenshot_2024-06-27_at_13.24.58.png)
    
- A **Canonical Model**
    - is a type of physical data model
    - describes the structure of data moving between systems.
    - Structures should be generic and reusable.
    - Used in the Enterprise Service Bus or Enterprise Application Integration (EAI).
- **Views**
    - are virtual tables used to simplify data access,
    - control data access and rename columns without redundancy and loss of referential integrity due to denormalisation.
- **Partitioning:**
    - Process of splitting a table to improve performance
    - **Vertically split**:
        - create subset tables that contain subsets of columns
    - **Horizontally split**:
        - a value in a column is a delimiter to create subset tables
        - create subset tables using the value of a column as the differentiator
- **Denormalisation:**
    - Deliberate transformation of normalised logical model entities into physical tables with redundant data structures
    - Done to improve performance
    - Called Embedding in Document databases, and Collapsing or Combining in Dimensional databases.

### 1.3.6 Normalisation

<aside>
💡 Is the process of applying **rules to organise business complexity** **into stables data structures**. The basic goal is to eliminate redundancy by keeping each attribute in only one place. Requires understanding of attribute’s relationship to its primary key

</aside>

- Normalisation levels:
    - **First normal form (1NF)**:
        - Valid primary key. Each attribute depends on key.
        - Eliminate repeating groups and ensure each attribute is atomic and not multi valued.
    - **Second normal form (2NF)**:
        - Each entity has the minimal primary key and each attribute depends on the complete primary key
    - **Third normal form (3NF)**:
        - no hidden primary keys.
        - Each attribute depends on no attributes outside the key (“the key, the whole key and nothing but the key”)
    - **Boyce / Codd normal form (BCNF)**:
        - Resolves overlapping composite candidate keys (hidden business rules)
    - **Fourth normal form (4NF)**:
        - Resolves all many to many relationships in pairs until they can’t be broken down into smaller pieces
    - **Fifth normal form (5NF)**:
        - Resolves inter-entity dependencies into basic pairs, and all join dependencies use parts of primary keys

### 1.3.7 Abstraction

<aside>
💡 Abstraction is the removal of details in such a way as to broaden applicability to a wide class of situations while preserving the important properties

</aside>

- **Generalisation**:
    - Groups common attributes and relationships into **supertype** entities
- **Specialisation**:
    - Separates distinguishing attributes within an entity into **subtype** entities
        - Subtypes can also be created using **roles** or  **classification** e.g., Party with subtypes Individual and Organisation
        
        ![Screenshot 2024-06-05 at 09.02.26.png](Chapter%205%20Data%20Modelling%20and%20Design%20570de6a2d2d84b218995b85ab9e57901/Screenshot_2024-06-05_at_09.02.26.png)
        
        - The *subtyping relationship* implies that all of the properties from the supertype are inherited by the subtype. In
        - the relational example, **University** and **High School** are subtypes of **School**.

# 2. Activities

## 2.1 Plan for data Modelling

- **Tasks to plan for**
    - Evaluating organisational requirements
    - Creating standards
    - Determining data model storage
- **Deliverable of the modelling process**
    - **Diagram:** The visual that captures the requirements in precise form. Depicts:
        - **Level of detail:** Conceptual, logical or physical
        - **Scheme:** Relational, Dimensional, Object-oriented, Fact-based, Time-based or NoSQL
        - **Notation:** information engineering, unified modelling language, object role modelling
    - **Definitions** for entities, attributes and relationships are essential for precision
    - **Issues and outstanding questions:** Document current issues
    - **Lineage**: Where the data comes from
        - A source/target mapping: Can see source system attributes and how they populate target system attributes
        - Trace components from conceptual to logical to physical
        - Data modeller obtains a good understanding of data requirements and can determine the source attributes
        - Source attributes can be used to check accuracy of the model and mapping

## 2.2 Build the Data Model

<aside>
💡 Modelling is an iterative process: Draft the model then go back to business analysts for clarification, update the model then ask more questions. This increase the precision of the model

</aside>

![Screenshot 2024-06-05 at 10.07.51.png](Chapter%205%20Data%20Modelling%20and%20Design%20570de6a2d2d84b218995b85ab9e57901/Screenshot_2024-06-05_at_10.07.51.png)

**Modelling involves**

- studying previous analysis
- existing data models & databases

### 2.2.1 Forward Engineering

- Build a new application beginning with the requirements.
    - CDM: Understand the scope and key terminology
    - LDM: Documents the business solution
    - PDM: Documents the technical solution
- **Conceptual Data Modeling**
    - steps to create a CDM
        - **Select scheme:** Relational, dimensional, fact-based or NoSQL
        - **Select notation:** Appropriate notation for selected scheme
        - **Complete initial CDM:** Capture the viewpoint of the user group
            - Collect the highest-level concepts (nouns)
            - Collect the activities (verbs) that connect these concepts. Relationships can go both ways or involve more than two concepts
        - **Incorporate enterprise terminology:** Ensure consistency with enterprise terminology and rules
        - **Obtain signoff:** Reviewed for data modelling best practices, and that it meets requirements
- **Logical Data Modelling**
    
    <aside>
    💡 LDM captures the data requirements within the scope of the CDM
    
    </aside>
    
    - **Analyse information requirements:**
        - Elicitation, organisation, documentation, review, refinement approval and change control of business requirements
    - **Analyse existing documentation:**
        - Pre-existing artefacts provide a jump start for new model
    - **Add associative entities:**
        - Used to describe the many-to-many relationships
    - **Add attributes:**
        - Should be atomic
    - **Assign domains:**
        - Allow for consistency of value sets and format
    - **Assign keys:**
        - Identify primary and alternate keys
    - **Normalise**
- **Physical Data Modelling**
    
    <aside>
    💡 LDM must be modified to perform well within storage applications
    
    </aside>
    
    - **Resolve logical abstractions:**
        - Subtypes and supertypes become separate entities
    - **Add attribute details:**
        - Technical names, physical domain, physical data types and length of fields as well as constraints such as NOT NULL
    - **Add Reference Data objects:**
        - Small Reference Data value sets
    - **Assign surrogate keys:**
        - Unique key values not visible to business
    - **Denormalise for performance:**
        - The performance benefit of adding redundancy outweighs the cost
    - **Index for performance:**
        - optimise query performance. Prevents every row being read (table scan)
    - **Partition for performance:**
        - Partition on a date key is usually recommended
    - **Create views:**
        - Requirements driven.
        - Control access to certain data elements or embed joins or filters

### 2.2.3 Reverse Engineering

<aside>
💡 The process of documenting an existing database

</aside>

- PDM: First to understand the technical design
- LDM: To document the business solution met by the system
- CDM: document the scope and key terminology

### 2.3 Review the Data Model

<aside>
💡 Apply a data quality verifier such as Steve Hoberman’s Data Model Scorecard ® for quality control.

</aside>

### 2.4 Maintain the Data Models

<aside>
💡 The data models need to be kept current. Update when business requirements or processes change. Compare physical with logical regularly.

</aside>

# 3. Tools

- **Data Modelling Tools:**
    - May support forward engineering from conceptual to logical to physical including DDL - **Data Definition Language** generation
    - **Rubber-banding** is the automatic redrawing of relationship lines when an entity is moved
    - Most support reverse engineering from database to CDM
    - Some support naming standards and metadata storage
- **Lineage Tools:**
    - Capture and maintenance of source structures for each attribute in the data model
    - Excel is most commonly used
- **Data Profiling Tools:**
    - Explores data content and validates it according to metadata and identifies data quality gaps/deficiencies
- **Metadata Repositories:**
    - Store descriptive data about the model, including diagram and definitions
    - Enable sharing
- **Data Model Patterns:**
    - Reusable modelling structures
- **Industry Data Models:**
    - Pre-built for an entire industry
    - Needs to be customised

# 4. Best Practices

<aside>
💡 DataBase Administrator takes primary responsibility for the detailed physical database design

</aside>

## 4.1 Best Practices in name convention

- **ISO 11179 Metadata Registry** is an international standard for representing Metadata, consists of sections related to data standards such as naming attributes and definitions
- Data architects, data analysts and database administrators jointly develop standards for an organisation, to complement related IT standards
- Names should be unique and descriptive
- Logical names must be meaningful to business users
- Physical names must conform to DBMS restrictions

## 4.2 Best Practices in Database Design

Design principles for the DBA (PRISM):

- **Performance and ease of use:** Quick and easy access
- **Reusability:** Multiple applications can use the data
- **Integrity:** Data should always have valid business meaning and value
- **Security:** Only available to authorised users
- **Maintainability:** Ensure data work yields value, and the cost of creating, storing, maintaining, using and disposing of data does not exceed its value to the organisation

# 5 Data Model Governance

## 5.1 Data Model and Design Quality Management

Data models and database designs should be a reasonable balance between the short term needs and the long term needs of the enterprise.

### 5.1.1 Develop Data Modelling and Design Standards

<aside>
💡 **Data modelling and database design standards** help **meet business data requirements**, conform to Enterprise and Data Architecture, and ensure data quality.

</aside>

- Standards should include the following:
    - List and description of standards data modelling and database design deliverables
    - List of standard names, abbreviations and abbreviation rules
    - List of standard naming formats for all data model objects
    - List and description of standard methods of creating and maintaining these objects
    - List and description of data modelling and database design roles and responsibilities
    - List and description of all Metadata properties captured in data modelling and database design
    - Metadata quality expectations and requirements
    - Too use guidelines
    - Guidelines for preparing and leading design reviews
    - Guidelines for versioning models
    - Practices that are discouraged

### 5.1.2 Review Data Model and Database Design Quality

- **Requirements Reviews:** Project team conducts this review
    - Starting model if there is one
    - Changes made to the model
    - Options considered and rejected
    - How well new model conforms to modelling and architectural standards
- **Design reviews:** Group of diverse subject matter experts
    - Chair meeting with an agenda to maintain order and move forward
    - Participants are given required documentation and chair solicits input
    - Summarise group’s consensus finding
    - If there is no approval:
        - Modeller reworks
        - Final say should be given by the owner of the system

### 5.1.3 Manage Data Model Versioning and Integration

- Preserve the lineage of changes:
    - **Why** the project or situation required the change
    - **What** and **how** the object changed
    - **When** the change was approved and made to the model
    - **Who** made the change
    - **Where** the change was made (which model)

Modelling tools may have a repository which provides versioning and integration, else preserve models on DDL(Data Definition Language) exports or XML files in a standard source code management system.

## 5.2 Data Modelling Metrics

<aside>
💡 Steve Hoberman’s Data Model Scorecard® provides a way to measure the quality of a data model and identifies specific areas for improvement.

</aside>

![Screenshot 2024-06-05 at 10.07.14.png](Chapter%205%20Data%20Modelling%20and%20Design%20570de6a2d2d84b218995b85ab9e57901/Screenshot_2024-06-05_at_10.07.14.png)

Description of each category:

1. **How well does the model capture the requirements?** 
    1. The model supports all required queries for example.
2. **How complete is the model?** 
    1. Completeness of requirements and completeness of Metadata, nothing extra, nothing missing.
3. **How well does the model match its scheme?** 
    1. Level of detail (conceptual, logical or physical) and the scheme (Relational, dimensional, NoSQL etc.) matches the definition of the type of model being reviewed.
4. **How structurally sound is the model?** 
    1. Validate the design practices to ensure a database can be built.
5. **How well does the model leverage generic structures?** 
    1. Appropriate level of abstraction.
6. **How well does the model follow naming standards?** 
    1. Ensure correct and consistent naming standards have been applied to the model.
7. **How well has the model been arranged for readability?** 
    1. Parent entities above child, groupings and shorter relationship lines improve readability.
8. **How good are the definitions?** 
    1. Clear, complete and accurate.
9. **How consistent is the model with the enterprise?** 
    1. If and Enterprise Data Model exists.
10. **How well does the Metadata match the data?** 
    1. Confirm the actual data to be stored fits in the model.