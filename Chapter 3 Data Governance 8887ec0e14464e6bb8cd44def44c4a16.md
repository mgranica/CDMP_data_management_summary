# Chapter 3: Data Governance

# 1. Introduction

<aside>
💡 Data Governance is the exercise of authority and control (planning, implementation, monitoring, and enforcement) over the management of data assets. Its purpose is to ensure that data is managed properly, according to the policies and best practices, and guides all other data management functions.

</aside>

<aside>
⚠️

All organisations make decisions about data, regardless of whether they have a formal Data Governance function.

Data governance is an ongoing program focused on ensuring that the organisation gets value from its data and reduces risks related to data.

The Data governance function is separate from the IT governance function (decisions on hardware, software, and overall technical architecture)

</aside>

- **Strategy**: Defining, communicating and driving execution of Data Strategy and Data Governance.
- **Policy**: Setting and enforcing policies relating to data and Metadata life cycle management (access, usage, security and quality, documentation, and purging)
- **Standards**: Setting and enforcing Data Management standards
- **Oversight**: Providing hands-on observation, audit and correction in key areas of quality, privacy, security, and data management policies and procedures
- **Compliance**: Ensuring the organisation can meet data-related regulatory compliance requirements
- **Issue management:** Identifying, defining, escalating and resolving issues related to data security, data access, data quality, regulatory compliance, data ownership, policy, standards, terminology or data governance procedures
- **Data Management projects**: Sponsoring efforts to improve data management practices
- **Data asset valuation**: Setting standards and processes to define business value of assets

(2024 revised version):

![image.png](Chapter%203%20Data%20Governance%208887ec0e14464e6bb8cd44def44c4a16/image.png)

- (Original version diagram)
    
    ![Screenshot 2024-06-27 at 10.33.00.png](Chapter%203%20Data%20Governance%208887ec0e14464e6bb8cd44def44c4a16/Screenshot_2024-06-27_at_10.33.00.png)
    

## 1.1 Business drivers

**Reducing risk**

- **General risk management**: oversight of the risks data poses on finances, reputation, legal e-discovery, regulatory issues
- **Data security**: Protection of data assets through controls for the availability, usability, integrity, consistency, auditability, and security of data
- **Privacy:** Control of private, confidential and Personal Identifying information (PII) through policy and compliance monitoring

**Improving processes**

- **Regulatory Compliance**
- **Data Quality improvement**
- **Metadata Management**
    - Business glossary and other Metadata
- **Efficiency en development projects**:
    - SDLC improvements
- **Vendor Management**
    - Contracts dealing with Data Governance is separate from IT governance and is ongoing

## 1.2 Goals And Principles

1. Enable an organization to manage its data as an asset
2. Define, approve, communicate and implement principles, policies, procedures, metrics, tools and responsibilities for data management
3. Monitor and guide policy compliance, data usage and management activities

**Program to achieve these GOALS**

- **Sustainable:** Ongoing and depends on business leadership, sponsorship and ownership
- **Embedded** DG Activities incorporated into development methods, use of analytics, management of Master Data and Risk Management
- **Measured:** to show positive financial impact
- **Foundational Principles**:
    - **Leadership and Strategy** committed leadership, driven by enterprise business strategy
    - **Business-driven** DG is a **business program** and must govern IT decisions relating to data
    - **Shared responsibility** Across all Data Management knowledge areas
    - **Multi-layered** All levels from local to enterprise
    - **Framework-based** Establish an operating framework
    - **Principle-based** Principles are the basis of policies

## 1.3 Essential Concepts

<aside>
💡 Ensuring data is managed without directly executing data management. **Separation of duties between oversight and execution - RACI model**

</aside>

![Screenshot 2024-05-29 at 16.53.12.png](Chapter%203%20Data%20Governance%208887ec0e14464e6bb8cd44def44c4a16/Screenshot_2024-05-29_at_16.53.12.png)

### 1.3.1 Data Centric Organisation

<aside>
💡 A data centric organisation values **data as an asset** and manages data through all phases of its lifecycle, including project development and ongoing operations

</aside>

**Principles**

- Manage DATA as a corporate asset
- Incentivise Data Management best practices across the organisation
- Enterprise data strategy misaligned to overall business strategy
- Continually improve data management processes

### 1.3.2 Data Governance Organisation

![Screenshot 2024-05-29 at 16.56.40.png](Chapter%203%20Data%20Governance%208887ec0e14464e6bb8cd44def44c4a16/Screenshot_2024-05-29_at_16.56.40.png)

| Data Governance Body | Description |
| --- | --- |
| **Data Governance Steering committee** | The **primary and highest authority organisation** for data governance. 
Responsible for oversight, support and funding of data governance activities. 
consist of a Cross functional group of senior executives
typically chair by **Chief data Steward (Busines) / Chief Data Officer
set the overall direction for Data Governance**:  |
| **Data Governance Council (DGC)** | Manages Data governances initiatives (e.g. development of **policies or metrics**) issues and escalations. 
Consists of executive according to the operating model used. 
ultimate sponsor and approving body for the enterprise data architecture |
| **Data Governance Office (DGO)** | Ongoing focus on **enterprise-level data definitions** and data management standards across all DAMA-DMBOK knowledge areas. 
Consist of coordinating roles that are labelled as *data stewards* or *custodians* and *data owners*. |
| **Data Stewardship Teams** | Communities of interest focused on one or more specific subject-areas or projects, 
collaborating or consulting with project teams on data definitions an data management standards related to the focus. 
Consists of business and technical data stewards and data analysts |
| **Local Data Governance Committee** | Large organisations may have divisional or departamental data governance council working under the auspices of an enterprise DGC. 
Smaller organisations should try to avoid such complexity |

![Screenshot 2024-05-29 at 17.40.47.png](Chapter%203%20Data%20Governance%208887ec0e14464e6bb8cd44def44c4a16/Screenshot_2024-05-29_at_17.40.47.png)

![Screenshot 2024-05-29 at 17.40.58.png](Chapter%203%20Data%20Governance%208887ec0e14464e6bb8cd44def44c4a16/Screenshot_2024-05-29_at_17.40.58.png)

 

### 1.3.3 data Governance Operating Model Types

- **Centralised**
    - One central EIM / DG Team with Councils within the Business
    - Data Governance organization oversees all activities in all subject areas
        
        ![Screenshot 2024-06-27 at 10.40.36.png](Chapter%203%20Data%20Governance%208887ec0e14464e6bb8cd44def44c4a16/Screenshot_2024-06-27_at_10.40.36.png)
        
- **Decentralised / replicated**
    - One DG Team per Business Organisation Structure
        
        ![Screenshot 2024-06-27 at 10.41.01.png](Chapter%203%20Data%20Governance%208887ec0e14464e6bb8cd44def44c4a16/Screenshot_2024-06-27_at_10.41.01.png)
        
- **Hybrid**
    - One central EIM and by business organisation structure
- **Federated**
    - Unite in a federation - individual anatomy, centralised strategy, functions in BUs
    - Data Governance organization coordinates with multiple Business Units to maintain consistent definitions and standards
        
        ![Screenshot 2024-06-27 at 10.41.21.png](Chapter%203%20Data%20Governance%208887ec0e14464e6bb8cd44def44c4a16/Screenshot_2024-06-27_at_10.41.21.png)
        
- **Self-organising/Network**
    - Non invasive Model based on RACI

### 1.3.4 Data Stewardship

<aside>
💡 A **Steward** is a person whose job it is to manage the property of another person??
Effective data stewards are accountable and responsible for data processes that ensure effective control and use data assets

</aside>

- recognized subject matter expert in data subject area / business domain that he or she is responsible for
- works in association with the data owner to protect and enhance the data assets
- effective communicator
- works collaborativelly across the organisation with data stakeholders and others identifying data problems & issues

**Activities**

- Creating and managing core Metadata
- Documenting rules and Standards
- Managing Data quality issues
- Executing operational data governance activities

### 1.3.4 Types of Data Steward

<aside>
💡 A **Data Steward** manages the data assets on behalf of others and in the best interests of the organisation.
They are accountable and responsible for data governance and have a portion of their time dedicated to these activities

</aside>

- **Chief data Stewards**
    - Chair DG bodies, act as CDO, be executive sponsors
- **Executive Data Steward**:
    - Senior Managers who serve on the Data Governance Council
- **Enterprise Data Steward**
    - Oversight of a data domain across business functions
- **Busines Data Steward**
    - Business professionals, subject matter experts
- **Data Owner**
    - A business data steward whit approval authority for decisions within domain
- **Technical Data Stewards**
    - IT professional operating in one of the knowledge areas:
        - DBA
        - BI specialist
        - Data integration specialist
        - Data Quality analyst
        - Metadata Administrators
- **Coordinating Data Stewards**
    - Lead teams of business of the knowledge areas (prior category)

**Data Principles** → *Extra not in the DMbok*

- **Enterprise data must be modelled:**
    - Modelled, named and defined according to standards across all business divisions
    - Effort made by management to share data – not maintain redundant data
    - Originating data stewards recognise needs of downstream processes
- **Enterprise data must be maintained close to the source:**
    - Create and maintain as close to the source as possible
    - Data Quality standards applied to approved reliability levels as defined by business units
- **Enterprise data must be safe and secured:**
    - In all electronic formats must be safeguarded on requirements and compliance guidelines
    - Guidelines are determined by business stewards of Enterprise data
    - Backup and recovery measures
- **Enterprise data must be accessible**:
    - Enterprise data and metadata shall be readily available and accessible to all except where restricted
    - Business stewards of enterprise data are responsible for defining the types of individuals, and levels of access privileges
    - Information Security will be responsible for the implementation of proper security controls
- **Metadata will be recorded and utilised:**
    - All projects utilise defined Metadata for data naming, data modelling and database design.
    - Data Governance is responsible for the Metadata program

### 1.3.6 Data Policies

<aside>
💡 Directives that codify principles and management intent into fundamental rules governing the creation, acquisition, integrity, security, quality and uso of data and information

</aside>

- Global
- Describe the “what” of the data governance
- should be few data policies and should be stated briefly and directly

### 1.3.7 Data Asset Valuation

<aside>
💡 Process of understanding and calculating the economic value of data to the organisation

</aside>

Data sets are font interchangeable (fingible) between organisations. How an organisation gets value from customers data can be a competitive differentiator

**Ways of measuring value**

- **Replacement Cost** of data lost in a breach or disaster
- **Market Value**. As a business asset at the time of a merge or acquisition
- **Identified opportunities** The income to be gained
- **Selling data** as a package, or the insights to be gained
- **Risk cost** Potential penalties, remediation costs and litigation expenses

**Principles for data Asset Accounting** → Generally Accepted Accounting Principles

| Principle | Description |
| --- | --- |
| Accountability principle | An organisation must identify individuals who are ultimately accountable for data and content of all types |
| Asset principle | Data and content of all types are assets and have characteristics of other assets. they should be managed, secured and accounted for as other material or financial assets |
| Audit Principle | The accuracy of data and content is subject to periodic audit by an independent body. |
| Due diligence principle | If a risk is known. It must be reported.
If a risk is possible, it must be confirmed
Data risks include risks related to poor data management practices |
| Going Concern principle | Data and content are critical to successful, ongoing business operations and management
(i.e., they are not viewed as temporary means to achieve results or merely as a business by-
product). |
| level of valuation | Value the data as an asset at a level that makes more sense, or it is easier to measure |
| liability principle | Financial liability connected to data or content based on regulatory and ethical misuse or missmanagement |
| quality principle | The meaning, accuracy and lifecycle of data and content can affect the financial status of theorganisation |
| risk principle | There is a risk associated with data and content  |
| value principle | There is value in data and content, based on the ways these are used to meet an organization’s objectives, their intrinsic marketability, and/or their contribution to the organization’s goodwill valuation.
The value if information reflects its contribution to the organization offset by the cost of maintenance and movement |

# 2. Data Governance activities

## 2.1 Data Governance Activities

- DG must support business strategy and goals
- Enterprise Data Strategy is informedly business strategy and goals
- DG enables shared responsability for data decisions
- Clear understanding of what and who are governed and who is governing
- DG is most effective when it is an enterprise effort

## 2.2 Perform Readiness Assessment

- **Data management maturity**:
    - Understand what the organisation does whit data, measures current management capabilities
- **Capacity to change**
    - Measure capacity of organisation to change and identify possible resistance points
- **Collaborative readiness**
    - measures collaboration across functional areas
- **Business Alignment**
    - how well data use aligns with business strategy

## 2.3 Perform Discovery and business Alignment

- **Discovery Activity**
    - Identify and assess effectiveness of existing policies and guidelines
    - identify opportunities for DG to improve usefulness of data
- **Business Alignment**
    - Attaches business benefits to DG
- **Data Quality analysis**
    - Identify issues and risks associated with poor quality data
    - Identify business processes at risk from poor quality data
    - Financial and other benefits from creating a DQ program as part of DG
- Assessment of **data management practices**
- Derive a list of **Dg Requirements** which will drive **DG** to the CDO

## 2.4 Develop organisational touch points

<aside>
💡 touch points for Data Governance work that support alignment of an enterprise data governance and data management outside the direct authority of the CDO

</aside>

<aside>
💡 touch points throughout the project lifecycle are facilitated by the **Data Governance Office**

</aside>

![Screenshot 2024-06-27 at 10.57.26.png](Chapter%203%20Data%20Governance%208887ec0e14464e6bb8cd44def44c4a16/Screenshot_2024-06-27_at_10.57.26.png)

- **Procurement and contracts**
    - enforce standard contract language
- **Budget and Funding**
    - prevent duplicate acquisitions and ensure optimisation if data assets
- **Regulatory compliance**
    - CDO understands and works within regulatory requirements
- **SDLC / System Development Life Cycle framework**
    - identifies control points where enterprise policies, processes and standards can be developed

## 2.5 Develop Data Governance Strategy

<aside>
💡 defines the scope and approach to governance efforts. DG strategy should be defined comprehensively and articulated in relation to the overall business strategy, as well as to data management and IT strategies.

</aside>

- The specific content will be tailored to each organization, but the deliverables include:
    - **Charter**
        - business drivers, vision, mision and principles of data governance
    - **Operating framework and accountabilities**
        - Structure and responsabilities
    - **Implementation roadmap**
        - TimeFrames
    - **Plan for operational success**
        - describe target state

## 2.6 Define the DG of Operating framework

<aside>
💡 consider the following areas when constructing the organisations operating model.

</aside>

- **Value of data to the organisation**
    - Important if the organisation sells data
- **Business model**
    - Decentralised, centralised, international
- **Cultural factors**
    - Acceptance of discipline and adaptability to change
- **Impact of regulation**
    - Level of regulation of the organisation

<aside>
💡 **Layers of Governance:** determine where accountability resides for stewardship activities and data ownership

</aside>

**The DG operating framework defines**

- Interaction between Governance Organisation and people responsible for data management initiatives
- Engagement of change management initiatives to introduce DG
- Modeller issue resolution pathway through governance
    
    ![Screenshot 2024-06-27 at 11.04.08.png](Chapter%203%20Data%20Governance%208887ec0e14464e6bb8cd44def44c4a16/Screenshot_2024-06-27_at_11.04.08.png)
    

## 2.7 Develop Goals, Principles and Policies

Derived from the DG strategy to the desired future state

- Drafted by data management professionals and/or business policy staff
- Refined by data stewards and management
- Data governance Council conducts final review, revision and adoption

Data policies must be effectively communicated, monitored, enforced and periodically re-evaluated. 

**Data Governance Council** may delegate this authority to the Data Stewardship Steering Committee

## 2.8 Underwrite Data Management Projects

<aside>
💡 Promote enterprise wide data management improvements by articulating the ways they improve efficiency and reduce risk
Should be Priority for organisations wanting more value from their data

</aside>

- The DGC helps define the business case and oversees data management improvement project status and progress in coordination with the Project Management Office
- Data Management projects are part of the IT Projects portfolio
- The DGC coordinates projects with enterprise wide scope such as Master Data Management, Enterprise Resource Planning (ERP) and Customer Relationship Management (CRM).
- Data Management requirements must be captured in the planning and design phases of the SDLC

## 2.9 Engage Change Management

<aside>
💡 **Organisational Change Management** is required to bring about change in the organisation’s systems and processes. A mature organisation in Change Management builds clear vision, leads and monitors from top, and designs & manages small changes with feedback. involves collaboration in whole organisation

</aside>

- **Planning**
    - Stakeholder analysis
    - Gain sponsorship
    - communications approach to resistance to change
- **Training**
    - Creating and executing training plans for DG programs
- **Influencing systems development**
    - engage with PMO to add DG steps to the SDLC
- **Policy implementation**
    - Communicate policies and the organisation’s commitment to Data Management activities
- **Communications**
    - Promoting the value of data assets
    - Monitoring and acting on feedback about DG activities
    - implementing data management training
    - measuring the effects of change management in 5 key areas
        - Awareness of the need to change
        - Desire to participate and support the change
        - Knowledge about how to change
        - ability to implement new skills and behaviours
        - Reinforcement to keep change in place
    - implementing new metrics and KPIs
        - Employee incentives

## 2.10 Engage in Issue Management

the process of identifying quantifying prioritising and resolving DG issues:

- **Authority:** Questions around rights and procedures
- **Change management escalations:** Arising from the change management process
- **Compliance:** Issues needing compliance requirements
- **Conflicts:** Policies, procedures, business rules, names, definitions, stakeholder interests etc.
- **Conformance:** Issues related to conformance to policies, standards, architecture etc.
- **Contracts:** Negotiation and review
- **Data security and identity**: Privacy and confidentiality issues and breaches
- **Data quality:** Detection and resolution of DQ issues

![Screenshot 2024-06-27 at 11.10.26.png](Chapter%203%20Data%20Governance%208887ec0e14464e6bb8cd44def44c4a16/Screenshot_2024-06-27_at_11.10.26.png)

Develop control mechanisms and procedures for:

- indentifying, capturing, logging and updating issues
- Assignment and tracking of action items
- Documenting stakeholder viewpoints and resolution alternatives
- Determining, documenting and communicating issue resolutions
- Facilitating objective, neutral discussions where all viewpoints are heard
- Escalating issues to higher levels of authority

## 2.11 Assess Regulatory Compliance Requirements

<aside>
💡 Part of the DG function is to **monitor and ensure regulatory compliance.** 
DG guides the implementation of controls to monitor and document compliance with data-related regulations.

</aside>

**Global regulations with impact data management practices**

- Accounting standards
- BCBS 239 (Basel Committee on Banking Supervision) and Basel II – for banks
- CPG 235 (Australian Prudential Regulation Authority APRA) – banks and insurance
- PCI-DSS – The Payment Card Industry Data Security Standards
- Solvency II - European Union Rules for insurance, similar to Basel II
- Privacy Laws

**Evaluate the implications of the regulations**

- Relevance of regulation to the organisation
- What constitutes compliance, and what policies and procedures are required?
- When is compliance achieved, and how and when is it monitored?
- Can industry standards achieve compliance?
- How is compliance demonstrated?
- Risks and penalties for non-compliance
- How is non-compliance identified and reported?
- How is non-compliance managed and rectified?

## 2.12 Implement DG

<aside>
💡 There are many complex activities which need to be coordinated using a roadmap with timeframes.
Schedules may differ in a federated model with different business units based on differing levels of engagement, maturity and funding.

</aside>

**Prioritised DG activities in the early stage:**

- define activities for high-priority goals
- business glossary, document terminology and standards
- coordinate with enterprise and data architecture to understand the data and systems
- assign financial value to data assets to enable better decision making and understanding

## 2.13 Sponsor Data Standards and Procedures

<aside>
💡 **Standard** something set up and established by authority as a rule for measure of quantity, weight, extent, value or quality
help define DQ by providing a means of comparison

</aside>

enforce standards to promote consistent results from the processes using them. Data can be measured against standards. The DGC or Data Standards steering committee should audit DM activities as part of the SDLC approval process or by schedule

### 2.13.1 Standards difficulties in organisations

- Politicised
- Organisation not practiced at developing or enforcing DG standards
- Value of implementing standards is not recognised
- No knowledge how to implement standards

### 2.13.2 Differents forms of data standards

- How a field should be populated
- Rules governing relationships between fields
- Acceptable and unacceptable values
- Format

### 2.13.3 Process

<aside>
💡 Data standards must be communicated, monitored, reviewed and updated. There must be a means to enforce them.

</aside>

- Standards are drafted by data management professionals
- Reviewed, approved and adopted by the DGC or a Data Standards Steering Committee (A delegated workgroup)
- Document with capturing organisational knowledge in mind

The DGC or DSSC should audit DM activities for standards compliance on a defined schedule or as part of the SDLC approval processes.

<aside>
💡 **Data management Procedures** the documented methods, techniques and steps followed to accomplish specific activities that produce certain outcomes and supporting artefacts

</aside>

## 2.14 Develop a Business Glosary

<aside>
💡 A **Business glossary** is list of terms, definitions and others metadata such as synonyms, metrics, lineage, business rules. The data steward who is responsible for that terms

</aside>

![Screenshot 2024-05-30 at 16.50.07.png](Chapter%203%20Data%20Governance%208887ec0e14464e6bb8cd44def44c4a16/Screenshot_2024-05-30_at_16.50.07.png)

**Objectives of business glossary**

- Enable common understanding of core business concepts and terminology
- Reduce the risk that data will be misused due to inconsistent understanding of the business concepts
- improve alignment between technology assets and business organisation
- maximise search capability and enable access to documented institutional knowledge

## 2.15 Coordinate with Architecture groups

<aside>
💡 DG sponsors and approves data architecture artefacts & enterprise data model

</aside>

Enterprise Data Architecture Steering Committee or Architecture Review Board appointed by DGC to oversee DA Program

- **Enterprise Data model developed by Data Architects and Data Stewards** in subject area teams
- Changes or extensions to EDM proposed and developed by Data Steward Teams
- EDM must align with business strategy and data strategy

<aside>
💡 The enterprise data model must be reviewed, approved and formally adopted by the DGC. It must be align to key business strategies, processes and systems

</aside>

## 2.16 Sponsor data asset valuation

<aside>
💡 DGC organises and standardises the effort. to put monetary value to data

</aside>

- Information gaps represents business liabilities
- Business value of missing data can be the cost of closing the gaps
- Develop models to estimate value of information that does not exist
- Build value estimates into the data strategy road map
    - justifies business cases for root cause DQ solutions
    - Business cases for other DG initiatives

## 2.17 Embed DG

<aside>
💡 The organisation accepts the governance of data and the processes and funding are in place to enable the continued performance of the DG framework

</aside>

- **GOAL of the DGO**
    - Embeed behaviours related to managing data as an asset in processes
    - operations plan to implement and operate DG activities
    - activities, timing and techniques to ensure success
- **Sustainability of the DG organisational framework**
    - Processes and funding in place
    - organisation accepts the governance of data
    - DG is measured monitored and obstacles overcome
- **Create a Data governance community of interest**
    - depends the understanding of DG
    - Helpful in early years of governance

# 3 Tools and techniques

<aside>
💡 DG is fundamentally about organisational behaviour, but tools can help with communication, metrics and business glossary development
Requirements must be clearly defined before purchasing a tool

</aside>

- **Online Presence / Websites:**
    - For collaboration, communication and sharing documents
- **Business Glossary:**
    - Core DG tool housing agreed-upon definitions and business terms and relates them to data
- **Workflow tools:**
    - Connects processes to documents and is useful in policy admin and issue resolution
- **Document management tools**
- **Data Governance Scorecards:**
    - Collection of metrics to track DG activities. Can be automated

# 4. Implementation guidelines

## 4.1 Organisation and culture

<aside>
💡 The target of organisational change is **sustainability** (a quality of a process that measures how easy it is for the process to continue to add value)

</aside>

## 4.2 Adjustment and Communication

- Business / DG strategy map
- DG Roadmap
- Ongoing business case for DG
- DG Metrics

# 5. Metrics

<aside>
💡 DG program must be able to measure progress and success and how DG participants have added value to business objectives

</aside>

- **Value**: Contributions to business objectives, reduction of risk, improved efficiency
- **Effectiveness**: Achievement of goals and objectives, Stewards using relevant tools, Effectiveness of communication, education and training
- **Sustainability**: Policies and processes working appropriately, Staff conforming to standards and procedures

![Screenshot 2024-05-30 at 17.12.22.png](Chapter%203%20Data%20Governance%208887ec0e14464e6bb8cd44def44c4a16/Screenshot_2024-05-30_at_17.12.22.png)

![Screenshot 2024-05-30 at 17.12.45.png](Chapter%203%20Data%20Governance%208887ec0e14464e6bb8cd44def44c4a16/Screenshot_2024-05-30_at_17.12.45.png)