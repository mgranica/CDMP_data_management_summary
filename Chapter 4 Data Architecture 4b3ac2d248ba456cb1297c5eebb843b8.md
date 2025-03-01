# Chapter 4: Data Architecture

# 1. Introduction

<aside>
💡

In a general sense, *architecture* refers to an organized arrangement of component elements intended to optimize the function, performance, feasibility, cost and aesthetics of an overall structure or system.

</aside>

<aside>
⚠️

*Architecture* can refer to different things depending on the context:

- Description of a current state of systems.
- Components of a set of systems.
- The discipline of designing systems (architecture practice).
- The intentional design of a system or a set of systems (future state or proposed architecture).
- The artifacts that describe a system (architecture documentation).
- The team that does the design work (architecture team or architects).
</aside>

<aside>
💡

Architecture practice (discipline of designing systems) is carried out:

- At different levels within an organisation (enterprise, domain, project, etc.)
- With different areas of focus (infrastructure, application, and data).
</aside>

<aside>
💡 In a more practical sense, *Data Architecture* refers to identifying the data **needs of the enterprise** (regardless of structure) and designing and maintaining the **master blueprints to meet those needs**. Using master blueprints to guide data integration, control data assets and align data investments with business strategy.

</aside>

- Essential components:
    - **Data Architecture Outcomes**
        - The data architecture artifacts, such as models, definitions, and data flows of various levels
        - These constitute metadata and should be stored and managed in an enterprise architecture artifact repository.
    - **Data Architecture Activities**
        - to form, deploy and fulfill Data architecture intentions
    - **Data Architecture Behavior**
        - Collaboration, mindsets, and skills among roles that affect the enterprise’s DA
    
    <aside>
    💡 Data Architecture is fundamental to Data Management. The vast data of an organisation must be represented at various levels of abstraction so that it can be understood for management to make decisions (conceptual, logical, physical)
    
    </aside>
    
- **Organisation’s Data Architecture consist of:**
    - Integrated collection of Master design documents at different levels of abstraction
    - Formal **Enterprise Data Model** - containing:
        - data names
        - metadata definitions: information of interest for the organisation
        - conceptual and logical entities
        - relationships
        - business rules
    
    <aside>
    💡 Data Architecture enables consistent data standardization and integration across the enterprise.
    
    </aside>
    
- **ISO/IEV 42010:2007 Definition**
    
    <aside>
    💡 *Architecture* as “the fundamental organisation of a system, embodied in its components, their relationship to each other and the environment and the principles governing its design and evolution”.
    
    </aside>
    

## 1.1 Business Drivers

<aside>
💡 The goal of Data Architecture is to be a **bridge business strategy and technology execution**. Data Architects create and maintain organisational knowledge about data and the systems through which it moves, which enables it to maintain data as an asset and to increase the value obtained from data.

</aside>

Data Architects do:

- Strategic preparation of evolution of products, services and data to take advantage of business opportunities in emerging technologies
- Translate business needs into data and system requirements
- Manage complex data delivery throughout the enterprise
- Facilitate alignment between business and IT
- Act as agent for transformation and agility

These business drivers influence measures of the value of data

## 1.2 Data Architecture Outcomes and Practices

- **Primary Data Architecture outcomes**
    - Data Storage and processing requirements
    - Designs of structure and plans that meet current and long term data requirements of the enterprise
    - strategically prepare organisations to quickly evolve their products, services and data to take advantage of business opportunities inherent  in emerging technologies
    

(2024, revised version):

![image.png](Chapter%204%20Data%20Architecture%204b3ac2d248ba456cb1297c5eebb843b8/image.png)

- (Original version diagram)
    
    ![Screenshot 2024-07-03 at 09.46.50.png](Chapter%204%20Data%20Architecture%204b3ac2d248ba456cb1297c5eebb843b8/Screenshot_2024-07-03_at_09.46.50.png)
    

### 1.2.1 Goals

- Identify data storage and processing requirements
- Design structures and plans to meet the current and long-term data requirements of the enterprise
- Strategically prepare organisations to quickly evolve their products, services and data to take advantage of business opportunities inherent in emerging technologies

**steps to reach the goals**

- Define the current state of the organisation
- Provide Standards business vocabulary for data and components
- Align Data Architecture with enterprise strategy and business architecture
- Express strategic data requirements
- Outline high level designs to meet these requirements
- Integrate with overall enterprise architecture road-map

An overall Data Architecture practice includes:

- Using DA artifacts (master blueprints) to define data requirements, guide data integration, control data assets, and align data investments with business strategy.
- Collaborating with, learning from, and influencing various stakeholder that are engaged with improving the business or IT systems development.
- Using DA to establish the semantics of an enterprise via common business vocabulary.

## 1.3 Essential Concepts

### 1.3.1 Enterprise Architecture Domains

| Domain | Enterprise Business Architecture | Enterprise Data Architecture | Enterprise Applications Architecture | Enterprise Technology Architecture |
| --- | --- | --- | --- | --- |
| Purpose | To identify how an enterprise creates value for customers and others stakeholders | To describe how data should be organised and managed | To describe the structure and functionality of applications in an enterprise | To describe physical technology needed to enable systems to function and deliver value |
| Elements | Business models, process, capabilities, services, events, strategies, vocabulary | Data models, data definitions, data mapping, specifications, data flows, structured data, APIs | Business systems, software packages, databases | Technical platforms, networks, security, integrations tools |
| Dependencies | Establishes requirements for the others domains | Manages data created and required by business architecture | Acts on specified data according to business requirements | Hosts and executes the application architecture |
| Roles | Business Architects, and analysts, business data stewards | Data Architects and modelers, and data stewards | Applications architects | Infrastructure architects |

![Screenshot 2024-06-03 at 10.25.59.png](Chapter%204%20Data%20Architecture%204b3ac2d248ba456cb1297c5eebb843b8/Screenshot_2024-06-03_at_10.25.59.png)

- TOGAF - The Open Group Architecture Framework

![Screenshot 2024-06-03 at 12.44.01.png](Chapter%204%20Data%20Architecture%204b3ac2d248ba456cb1297c5eebb843b8/Screenshot_2024-06-03_at_12.44.01.png)

enterprise architecture model coded BIAT

- Business
- Information
- Application
- Technology

<aside>
💡 Business Architecture has 2 main activities:
1. **Establish enterprise data architecture**
2. **Integrate with enterprise architecture**

</aside>

- **Components and deliverables of Data Architecture**
    - **Stakeholders**
        - the people involved in the business, whether suppliers, customers or the people in the organisation. There are:
            - business stakeholders
            - data stakeholders
    - **Value propositions**
        - is an innovation, service or feature intending to make a company or product attractive to customers. consist of
            - **Value streams**
                - sequence of activities necessary to deliver a product, service or experience to a customer, internal or external
            - **Data value items** each activity in the value stream
            - **metrics**
    - **Business capability**
        - requirements handled to deliver value → primary business functions an enterprise
    - **Business concepts concepts translate:**
        - information concept == data required
- **Example of a training business**
    
    ![Screenshot 2024-06-03 at 13.05.37.png](Chapter%204%20Data%20Architecture%204b3ac2d248ba456cb1297c5eebb843b8/Screenshot_2024-06-03_at_13.05.37.png)
    
    - **Business Value stream:** (pink process flow)
    - **Train Workforce**, is the deliverable from the Business Architecture
    - *The value stream shows **the sequence of activities necessary*** to deliver value to stakeholder (ie HOW)
    - Value streams may be externally or internally triggered, here it is triggered by a customer requesting training
    - **Metamodel** stores info about the value stream as a business model

![Screenshot 2024-06-03 at 13.07.24.png](Chapter%204%20Data%20Architecture%204b3ac2d248ba456cb1297c5eebb843b8/Screenshot_2024-06-03_at_13.07.24.png)

<aside>
💡 The business value stream is translated into the **value stream specification: which is mapped to the data value chain**

</aside>

![Screenshot 2024-06-03 at 13.45.02.png](Chapter%204%20Data%20Architecture%204b3ac2d248ba456cb1297c5eebb843b8/Screenshot_2024-06-03_at_13.45.02.png)

- **Value Stream Specification**:
    - **Business Entities** are
        - the top line / lanes.
        - They are nouns, eg **Customer**, **Training Facility** (the description of the Business Entities at the bottom in the Data Value Chain are constrained by the business model of the training provider e.g., Customer Training Facility is mapped to Modelware’s Training Session)
    - **Value Stream items**: (Understand **Training Requirements**, **Arrange Training Logistics** etc).
        - Value stream items are grouped by Business Entity (eg **Register for Training Session** & **Deliver Training Session** are grouped under the **Student** Business Entity)
    - There is a metric (orange scale ) used to measure Value stream item. eg **Clear Customer Expectations** measures the Value Stream Item **Understand Training** requirements
    - The metrics above contribute to the **Uplifted Workforce Capabilities** metric provided to the customer
- **Data Value chain**
    - The improvement of the value of data aligned to the business value chain. The data value chain must support the ongoing measurement and improvement of the business value chain
    - Data Value Chain (consists of Business entities, eg Customer, Training Section)
    - **Course evaluation** is the most important to measure success – do we have an uplifted workforce? Outcomes
    - DVC is critical data which builds. Each element enriches the next element. Each segment produces another value item. All comes together as total value
- **Business Capability Map**

![Screenshot 2024-06-03 at 13.49.52.png](Chapter%204%20Data%20Architecture%204b3ac2d248ba456cb1297c5eebb843b8/Screenshot_2024-06-03_at_13.49.52.png)

<aside>
💡 The capabilities will give us an idea of entities we will be mapping, for example we have **Client Management Capability**. Therefore we will need to include a Client entity in our data model

</aside>

### 1.3.2 Enterprise architecture Frameworks:

<aside>
💡

An Architecture Framework is a foundational structure used to develop a broad range of related architectures. They provide ways of thinking about and understanding an architecture (”architecture of architecture”).

</aside>

- Zachman Framework for enterprise architecture
    
    <aside>
    💡 developed by John A. Zachman in the 1980s: an Ontology. the **6x6 matrix** shows the models required to describe an enterprise and the relationships between them. Each cell represents a unique type of design artifact defined by the intersection of row and column
    
    </aside>
    

|  | What | How | Where | Who | When | Why |  |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Execute | Inventory Identification | Process Identification | Distribution Identification | Responsibility Identification | Timing Identification | Motivation Identification | Scope context |
| Business Management | Inventory Definition | Process Definition | Distribution Definition | Responsibility Definition | Timing Definition | Motivation Definition | Business concepts |
| Architect | Inventory Representation | Process Representation | Distribution Representation | Responsibility Representation | Timing representation | Motivation Representation | System Logic |
| Engineer | Inventory specification | Process Specification | Distribution Specification | Responsibility Specification | Timing Specification | Motivation Specification | Technology Physics |
| Technician | Inventory configuration | Process Configuration | Distribution Configuration | Responsibility Configuration | Timing Configuration | Motivation Configuration | Tool Components |
| Enterprise | Inventory instantiation | Process instantiation | Distribution Instantiation | Responsibility Instantiation | Timing Instantiation | Motivation Instantiation | Operational Instances |
|  | Inventory sets | Process flows | Distribution Networks | Responsibility Assignments | Timing Cycles | Motivation Intentions |  |
- **Columns** → *Communication Interrogatives*
    - What (the inventory column): Entities used to build the architecture
    - How (the process column: Activities performed
    - Where (the distribution column): Business location and technology location
    - Who (the responsibility column): Roles and organisations
    - When (the timing column): Intervals, events, cycles and schedules
    - Why (the motivation column): Goals, strategies and means
- **Rows** → *reification transformations*; the steps necessaries to translate an abstract idea into a concrete instance from different perspectives of the overall process (Planner, owner, designer, builder, implementer and user)
    - The executive perspective – Business context
    - The business management perspective – Business concepts
    - The architect perspective – Business logic
    - The engineer perspective – Business physics
    - The technician perspective – Component assemblies
    - The user perspective – Operations classes

### 1.3.3 Enterprise Data Architecture

<aside>
💡

Enterprise Data Architecture defines standard terms and designs for the business data as such, including the collection, storage, integration, movement, and distribution of data.

- Goal: To describe how data should be organised and managed
- Elements: Data models, data definitions, data mapping, specifications, data flows, structured data, APIs
- Dependencies: Manages data created and required by business architecture
- Roles: Data Architects and modelers, and data stewards
</aside>

<aside>
💡 **Enterprise Data Model**: a holistic, enterprise-level, implementation-independent conceptual or logical data model providing a common consistent view of data across the enterprise

</aside>

<aside>
💡 **Data flow** **design** defines requirements and master blueprint for storage and processing across databases, applications, platforms and networks

</aside>

- **Enterprise Data Model**
    
    <aside>
    💡 Can be a stand-alone artifact or may be composed of data models from different perspectives or levels of detail. An EDM includes both universal (Enterprise-wide conceptual and logistical models) and application/project specific data models, along with definitions, specifications, mappings and business rules
    
    </aside>
    
    - Conceptual overview over the enterprise’s subject areas
    - Views of entities and relationships for each subject area
    - Detailed, partially attributed logical views for the same subject area
    - Logical and physical models specific to an application or project

![Screenshot 2024-07-03 at 09.54.54.png](Chapter%204%20Data%20Architecture%204b3ac2d248ba456cb1297c5eebb843b8/Screenshot_2024-07-03_at_09.54.54.png)

- The Enterprise Data Model is built up by the combination of Subject Area Models:
    - **Top Down approach**: Form Subject Areas then populate them with models
    - **Bottom up Approach:** Subject Area structure is based on existing data models
- The **Subject Area Discriminator** (the way subject areas are formed) must be consistent throughout the enterprise data model:
    - **Funding:** Systems portfolios
    - **Organisational**: Data governance structure and data ownership
    - **Business value chains**: Top-level processes
    - **Using business capabilities:** See training organisation example above
    
    ![Screenshot 2024-07-03 at 10.30.21.png](Chapter%204%20Data%20Architecture%204b3ac2d248ba456cb1297c5eebb843b8/Screenshot_2024-07-03_at_10.30.21.png)
    
- **Data Flow Design**
    
    <aside>
    💡 Data flows are a type of **data lineage** documentation that depicts how data moves end-to-end through business processes and systems (where it originated, is stored and used and how it transforms).
    
    </aside>
    
    - documents relationships between data and applications with a business process, data stores and business roles
    - control of data assets

![Screenshot 2024-07-03 at 10.30.53.png](Chapter%204%20Data%20Architecture%204b3ac2d248ba456cb1297c5eebb843b8/Screenshot_2024-07-03_at_10.30.53.png)

![Screenshot 2024-07-03 at 10.31.20.png](Chapter%204%20Data%20Architecture%204b3ac2d248ba456cb1297c5eebb843b8/Screenshot_2024-07-03_at_10.31.20.png)

- two approaches
    - **Quality Oriented**
        - Focus on execution within business and IT structures. Unless architecture is managed it will deteriorate
    - **Innovation Oriented**
        - Focus on transforming business and IT to address new expectations and opportunities. Requires interaction with business development representatives and designers

## 2.1 Establish Data Architecture Practice

- **work streams**
    - **Strategy**:
        - Select Frameworks, state approaches, develop roadmap
    - **Acceptance and culture**
        - inform and motivate changes in behaviour
    - **Organisation**
        - Assign data architecture accountabilities and responsibilities
    - **Working methods**
        - Define best practices and perform data Architecture work within development projects, in coordination with enterprise architecture
    - **Results**
        - Produce Data Architecture artefacts within an overall roadmap
- Enterprise Architecture influences scope boundaries of projects/system releases:
    - Defining project data requirements
    - Reviewing project data designs
    - Determining data lineage impact
    - Data replication control
    - Enforcing Data Architecture standards
    - Guide data technology and renewal decisions

### 2.1.1 Evaluate Existing Data Architecture Specifications

<aside>
💡 Evaluate existing documentation for accuracy, completeness and level of detail. Update if necessary

</aside>

### 2.1.2 Develop a roadmap

<aside>
💡 describe the architecture 3 to 5 year development path, with business requirements, consideration of actual conditions and technical assessments. must be integrated into the enterprise architecture roadmap. Include milestones, resources needed, cost estimations and divided into work streams

</aside>

The enterprise Data Architecture can be formed by resolving input and output data flows in the chain if dependencies between business capabilities

Star with the most independent business capabilities and end with those most dependent on other activities. the following diagram has the lowest dependency on the top

![Screenshot 2024-07-03 at 10.43.49.png](Chapter%204%20Data%20Architecture%204b3ac2d248ba456cb1297c5eebb843b8/Screenshot_2024-07-03_at_10.43.49.png)

- Enterprise data architecture project-related activities include:
    - **Define scope**
        - Ensure the scope and interface are aligned with Enterprise Data Model. Identify components that can be reused and down stream dependencies
    - **Understand business requirements**
    - **Design**
        - Form detailed target specifications. look for shareable constructs in the enterprise logical data model.
        - Review and use technology standards
    - **Implement**
        - **When buying:** Reverse engineer purchased applications and map against data structure
        - **When reusing data:** Map application data models against common data structures and new and existing processes to understand CRUD operations. Enforce use of authoritative data
        - **When building:** Data storage according to data structure
- **Development methodologies for building architectural activities into pro projects**
    - **Waterfall methods**
        - Construct systems in sequential phases as part of an overall design
    - **incremental methods**
        - Learn and construct in gradual steps. creates prototypes based on vague overall requirements
    - **Agile, iterative methods**
        - Learn , construct and test in discrete delivery packages

## 2.2 Integrate with enterprise Architecture

<aside>
💡

Integrate Enterprise Data Architecture matters with project portfolio management as founded projects drive architecture priorities and Data Architecture can influence the scope of projects

</aside>

# 3. Tools

- **Data Modelling Tools:**
    - Include lineage and relation tracking to manage linkages between models
- **Asset Management Software:**
    - Used to inventory systems, describe their content and track the relationships between them
- **Graphical Design Applications:**
    - To create architectural design diagrams and other architectural artifacts

# 4. Techniques

## 4.1 Lifecycle Projections

- Architecture designs can be:
    - Aspirational and future-looking
    - Implemented and active
    - Plans for retirement
- What architectural plans represent should be clearly documented:
    - **Current:** Products supported and used
    - **Deployment period:** Products deployed for use in 1-2 years
    - **Strategic period:** Products available in the next 2+ years
    - **Retirement:** Retired products, or retirement within 1 year
    - **Preferred:** Products preferred for use by most applications
    - **Containment:** Limited for use by certain applications
    - **Emerging:** Researched and piloted for possible future deployment
    - **Reviewed:** Evaluated products and their evaluation results

![Screenshot 2024-06-03 at 17.01.03.png](Chapter%204%20Data%20Architecture%204b3ac2d248ba456cb1297c5eebb843b8/Screenshot_2024-06-03_at_17.01.03.png)

## 4.2 Diagramming clarity

- Models and diagrams must conform to an established set of visual conventions:
    - **Clear and consistent legend:**
        - Identify all objects and lines and placed in the same spot in all diagrams.
    - **Match between all diagram objects and the legend:**
        - Not all legend objects need appear on diagram
    - **Clear and consistent line direction:**
        - ****Usually left to right. Backward lines must be clear
    - **Consistent object attributes:**
        - Differences in size, line thickness and color should signify something
    - **Linear symmetry:**
        - Line up at least half of the objects to improve readability

# 5. Implementation Guidelines

- Data Architecture is about:
    - artifacts, activities and behaviour,
- Enterprise Data Architecture is about:
    - Organizing Enterprise Data Architecture teams and forums
    - Producing initial versions of Data Architecture artifacts such as enterprise data model, enterprise wide data flow and road maps
    - Forming and establishing a data architectural way of working in development projects
    - Creating organisation wide awareness of the value of Data Architecture efforts

<aside>
💡 **Enterprise Data Architecture** starts with **Master Data areas** in need of improvement in planned development projects, and expands to include business and other data.

</aside>

## 5.1 Readiness / Risk Assessment

- **More risks than other projects**, especially during an organisation’s first attempt:
    - Lack of management support
    - No proven record of accomplishment
    - Apprehensive sponsor
    - Counter-productive executive decisions
    - Culture shock
    - Inexperienced project leader
    - Dominance of a one-dimensional view

## 5.2 Organisation and Cultural change

- The ability of an organisation to adopt **Data Architecture practices** depends on several factors:
    - Cultural receptivity to architectural approach
    - Organisation recognizes data as a business asset, not just an IT concern
    - Ability to let go of a local perspective and adopt an enterprise perspective on data
    - Ability to integrate architectural deliverables into project methodology
    - Level of acceptance of formal data governance
    - Ability to look holistically at the enterprise

# 6. Data Architecture Governance

<aside>
💡 Enterprise data architecture and the data Governance Organisation must be well aligned.

</aside>

<aside>
💡 A data architect is best deployed during the early stages of a project to define and shape a strategic solution

</aside>

- A data steward and a data architect should be assigned to each subject area, even to each entity within, as **Data Architecture activities support the alignment and control of data.**
- Business event subject areas should be aligned with business processes governance as each event entity usually corresponds to a business process
- **Data Architecture governance activities** include:
    - **Overseeing projects:** Projects comply with required Data Architecture activities, use architectural assets and are implemented according to data architectural standards
    - **Managing architectural designs, lifecycle and tools:** Designs must be defined, evaluated and maintained
    - **Defining standards**
    - **Creating data-related artifacts**

## 6.1 Metrics

<aside>
💡 Data Architecture metrics may be monitored annually for business customer satisfaction:

</aside>

- **Architecture standard compliance rate:** How far projects comply with established data architectures
- **Implementation trends:** The degree to which enterprise architecture has improved the organisation’s ability to implement projects along at least two lines:
    - **Use/reuse/replace/retire measurements:** Proportion of new architectural artifacts to reused, replaced or retired artifacts
    - **Project execution efficiency measurements:** Measure lead times for projects and their resource costs for delivery improvements with reusable artifacts and guiding artifacts
- **Business value measurements:** Track progress towards expected business benefits
    - **Business agility improvements:** Account for the benefits of lifecycle improvements or the cost of delay
    - **Business quality:** Measure whether business cases are fulfilled and projects deliver changes leading to business improvements
    - **Business operation quality:** Measure of improved efficiency and accuracy
    - **Business environment improvements**