# Chapter 1: Data management

# 1. Introduction

<aside>
💡 DM requires technical and non-technical skills. Business and IT. must collaborate to share responsibility of managing data.Effective data management requires leadership commitment

</aside>

> **Data Management**: Is the development, execution and supervision of plans, policies, programs and practices that deliver, control, protect and enhance the value of data and information assets throughout their lifecylce
> 

> **Data Management Professional** is any person who works in any facet of data management, from highly technical to strategic business, to meet strategic organisation
> 

### 1.1 Business Drivers

- competitive advantage of better decisions based on reliable, high quality data
- Failure to manage data is the same as the failure to manage capital
- the primary driver is to enable organisations to get value from their data assets

### 1.2 Goals within an organization

- understanding and supporting the information needs of the enterprise including stakeholders
- Capturing, storing, protecting and ensuring the integrity of the data assets
- ensuring quality of data and information
- preventing unauthorised or inappropriate access, manipulation or use of data
- ensuring data can be used effectively add value to the organisation

# 2. Essential Concepts

### 2.1 Data **Definition**

- **IT understanding**: Information that has been stored in a digital form.
- Facts which can be aggregated, analysed and used to make a profit, improve health or influence public policy
- Data is a mean of representation which stands for things other than itself
- Data is both an interpretation of the objects it represent and an object that must be interpreted
- To interpreted data, context or metadata is needed

### 2.2 Data and Information

<aside>
💡 The terms *data* and *information* are used interchangeably in the DMBOK. **data** is a form of **information** and **information** is a form of **data.**

</aside>

- Knowledge is required to create data in the first place
- Data management body of knowledge is produced by the **Data management association**
- Data does not simply exist, it has to be created

### 2.3 Data as an Organisation Asset

<aside>
💡 An asset is an economic resource, that can be owned or controlled. It holds or produce value. As organisations become more reliant on data to make decisions the value of data assets is more clearly established

</aside>

### 2.4 Data Management Principles

<aside>
💡 Effective data management requires leadership commitment

</aside>

| principles | components | Description |
| --- | --- | --- |
| DATA IS VALUABLE | **Data is an asset with unique properties** | Not consumed as it is used unlike financial or physical assets |
|  | **The value of data can and should be expressed in economic terms** | NO standards yet. Organisations should develop consistent ways of quantify value. Measure costs of low quality as well as benefits of high quality data |
| DATA REQUIREMENTS ARE BUSINESS REQUIREMENTS | **Managing data means managing the quality of data** | Understand stakeholders requirements for quality and ensure data is fit for their purpose |
|  | **It takes Metadata to manage data** | Metadata enables us to understand what intangible data is, and how to use it |
|  | **It takes planning to manage data** | keep results aligned requires planning for architectural and business process |
| DATA MANAGEMENT RELIES ON DIVERSES SKILLS | **Data Management is Cross-Functional, it requires a range of skills and expertise** | Collaboration between technical and business skills. |
|  | **Data management requires an enterprise perspective** | to be effective, relies on the intertwine between DM and DG
Project ≠ Programs |
|  | **Data management must account for a range of perspectives** | DM must constantly evolve to keep up with the ways data is created and used |
|  | **Data Management requirements must drive information technology decisions** | technology serves rather than drives an organisation’s strategic data needs |
| DATA MANAGEMENT IS LIFECYCLE MANAGEMENT | **Different types of data have different lifecycle characteristics** | DM practices need to recognise this and be flexible enough to meet different kinds of lifecycle requirements |
|  | **Managing data includes managing the risks associated with data** | Lost, stolen, misused and ethical implications. Managed as part of the lifecycle |

## 2.5 Data Management Challenge

### 2.5.1 Data differs from others assets

<aside>
💡 Data is an organizational asset, as if the international standard is concerned with asset management  **ISO 55000/55001**

</aside>

- Data is not tangible
- It is durable and does not wear out
- The value changes as it ages
- Easy to copy and transport
- Not easy to reproduce if lost or destroyed
- can be stolen but not gone
- Not consumed when used
- The same data can be used by multiples people at the same time

### 2.5.2 Data Valuation

<aside>
💡 Data has a value but it is challenging to measure it. it must be managed with care

</aside>

> **Value** is the difference between the cost of a thing and the benefit derived from that thing. The value of data is contextual and often temporal
> 

**Cost Categories**

- Obtaining and sorting data
- replacing lost data
- impact of missing data to the organisation
- risk mitigation and potential costs of risks associated with data
- cost of improving data
- benefits of higher data quality
- what competitors would pay for data/ what data could be sold for
- expected revenue from innovative uses of data

### 2.5.3 Data Quality

<aside>
💡 **Define business needs and the characteristics that make data high quality with business data consumers.** People who use data need to assume data is reliable and trustworhty as they need to use the data to learn and create value, and make business decisions. Poor quality dates costly to the organization

</aside>

| Costs of poor quality data | Benefits of high quality data |
| --- | --- |
| scrap and rework | improved customers experience |
| Work-arounds and hidden correction processes | Higher productivity |
| Organisational inefficiencies or low productivity | Reduced risk |
| Organisational conflicts | Ability to act on opportunities |
| Low job satisfaction | increase revenue |
| Opportunity costs, including inability to innovate | Competitive advantage gained from insights on customers, products, processes and opportunities |
| Compliance costs or fines |  |
| Reputational costs |  |

### 2.5.4 Planning for better data

<aside>
💡 View data as a product and plan for quality throughout its life cycle. Planning is a collaboration between Business and Technology, as it involves architecture, modelling and other design finctions

</aside>

### 2.5.5 Metadata and data management

- Business Metadata (Chap 12)
- Technical Metadata (Chap 12)
- Operational Metadata (Chap 12)
- Metadata embedded in: (Chap 4-11)
    - Data architecture
    - data models
    - data security and requirements
    - data integration standards
    - data operational processes

### 2.5.6 Data Management is Cross-functional

<aside>
💡 Data is managed in differents places within an organisation by teams that have responsability for different phases of the lifecycle

</aside>

### 2.5.7 Establishing an Enterprise Perspective

<aside>
💡 Data is a ‘Horizontal’ as it moves across all the ‘verticals’ (Sales, Marketing, operations) of the organisation. Stakeholders assume the organisation’s data should be coherent, and the goal off managing data is the make the dispare data originating from different places fit together in common sense ways so that it is usable by a wide range of consumers

</aside>

### 2.5.8 Accounting for the others perspectives

<aside>
💡 People who create data must be aware others will use it later. Plan around other potential uses of the data to account for legal and compliance regulations and prevent future misuse

</aside>

### 2.5.9 The data Lifecycle

<aside>
💡 The data lifecycle is based on the product lifecycle. Throughout its lifecycle data can be cleansed, transformed, merged, enhanced or aggregated. Managing data involves interconnections processes aligned with the lifecycle

</aside>

![Screenshot 2024-05-27 at 16.55.08.png](Chapter%201%20Data%20management%20716abf8b89e844d9988c7fdd6bdf7465/Screenshot_2024-05-27_at_16.55.08.png)

- Data also has lineage, from point of origin to point of usage, which must be documented
- Minimize ROT data (Redundant, Obsolete, Trivial)

**Implications of the focus of data management on the data lifecycle**

| Implication | Description |
| --- | --- |
| **Creation and Usage are the most critical points in the data lifecycle** | it costs money to produce data and it only has value when it is used. |
| **Data Quality must be managed throughout the lifecycle** | see chapter 13 |
| **Metadata Quality must be managed through the data lifecycle** | in the same way as the quality of other data (See Chapter 12) |
| **Data security must be managed throughout the data lifecycle** | Protection from creation to disposal (see Chapter 7) |
| **Data management efforts should focus on the most critical data** |  |

### 2.5.10 Differents types of data

<aside>
💡 Classify the data to be managed as different types requires different processes. tools of data management focused on classification and control

</aside>

- By type:
    - Transactional data
    - Reference data
    - Master data
    - Metadata
    - Category data
    - Resource data
    - Detailed transaction data
- By content:
    - Data domains
    - Subject areas
- By format
- By the level of protection which the data requires

### 2.5.11 Data and Risk

- Low quality data represents risk as it is not right
- Data may be misunderstood and misused
- information gaps
- data privacy regulations
- Stakeholders requiring privacy may be broader than previous thought

### 2.5.12 Data Management and technology

<aside>
💡 data requirements aligned with business should drive decisions about technology

</aside>

### 2.5.13 Effective Data Management requires Leadership and Commitment

<aside>
💡 A **Chief Data Officer** (CDO) **leads data management initiatives** and ensures data management is business driven instead of IT driven. The CDO leads cultural change required for the organisation to have a more strategic approach to its data.

</aside>

## 2.6 Data Management Strategy

<aside>
💡 A strategic plan is a high-level course of action to achieve high-level goals. Should address all knowledge areas of DAMA-DMBOK

</aside>

- **Components of Data Management strategy**
    - A compelling vision for data management
    - A summary business case for data management with examples
    - Guide principles, values and management. prespectives
    - The mission and long term directional goals of data management
    - Proposed measures of data management success
    - Short term (12-24 months) Data Management program objectives that are **SMART** (Specific, Measurable, Actionable, Realistic, Time-bound)
    - Description of Data Management roles, organisations and their responsibilities
    - Descriptions of the Data Management program components and initiatives
    - Prioritised program of work with scope boundaries
    - Draft implementation roadmap with projects and action items
- **Deliverables**
    - **Data Management Charter:**
        - Overall vision, business case, goals, principles, measures of success, critical success factors, risks, operating model
    - **Data Management Scope Statement:**
        - Goals and objectives for usually 3 years, roles, organisations and individual leaders accountable
    - **Data Management Implementation Roadmap:**
        - Specific programs, projects, tasks and milestones

# 3. Data Management Frameworks

<aside>
💡

</aside>

<aside>
💡 A framework is needed in order to prepare a plan and its associated documentation aligned with operations, tactics, strategy and business…

</aside>

- **5 models are presented**
    - The **Strategic Alignment Model** and the **Amsterdam information Model**
        - show high level relationships that influence how the organisation manages data.
    - The **DAMA DMBOK Framework**
        - describes Data Management knowledge Areas and explains their visual representation within the DMBOK.
        - **DAMA Wheel**
        - **Hexagon and Context Diagram**
    - the final 2 are rearrangements of the DAMA wheel

### 3.1 Strategic Alignment Model 1999

![Screenshot 2024-05-28 at 09.20.33.png](Chapter%201%20Data%20management%20716abf8b89e844d9988c7fdd6bdf7465/Screenshot_2024-05-28_at_09.20.33.png)

### 3.2 Amsterdam Information Model 1997

![Screenshot 2024-05-27 at 14.27.41.png](Chapter%201%20Data%20management%20716abf8b89e844d9988c7fdd6bdf7465/Screenshot_2024-05-27_at_14.27.41.png)

### 3.3 The DAMA-DMBOK Framework

**The DAMA Wheel**

<aside>
💡 Governance in the center for consistency within and balance between the **knowledge areas**

</aside>

![Screenshot 2024-05-28 at 09.25.34.png](Chapter%201%20Data%20management%20716abf8b89e844d9988c7fdd6bdf7465/Screenshot_2024-05-28_at_09.25.34.png)

**The Environmental Factors Hexagon**

<aside>
💡 Relationships between **people, process and technology**, **GOALS and Principles** in the center.

</aside>

![Screenshot 2024-05-28 at 09.27.04.png](Chapter%201%20Data%20management%20716abf8b89e844d9988c7fdd6bdf7465/Screenshot_2024-05-28_at_09.27.04.png)

**Basic Environmental Elements**

1. **Goals & Principles**: directional business goals of each function and the fundamental principles that guides the performance of each function
2. **Activities**: Each function is composed of lower level activities. Some activities are grouped into sub-activities. Activities are further decomposed into tasks and steps
3. **Deliverables**: The information and physical database and documents created as interim and final outputs of each function. Some deliverables are essential, some are generally recommended, and others are optional depending on circumstances.
4. **Roles and Responsibilities**: The business and It roles involved in performing and supervising the function and the specific responsibilities of each role in that function. Many roles will participate in multiples functions

**Supporting Environmental Elements**

1. **Techniques**: Common a popular methods and procedures used to perform the processes and produce the deliverables. Practices and techniques may also include common convention, best practices recommendations and alternative approaches without elaboration
2. **Tools:** Categories os supporting technology(primary software tools), standards and protocols, product selection criteria and common learning curves
3. **Organisations and Culture**:
    1. Management Metrics: measures of size, effort, time, cost, quality…
    2. Critical succes factors
    3. Reporting Structures
    4. Contracting Strategies
    5. Budgeting and Related Resource allocation
    6. Team work and Group Dynamics
    7. Authority and Empowerment
    8. Shared Values and Beliefs
    9. Expectations and Attitudes
    10. Personal Style and preference Differences
    11. Cultural rites, Rituals and Symbols
    12. Organisational Heritage
    13. Change management recomendations

Each **knowledge Area** Context diagram was made up using the following Matrix:

| Data Management Functions | Goals and Principles | Activities | Primary deliverables | Roles and Responsabilities | Technology | Practices and Techniques | Organization and Culture |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Data Governance |  |  |  |  |  |  |  |
| Data Architecture Management |  |  |  |  |  |  |  |
| Data Development |  |  |  |  |  |  |  |
| Data Operations Management |  |  |  |  |  |  |  |
| Data Security Management |  |  |  |  |  |  |  |
| References and Master Data Management |  |  |  |  |  |  |  |
| Data Warehouse and Business Intelligence Management |  |  |  |  |  |  |  |
| Document and Content Management |  |  |  |  |  |  |  |
| Metadata Management |  |  |  |  |  |  |  |
| Data Quality Management |  |  |  |  |  |  |  |

**The DMBOK Version 2 generic Knowledge area context diagram**

![Screenshot 2024-05-28 at 10.56.53.png](Chapter%201%20Data%20management%20716abf8b89e844d9988c7fdd6bdf7465/Screenshot_2024-05-28_at_10.56.53.png)

- Activities that drive goals classified in 4 phases:
    - Planning - Strategic and tactical
    - Development activities - Organised around system lifecycle
    - Control Activities - ensure quality, integrity, reliability and security
    - Operational activities - support systems and processes

### 3.4 DMBOK Piramid (Aiken)

![Screenshot 2024-05-28 at 11.04.07.png](Chapter%201%20Data%20management%20716abf8b89e844d9988c7fdd6bdf7465/Screenshot_2024-05-28_at_11.04.07.png)

### 3.5 DAMA Data Management Framework evolved

<aside>
💡 Dama Functional Area dependencies, explore the relation between the knowledge areas

</aside>

- BI/Analytics depend on all the others
- DW and Master data depend on feeding system/applications
- system/applications Depends on reliable data quality, design and integration
- Governance is the foundation on which all functions dependent

![Screenshot 2024-05-28 at 11.06.23.png](Chapter%201%20Data%20management%20716abf8b89e844d9988c7fdd6bdf7465/Screenshot_2024-05-28_at_11.06.23.png)

<aside>
💡

DAMA Data Management Function Framework

</aside>

- Guide Purpose of data management → **deriving value from data assets**
- deriving value requires lifecycle management → Depicted in the center of the diagram
- Foundational activities support the lifecycle
- A data governance program provides oversight and containment, and enables the organisation to be data driven, as it puts in place the strategy and supporting principles, policies procedures and stewardship practices

![Screenshot 2024-05-28 at 11.09.36.png](Chapter%201%20Data%20management%20716abf8b89e844d9988c7fdd6bdf7465/Screenshot_2024-05-28_at_11.09.36.png)

<aside>
💡 Evolution of the DAMA Wheel: core activities surrounded by lifecycle and usage activities, within the structures of governance

</aside>

- Core activities in centre
- Surrounded by lifecycle and usage activities
- Lifecycle management: Plan and Enable
- Uses come from lifecycle activities
- Data Governance provides oversight and containment

![Screenshot 2024-05-28 at 11.27.53.png](Chapter%201%20Data%20management%20716abf8b89e844d9988c7fdd6bdf7465/Screenshot_2024-05-28_at_11.27.53.png)

**DM Functions and Data Lifecycle Management**

<aside>
💡 Relationships with additional content of the knowledge areas. Data management enables organisations to get value from their data. This require data lifecycle management, and these activities are in the centre of the diagram.

</aside>

<aside>
💡

A framework helps to understand data management comprehensively and see the relationships between component pieces. Frameworks are developed at different levels of abstraction and provide a range of perspectives

</aside>