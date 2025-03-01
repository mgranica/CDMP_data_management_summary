# Chapter 9: Document and Content management

# 1. Introduction

<aside>
💡 Document & Content Management entails controlling the capture, storage, access and use of data and information **stored outside relational databases.** Records include both paper documents and ESI (Electronically stored information). Ensuring security and quality requires governance, reliable architecture and well-managed metadata.

</aside>

- (2024, revised version Diagram)
    
    ![image.png](Chapter%209%20Document%20and%20Content%20management%2022856610d32d4ab1a3102ebb5ffa2c5e/image.png)
    
- (Original Version Diagram)
    
    ![Screenshot 2024-06-11 at 15.18.09.png](Chapter%209%20Document%20and%20Content%20management%2022856610d32d4ab1a3102ebb5ffa2c5e/Screenshot_2024-06-11_at_15.18.09.png)
    

## 1.1 Business drivers

- **Regulatory compliance** (audits and recording)
- **The ability to respond to litigation:** Respond efficiently and consistently
- **e-discovery:** The process of finding electronic records that might serve as evidence in litigation. Includes email, chats, websites, raw application data and Metadata. Huge volume of ESI. Proactive management is essential
- **Business continuity requirements**
- **Efficiency**: Use technology to streamline processes, manage workflow, eliminate repetitive manual tasks and enable collaboration
- **Customer satisfaction**: Well organised and searchable websites

## 1.2 Goals & Principles

- Goals of implementing best practices around Document and Content management:
    - ensuring effective and efficient retrieval and use of data in unstructured formats
    - Ensuring integration capability between structured and unstructured data
    - Complying with legal obligations and customer expectations
- Management of document and content follow these guideline principles:
    - everyone in the organisation must create, use, retrieve and dispose of records in accordance with the established policies and procedures. Train everyone
    - Experts in handling of records and content should be fully engaged in policy and planning
    - in 2009, ARMA International published GARP (Generally Acepted Recordkeeping Principles) how business records must be maintained: details on ARMA website
        - **Principles of accountability:**
            - Senior executive assigns appropriate individuals, adopts policies and processes and ensures auditability
        - **Principles of integrity**
            - Guarantee of authenticity and reliability
        - **Principle of Protection:**
            - Personal information is protected
        - **Principle of Compliance:**
            - Program should comply with laws, binding authorities and the policies of the organisation
        - **Principle of Availability:**
            - Information is managed in a manner that ensures timely, efficient and accurate retrieval of information
        - **Principle of Retention:**
            - Retain information for an appropriate time taking legal and regulatory requirements into consideration
        - **Principle of Disposition:**
            - Provide secure and appropriate disposition of information in accordance with operational, legal, regulatory and fiscal requirements
        - **Principle of Transparency:**
            - Policies, processes, activities, governance program documented and understood by all staff and appropriate interested parties

## 1.3 Essential Concepts

### 1.3.1 Content

<aside>
💡 Document is to content what a bucket is to water: container or file. **Content** refers to data and information inside the file, document or website. Content has a lifecycle and can become an official record. Official record are treated differently to other content

</aside>

- **Content Management**
    - The processes, techniques and technologies for organising, categorising and structuring information resources so that they can be stored, published and reused
    - Important in websites
    - Indexing based on keywords from taxonomies
    - Enterprise Content Management (ECM) for entire enterprise
- **Content Metadata:** Essential for managing unstructured data and “big data”
    - **Format:** Often dictates the method to access the data
    - **Search-ability:** Whether search tools already exist
    - **Self-documentation:** Whether the ****Metadata self-documenting as in file systems
    - **Existing patterns:** Whether existing methods can be adopted or adapted
    - **Content subjects:** The things people are likely to be looking for
    - **Requirements:** Need for thoroughness and detail in retrieval means a content tagging tool is necessary
- **Content Modelling:** The process of converting logical content concepts into content types, attributes and data types with relationships using metadata management and data modelling techniques. two levels of content modelling:
    - Information product level e.g., creating a website
    - Component level with detail the elements in the information product
- **Content Delivery Methods:** Convert to XML to enable reuse over many channels. Types of delivery systems:
    - **Push:** Users choose type of content to be delivered to news channels and providers on a schedule
    - **Pull:** Users pull content through the Internet
    - **Interactive:** e.g., Electronic point of sale. High volumes of real-time data. Options include EAI, CDC, Data Integration and EII

### 1.3.2 Controlled Vocabularies

<aside>
💡 A defined list of explicitly allowed terms to index, categorise, tag, sort and retrieve content through browsing and sorting, and to systematically organise content. Controlled vocabularies should be aligned with the entity names and definitions in the Enterprise Conceptual Model. May be considered **Reference Data** and **Metadata**

</aside>

- **Vocabulary Management:** The function of defining, sourcing, importing and maintaining any given vocabulary.
    - ANSI/NISO Z39.19-2005 definition:
        - Way to improve the effectiveness of information storage and retrieval systems, web navigation systems and other environments that seek to both identify and locate desired content via a description using language
    - Purpose of vocabulary control is consistency in the description of content objects to facilitate retrieval
- **Vocabulary Views and Micro-Controlled Vocabulary:**
    - A **vocabulary view**
        - a subset of a large standard vocabulary relevant to a group of users e.g., Finance only needs financial terms
    - A **micro-controlled vocabulary**
        - vocabulary view containing highly specialised terms not present in the general vocabulary
- **Term and Pick Lists:**
    - Lists in applications that do not contain relationships, such as menus or drop-downs. They control the domain of values
- **Term Management:**
    - One or more words designating a concept (ANSI/NISO Z39.19-2005). Terms should be specified and managed through governance processes. Three types of term relationships:
        - **Equivalent term relationship:**
            - Leads to one or more terms to use
        - **Hierarchical relationship:**
            - Depicts broader (general) to narrower (specific) or whole-part relationships
        - **Related term relationship:**
            - A term that is associatively but not hierarchically linked to another term in a controlled vocabulary
- **Synonym rings and Authority lists:**
    - **Synonym ring:**
        - A set of terms with roughly equivalent meaning. A search on one reveals content on the others
    - **Authority list:**
        - A controlled vocabulary of descriptive terms designed to facilitate retrieval of information within a specific domain.
        - Terms have different authority levels, some are preferred, and some are variants. Must have a designated manager
- **Taxonomies:**
    - Any classification or controlled vocabulary.
    - A naming structure containing a controlled vocabulary used for outlining topics and enabling navigation and search systems.
    - Can be a data model. i.e. the Dewey decimal System for libraries
        - **Flat taxonomy:**
            - No relationships among the set of controlled categories. A list
        - **Hierarchical taxonomy:**
            - Tree structure where nodes are related by a rule. Going up expands the category and going down refines.
        - **Polyhierarchy:**
            - Tree structure with more than one rule. Multiple parents. Paths are complex
        - **Facet taxonomy:**
            - Star structure. Each node is associated to a central node e.g., Metadata where each attribute is a facet of a content object
        - **Network taxonomy:**
            - Both hierarchical and facet structures, e.g., a thesaurus
- **Classification Schemes and Tagging:**
    - Classification schemes are codes that represent controlled vocabulary, e.g., Dewey Decimal System for libraries
    - **Folksonomy:**
        - For online content and terms and names are obtained though social tagging
- **Thesauri:**
    - A Thesaurus is a controlled vocabulary used for content retrieval. Provides information about each term and its relationship to other terms
- **Ontology:**
    - A type of taxonomy that represents a set of concepts and their relationships within a domain
    - Semantic Web
    - Developed using ontology languages such as RDFS (Resource Description Framework Schema)
    - Describe classes (concepts), Individuals (instances) attributes, relations and events
    - two **differences** between taxonomy and ontology:
        - **Taxonomy:** Data content classifications for a given concept area
        - **Ontology:** Content concepts are mixed and identified through Metadata
        - **Taxonomy:** Closed-world assumption, only what is known is defined
        - **Ontology:** Open-world assumption, possible relationships are inferred

### 1.3.3 Documents and Records

<aside>
💡 **Documents** are electronic or paper objects which communicate information and knowledge.

**Records** are a subset of documents which provide evidence of actions taken and decisions made in accordance with procedures. Can be created manually or automatically by equipment.

</aside>

- **Document Management:** Processes, techniques and procedures for controlling and organising documents and records throughout their lifecycle
    - **Inventory:** Identification of existing and newly created documents and records
    - **Policy:** Creation, approval and enforcement of documents and records policies
    - **Classification**
    - **Storage:** Short and long term physical storage
    - **Retrieval and circulation:** Allow access in accordance with policies, security and legal standards
    - **Preservation and disposal:** Archiving and destroying documents and records according to organisational needs, statutes and regulations
- **Records Management:**
    - Managing records through the full lifecycle:
        - Record creation or receipt
        - Processing
        - Distribution
        - Organisation
        - Retrieval
        - Disposition
    - Records can be physical, electronic, web content, documents on all kinds of media, data in any kind of database
    - A **Vital Record**: A type of record required by an organisation to resume operations during and after a disaster
    - Trustworthy records have signatures for regulatory compliance and integrity
    - Characteristics of well-prepared records:
        - **Content**: Accurate, complete, truthful
        - **Context:** Collect Metadata
        - **Timeliness:** Created promptly after the event
        - **Permanency:** Records may never be changed
        - **Structure:** Content should be clear and legible
    
    ![Screenshot 2024-06-12 at 10.25.26.png](Chapter%209%20Document%20and%20Content%20management%2022856610d32d4ab1a3102ebb5ffa2c5e/Screenshot_2024-06-12_at_10.25.26.png)
    
- **Digital Asset Management:** Document management for rich media documents (videos, logos, photographs etc.)

### 1.3.4 Data Map

<aside>
💡 A data map is an inventory of all ESI (Electronically Stored Information) data sources, applications and IT environments.

</aside>

### 1.3.5 E-Discovery

<aside>
💡 Discovery is the pre-trial phase of a lawsuit where both parties request information from each other to find the facts of the case. Rules were amended in 2006 to include ESI (Electronically Stored Information). Electronic documents have Metadata which plays a part in evidence.

</aside>

- Legal requirements:
    - e-discovery
    - data and records retention practices
    - Legal hold notification (LHN) process
    - Legally defensible disposition practices

![Screenshot 2024-06-12 at 10.25.52.png](Chapter%209%20Document%20and%20Content%20management%2022856610d32d4ab1a3102ebb5ffa2c5e/Screenshot_2024-06-12_at_10.25.52.png)

### 1.3.6 Information Architecture

<aside>
💡 Information architecture is the process of creating structure for a body of information or content. Identifies links and relationships between documents and content

</aside>

- components:
    - Controlled vocabulary
    - Taxonomies and ontologies
    - Navigation maps
    - metadata maps
    - Search functionality specifications
    - use cases user flows

<aside>
💡 the information architecture and the content strategy together describe what content will be managed in the system. Design phases describe HOW the strategy will be implemented

</aside>

### 1.3.7 Search Engine

<aside>
💡 A search engine is software that searches for information based on terms and retrieves websites that have those terms within their content. e.g., Google.

</aside>

### 1.3.8 Semantic Model

<aside>
💡 Semantic modelling is a type of modelling that describes a network of concepts and their relationships, and allows users to ask questions of the system in a non-technical way

</aside>

### 1.3.9 Semantic Search

<aside>
💡 A semantic search engine can use artificial intelligence to identify query matches based on keywords and their context. BI and analytics tool users often have semantics search requirements.

</aside>

### 1.3.10 Unstructured Data (rather call it non-tabular or semi-structured data)

<aside>
💡 About 80% of all stored data is outside relational databases. Include word processing documents, emails, social media, chats, flat files, spreadsheets, XML files, transactional messages, reports, graphics, digital images, microfiche and video and audio recordings.

</aside>

- there is no data model to aid understanding. No tags. Not organised in rows and columns
- The fundamental principles of Data Management apply. Unstructured data requires data governance, architecture, security, Metadata and data quality.

### 1.3.11 Workflow

<aside>
💡 Manage content management through a workflow that ensures content is created on schedule and receives proper approvals. Should be automated through use of a content management system (CMS) to provide version control.

</aside>

# 2. Activities

## 2.1 Plan for lifecycle management

- Planning for document management:
    - For the document’s lifecycle
    - Developing classification / indexing systems and taxonomies
    - Creating policy specifically for records

<aside>
💡 Identify an organisational unit responsible for managing documents and records

</aside>

### 2.1.1 Plan for Records Management

<aside>
💡 Define what constitutes a record. the defining team for a functional area should include SMEs and records system people:

</aside>

- Decisions:
    - Where to store and archive
    - Account for paper records as well as electronic unstructured and structured data

### 2.1.2 Develop a Content Strategy

<aside>
💡 Defines how content will be prioritised, organised and accessed

</aside>

- Identify content drivers (the reason content is needed):
    - Inventory of current state
    - Gap assessment

### 2.1.3 Create Content handling Polices

<aside>
💡 Policies help employees understand and comply with the requirements for document and records management

</aside>

- most document management programs have policies relating to:
    - Scope and compliance with audits
    - Identification and protection of vital records
    - Purpose and schedule for retaining records
    - How to respond to information hold orders (in the event of a lawsuit holding records beyond expiry of retention)
    - Requirements for onsite and offsite storage of records
    - Use and maintenance of hard drive and shared network drives
    - Email management, addressed from content management perspective
    - Proper destruction methods
    - **Social Media Policies:** Does a social media post from an employee conducting business become a record?
    - **Device Access Policies:** Content and records management functions need to work with user driven IT (BYOD bring-your-own-devices)
    - **Handling Sensitive Data:** Data Security and Data Governance establish confidentiality schemes and identify confidential and restricted assets. People who assemble content must apply these classifications
    - **Responding to Litigation:** Prepare for the possibility of litigation through proactive e-discovery. Create an inventory of data sources and their associated risks

### 2.1.4 Define content information Architecture

<aside>
💡 Users need to submit search to a system which contains unstructured data in a form understandable th that system. the inventory of structured and unstructured documents needs to be described or indexed for quick retrieval

</aside>

## 2.2 Manage the lifecycle

### 2.2.1 Capture Records and content

- Capturing Data:
    - Electronic content is in the form to be stored in electronic repositories
    - Paper: scan and upload using an electronic signature
        - Tag/index with the appropriated Metadata necessary for retrieval:
            - document identifier
            - Date and time of capture
            - title and authors

### **2.2.2 Manage Versioning and Control**

- ANSI Standard 859 has three levels based on criticality of the data:
    - **Formal control:** Formal change control processes through change control authority
    - **Revision control:** Notify stakeholders and increment versions when a change is required.
    - **Custody control:** Least formal, requires safe storage and means of retrieval.
    
    ![Screenshot 2024-06-12 at 10.26.30.png](Chapter%209%20Document%20and%20Content%20management%2022856610d32d4ab1a3102ebb5ffa2c5e/Screenshot_2024-06-12_at_10.26.30.png)
    
- ANSI 859 recommends taking the following into account when determining control level for an asset
    - Cost of providing and updating the asset
    - Project impact of changes in terms of cost
    - Other consequences of change to the enterprise or project
    - Need to reuse or earlier versions of the asset
    - Maintenance of a history of change

### 2.2.3 Back up and Recovery

Include the documents/record management system in the organisation’s **corporate backup and recovery plan** and **Business Continuity Plan**. A **vital records program** allows the business to conduct business during a disaster and resume normal business afterwards. Vital records must be identified and plans for their protection and recovery must be developed and maintained.

### 2.2.4 Manage retention and disposal

- retentions and disposition policy defines (in accordance with legal and regulatory requirements):
    - The timeframes during which documents for operational, legal, fiscal or historical value must be maintained
    - When inactive documents can be transferred to a secondary storage facility
    - Processes for compliance
    - Methods and schedules for disposition of documents

records managers and information asset owners ensure **privacy and data protections requirements** and prevent identity theft

**software considerations:** may require a certain version of the operating system to read. An upgrade can make documents unreadable or inaccessible

Non-value-added information must be identified and removed as it wastes resources and can be discoverable in the event of litigation. this is often not prioritised because:

- Policies are not adequate
- One person’s non-value-added information is another’s valued information
- Inability to see future needs for current non-value-added records
- There is no buy-in for records management
- Inability to decide which to delete
- Perceived cost of making the decision and removing physical and electronic records
- Electronic space is cheap. Buying more space is easier than archival or removal processes

### 2.2.5 Audit Documents/Records

![Screenshot 2024-06-12 at 10.27.00.png](Chapter%209%20Document%20and%20Content%20management%2022856610d32d4ab1a3102ebb5ffa2c5e/Screenshot_2024-06-12_at_10.27.00.png)

Steps of an audit:

- Define organisational drivers and stakeholders – the why
- Gather data on the process (the how), determine what to measure and what tools to use
- Report the outcomes
- Develop an action plan of next steps and timeframes

## 2.3 Publish and deliver content

- **Provide access, search and retrieval** once it is described by Metadata/key word tagging and classified within the appropriate information content architecture
- **Deliver through acceptable channels**: Users want to consume data on the device of their choice meaning the format may change. It may be difficult to bring it back to the original format e.g., HTML to originally structured

# 3. Tools

## 3.1 Enterprise Content Management System

<aside>
💡 An ECM consists of a platform of core components or applications which can be in-house or in the cloud.

</aside>

- Reports can delivered through common tools or a document management system interface allowing search, view, download and print. Report management is the ability to add, change or delete reports organised in folders

### 3.1.1 Document Management

<aside>
💡 A **document management system** is an application used to track and store electronic documents and electronic images of paper documents. Provides storage, versioning, security, metadata management, content indexing and retrieval

</aside>

Once a document is created within the document management system it is indexed with keywords so that it can be found. Metadata (Extracted automatically or added manually) is stored for each document. Bibliographic records of documents are descriptive structured data in MARC (Machine-Readable Cataloging) standard format.

A document repository enables check-in and check-out features, versioning, collaboration, comparison, archiving, status state, migration from one storage media to another and disposition.

May have a module that supports different types of workflows: Manual, rules-based or dynamic rules based on content.

Document management systems have a rights module to allocate permissions.

- Specialised document management:
    - **Digital asset management:** Document management systems may include management of audio, video and digital photographs
    - **Image processing:** Captures, transforms and manages images of paper and electronic documents. Uses:
        - **Scanning:** Digitising
        - **Optical Character Recognition (OCR):** Mechanical or electronic conversion of digitised print or handwriting to form recognised by software
        - **Intelligence character recognition (ICR):** More intelligent, convert cursive handwriting
        - **Form processing:** Capture of printed forms. System recognises the format
        - **Other digitised images:** Binary image file formats:
            - **vector**: Mathematical formulae to create graphics. Can be resized without compromising resolution. File formats: .eps, .ai and .pdf
            - **Raster**: bitmap of coloured pixels. .jpeg, .gif, .png, .tiff
    - **Records management system:**
        - Automation of retention and disposition
        - E-discovery support
        - Long term archiving to comply with legal and regulatory requirements
        - Vital records program for critical records

### 3.1.2 Content Management System

<aside>
💡 A **content management system** is used to collect, index and retrieve content, storing it either as components or whole documents while maintaining links between the components. It maintains content throughout the lifecycle

</aside>

### 3.1.3 Content and Document workflow

<aside>
💡 **Workflow** tools support business processes, route content and documents, assign work tasks, track status and create audit trails.

</aside>

## 3.2 Collaboration tools

for teams?

## 3.3 Controlled vocabulary and metadata tools

<aside>
💡 Office productivity software, metadata repositories, BI tools and document and content management systems

</aside>

## 3.4 Standard markup and exchange formats

<aside>
💡 To allow computer systems to process unstructured data it must be reformatted

</aside>

- **XML:** Extensible Markup Language
    - Uses Metadata to describe content, structure and business rules of a document
    - Translates structure of the data into a document for data exchange
    - XML tags data elements to identify the meaning of data
    - Older markup methods are HTML and SGML
    - Need for XML-capable content management:
        - Integrating structured and unstructured data in a relational database
        - XML can build enterprise or corporate portals
        - XMP provides labelling and identification of unstructured data
- **JSON:** JavaScript Object Notation
    - Text format is language independent and easy to parse
    - Two structures:
        - Objects: a collection of unordered name/value pairs
        - An array: an ordered list of values
    - Preferred format for web and NoSQL databases
- **RDF and related W3C specifications:**
    - **Resource Description Framework** is the standard for web data exchange
    - Stored in a **triplestore:** Subject (Resource) – predicate (property name) – Object (property value)
    - URI (Uniform Resource Identifier) describes subject-predicate-object
    - URL (Uniform Resource Locator) is a form of URI
    - Semantic Web needs access to both data and relationships between data sets (Linked Data). This is provided by URIs
    - RDF uses XML as its encoding syntax
    - SKOS (Simple Knowledge Organisation System) is an RDF vocabulary
    - OWL (W3C Web Ontology Language) is a vocabulary extension of RDF used for publishing and sharing OWL documents on the web
    - Big Data: If data is accessible using the RDF Triples model, SPARQL query language can be used to find patterns without predefining a schema
- **Schema.org:** Labelling content with open source semantic markup

## 3.5 E-discovery technology

<aside>
💡 Large volume of data. Technology Assisted Review (TAR) is a process where a team can review selected documents and mark them relevant or not. This is input to a predictive coding engine that reviews and sorts the remaining documents according to relevancy

</aside>

# 4. Techniques

- Litigation response playbook
- Litigation Response data map

# 5. Implementation Guideliness

## 5.1 Readiness Assessment / Risk Assessment

<aside>
💡 identify areas where content management improvement is needed. A data management maturity assessment model can help

</aside>

- Specific ECM critical success factors:
    - Content audit and classification for existing content
    - Appropriate information architecture
    - Support of the content lifecycle
    - Definitions of appropriate Metadata tags
    - The ability to customise functions of the ECM solution

### 5.1.1 Records Management Maturity

<aside>
💡 ARMA Generally Accepted Recordkeeping principles guides policy and practice for records management.

</aside>

- ARMA information governance maturity model assesses the organisation’s record keeping program:
    - **Level 1 Sub-Standard:** Information governance and recordkeeping concerns not addressed or just minimally
    - **Level 2 In Development:** Developing recognition information governance and recordkeeping can have an impact
    - **Level 3 Essential:** Minimum requirements to meet legal and regulatory requirements
    - **Level 4 Proactive:** A proactive information governance
    - **Level 5 Transformational**: Information governance is integrated into the corporate infrastructure and business processes

Analyse gaps and risks and their impact on the organisation. If an organisation does not inventory records it is already at risk.

### 5.1.2 E-discovery Assessment

<aside>
💡 A readiness assessment examines and indentifies improvements to the litigation process

</aside>

- A mature process will be documented, defensible and auditable and will specify:
    - Clear roles and responsabilities
    - preservation protocols
    - data collection methodologies
    - disclosure processes

## 5.2 Organisation and Cultural Change

ECM can lead to more tasks, such as scanning and defining Metadata.

Management of content and records may be siloed. Training may be necessary to enforce policies across the enterprise.

Content and records management should be elevated to a high priority activity organisationally, especially in highly regulated industries where the RIM function needs to be closely aligned with Corporate legal and e-discovery functions.

# 6. Document and Content Governance

## 6.1 Information Governance Framework

<aside>
💡 Documents, records and other unstructured content poses risk to an organisation

</aside>

- Drivers to managing the risk include:
    - Legal and regulatory compliance
    - Defensible disposition on records
    - Pro-active preparation for e-discovery
    - Security of sensitive information
    - Management of risks associated with email and Big Data
- Principles of successful information
    - ARMA GARP® principles
    - Assign executive responsibility for accountability
    - Educate employees on information governance responsibilities
    - Classify information correctly
    - Ensure authenticity and integrity of information
    - Determine that the official record is electronic unless specified directly
    - Develop policies for alignment of business systems and third-parties to information governance standards
    - Store, manage and make accessible, monitor and audit approve enterprise repositories and systems for records and content
    - Secure confidential or personally identifiable information
    - Control unnecessary growth of information
    - Dispose information at the end of its lifecycle
    - Comply with requests for information.
    - Improve continuously

<aside>
💡 The Information Governance Reference model (IGRM) shows the relationship of Information Governance with other business functions. The outer ring shows the stakeholders who put policies, standards, processes, tools and infrastructure in place. The centre is a lifecycle diagram.

</aside>

![Screenshot 2024-06-12 at 11.41.43.png](Chapter%209%20Document%20and%20Content%20management%2022856610d32d4ab1a3102ebb5ffa2c5e/Screenshot_2024-06-12_at_11.41.43.png)

## 6.2 Proliferation of information

- The challenge of governance of unstructured data:
    - Unstructured data grows much faster than structured data
    - Ownership can be difficult to ascertain
    - Difficult to classify as business purpose cannot always be inferred
    - Unstructured data without Metadata is a risk as it can be misinterpreted and may be mishandled

## 6.3 Govern for Quality Content

<aside>
💡 Requires effective partnership between data stewards and other data management professionals and records managers. Business data stewards can help define web portals, enterprise taxonomies, search engine indexes and content management issues.

</aside>

- defining quality content requires understanding the context of its production and use:
    - **Producers:** Who creates the content and why
    - **Consumers:** Who uses the information and for what purpose
    - **Timing:** When and how frequently the information is needed
    - **Format:** Is a consistent format required? Are there unacceptable formats?
    - **Delivery:** How the information is delivered, how it will be accessed and security to prevent inappropriate access

## 6.4 Metrics

<aside>
💡 KPIs at strategic and poperational levels, especially if they measure lifecycle functions or risks

</aside>

### 6.4.1 Records Management

- Strategic level:
    - Within regulatory requirements e.g., time taken to meet a requirement
    - Governance e.g., compliance with policies
- Operational level:
    - Within areas of records management resources e.g., operational and capital costs
    - Training
    - Delivery of daily records management services and operations
    - Integration of records management functions with other business functions
- Criteria to measure the success of a records management system:
    - Percentage of total documents and email per user identified as corporate records
    - Percentage of these records put under records control
    - Percentage of the total stored records that have proper retention rules applied
- Use ARMA’s GARP principles and maturity model to guide definition of KPIs.

### 6.4.2 E-Discovery

- KPIs of e-discovery:
    - Cost reduction
    - Efficiency of collecting documents ahead of time rather than reactively
    - How quickly an organisation can implement a legal hold notification process (LHN)

### 6.4.3 ECM (Electronic Content Management)

<aside>
💡 KPIs measure tangible and intangible benefits to the organisation:

</aside>

- Tangible:
    - Increased productivity
    - Cost reduction
    - Improved information quality
    - Improved compliance
- Intangible:
    - Improved collaboration
    - Simplification of job routines and workflow