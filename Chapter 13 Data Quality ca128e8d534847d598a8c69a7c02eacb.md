# Chapter 13: Data Quality

# 1. Introduction

![Screenshot 2024-06-20 at 16.25.23.png](Chapter%2013%20Data%20Quality%20ca128e8d534847d598a8c69a7c02eacb/Screenshot_2024-06-20_at_16.25.23.png)

<aside>
💡 The value of data is that data is reliable and trustworthy → High data quality

</aside>

- Factors that contribute to poor quality data:
    - lack understanding of the effects of poor quality data on the decision-making process
    - Bad planning
    - Siloed system design
    - Inconsistent development processes
    - Incomplete documentation
    - A lack of standards
    - A lack of governance
    - Failure to define what makes data fit for purpose

<aside>
💡 High quality data should be the goal of all data management disciplines and they all contribute to the quality of data. Data Quality should be managed by a Data Quality program team. Data Quality is an enterprise program like Data Governance

</aside>

![Screenshot 2024-06-20 at 16.32.47.png](Chapter%2013%20Data%20Quality%20ca128e8d534847d598a8c69a7c02eacb/Screenshot_2024-06-20_at_16.32.47.png)

## 1.1 Business drivers

- Business drivers for establishing a Data Quality Program:
    - Increase value of business data and opportunities to use it
    - Reduce risks associated with poor quality data
    - Improve organisational efficiency and productivity
    - Protect and enhance the organisation’s reputation
- Direct costs associated with poor quality data include:
    - Inability to invoice correctly
    - Increased customer service calls and decreased ability to resolve them
    - Revenue lost due to missed opportunities
    - Delay if integration during mergers or acquisitions
    - Increased exposure to fraud
    - Loss due to bad business decisions driven by bad data
    - Loss of business due to poor credit standing

## 1.2 Goals and Principles

- General Goals:
    1. Develop a governed approach to make data fit for purpose based on data consumers’ requirements.
    2. Define **standards, requirements, and specifications** for data quality controls as part of the data lifecycle.
    3. Define and implement processes to measure, monitor, and report on data quality levels.
    4. Identify and advocate for opportunities to improve the quality of data, through process and system improvements.
- A data quality program should be guided by the following principles:
    - **Criticality:**
        - Focus on data most critical to the enterprise and its customers
    - **Lifecycle management:**
        - Manage data across data lifecycle from creation through disposal
    - **Prevention:**
        - Focus should be on prevention of data errors
    - **Root cause remediation:**
        - Don’t just correct errors, address the root cause
    - **Governance:**
        - Support from Data Governance activities
    - **Standards-driven**:
        - Define requirements as measurable standards
    - **Objective measurement and transparency:**
        - Measurement and methodology must be communicated to stakeholders
    - **Embedded in business processes:**
        - Business process owners must enforce data quality standards
    - **Systematically enforced:**
        - System owners must enforce data quality requirements
    - **Connected to service levels:**
        - Data quality reporting and issues management must be incorporated into SLAs

## 1.3 Essential concepts

### 1.3.1 Data Quality

<aside>
💡 Data is high quality when it meets the expectations and needs of data consumer
i.e. it is fit for the purpose to which they want to apply it

</aside>

### 1.3.2 Critical Data

- How to identify critical data. it is usually required by:
    - regulatory reporting
    - financial reporting
    - business policy
    - ongoing operations
    - business strategy, especially efforts at competitive differentiation
    - MASTERDATA is always critical, by definition

### 1.3.3 Data Quality dimensions

<aside>
💡 Data Quality Dimensions are measurable characteristics of data which form the basis for measurable rules

</aside>

- DAMA UK white paper identified 6 core dimensions:
    - **Completeness:**
        - Proportion of data stored against 100%
    - **Uniqueness:**
        - No entity instance recorded more than once
    - **Timeliness:**
        - Degree to which data represents reality at any point in time
    - **Validity:**
        - Data conforms to the syntax of its definition
    - **Accuracy:**
        - Degree to which data describes the real world
    - **Consistency:**
        - No difference found when comparing two or more representations of a thing to definitions
- Other useful measurable characteristic (Not listed as dimensions):
    - **Usability:**
        - Is the data understandable, simple, relevant, accessible, maintainable, and at the right level of precision?
    - **Timing issues:**
        - Is it stable yet responsive to legitimate change requests?
    - **Flexibility:**
        - Can it be repurposed? Is it easy to manipulate?
    - **Confidence:**
        - Are Data Governance processes in place? Is the data verified?
    - **Value:**
        - Good benefit case for the data? Is it being optimally used?

| Dimension of Quality | Description |
| --- | --- |
| Accuracy | Accuracy refers to the degree that data **correctly represents ‘real-life’ entities**. 
Accuracy is difficult to measure, unless an organization can r**eproduce data collection or manually confirm accuracy ofrecords**. 
Most measures of accuracy rely on **comparison to a data source that has been verified as accurate**, such as a system of record or data from a reliable source (e.g., Dun and Bradstreet Reference Data). |
| Complenteness | Completeness refers to **whether all required data is present**. 
Completeness can be **measured** at the **data set, record, or column level**. 
Does the data set contain all the records expected? Are records populated correctly? (Records with different statuses may have different expectations for completeness.) 
Are columns/attributes populated to the level expected? (Some columns are mandatory. Optional columns are populated only under specific conditions.) Assign completeness rules to a data set with varying levels of constraint: Mandatory attributes that require a value, data elements with conditional and optional values, and inapplicable attribute values. 
Data set level measurements may require comparison to a source of record or may be based on historical levels of population. |
| Consistency | Consistency can refer to **ensuring that data values are consistently represented within a data set and between data sets, and consistently associated across data sets**. 
It can also refer to the size and composition of data sets between systems or across time. Consistency may be defined between one set of attribute values and another attribute set within the same record (**record-level consistency**), between one set of attribute values and another attribute set in different records (**cross-record consistency**), or between one set of attribute values and the same attribute set within the same record at different points in time (**temporal consistency**). 
Consistency can also be used to refer to consistency of format. Take care not to confuse consistency with accuracy or correctness.
Characteristics that are expected to be consistent within and across data sets can be used as the basis for standardizing data. **Data Standardization** refers to the conditioning of input data to ensure that data meets rules for content and format. Standardizing data enables more effective matching and facilitates consistent output. Encapsulate consistency constraints as a set of rules that specify consistent relationships between values of attributes, either across a record or message, or along all values of a single attribute (such as a range or list of valid values). For example, one might expect that the number of transactions each day does not exceed 105% of the running average number of transactions for the previous 30 days. |
| Integrity | Data Integrity (or Coherence) includes ideas associated with completeness, accuracy, and
consistency. In data, integrity usually refers to either **referential integrity** (consistency between data objects via a reference key contained in both objects) or **internal consistency** within a data set such that there are no holes or missing parts. Data sets without integrity are seen as corrupted, or have data loss. Data sets without referential integrity have ‘**orphans**’ – invalid reference keys, or ‘**duplicates**’ – identical rows which may negatively affect aggregation functions. The level of orphan records can be measured as a raw count or as a percentage of the data set. |
| Reasonability | Reasonability asks whether a **data pattern meets expectations**. For example, whether a distribution of sales across a geographic area makes sense based on what is known about the customers in that area. Measurement of reasonability can take different forms. For example, reasonability may be based on comparison to benchmark data, or past instances of a similar data set (e.g., sales from the previous quarter). Some ideas about reasonability may be perceived as subjective. If this is the case, work with data consumers to articulate the basis of their expectations of data to formulate objective comparisons. Once benchmark measurements of reasonability are established, these can be used to objectively compare new instances of the same data set in order to detect change. (See Section 4.5.) |
| Timeliness | The concept of data Timeliness refers to several characteristics of data. Measures of timeliness need **to be understood in terms of expected volatility** – **how frequently data is likely to change and for what reasons.** Data currency is the measure of whether data values are the most up-to-date version of the information. Relatively static data, for example some Reference Data values like country codes, may remain current for a long period. Volatile data remains current for a short period. Some data, for example, stock prices on financial web pages, will often be shown with an as-of-time, so that data consumers understand the risk that the data has changed since it was recorded. During the day, while the markets are open, such data will be updated frequently. Once markets close, the data will remain unchanged, but will still be current, since the market itself is inactive. **Latency measures the time between when the data was created and when it was made available for use**. For example, overnight batch processing can give a latency of 1 day at 8am for data entered into the system during the prior day, but only one hour for data generated during the batch processing. (See Chapter 8.) |
| Uniqueness/deduplication | Uniqueness states that **no entity exists more than once within the data set**. Asserting uniqueness of the entities within a data set implies that a key value relates to each unique entity, and only that specific entity, within the data set. Measure uniqueness by testing against key structure. (See Chapter 5.) |
| Validity | Validity refers to whether **data values are consistent with a defined domain of values.** A **domain of values may be a defined set of valid values** (such as in a reference table), a range of values, or value that can be determined via rules. The data type, format, and precision of expected values must be accounted for in defining the domain. Data may also only be valid for a specific length of time, for example data that is generated from RFID (radio frequency ID) or some scientific data sets. Validate data by comparing it to domain constraints. Keep in mind that data may be valid
(i.e., it may meet domain requirements) and still not be accurate or correctly associated with
particular records. |
- **Relationship between data quality dimensions an data quality concepts:**
    
    ![Screenshot 2024-06-20 at 16.55.38.png](Chapter%2013%20Data%20Quality%20ca128e8d534847d598a8c69a7c02eacb/Screenshot_2024-06-20_at_16.55.38.png)
    

*Relationship between Data Quality Dimensions, Underlying Concepts and Metrics (Author Unknown)*

![Screenshot 2024-06-20 at 16.57.33.png](Chapter%2013%20Data%20Quality%20ca128e8d534847d598a8c69a7c02eacb/Screenshot_2024-06-20_at_16.57.33.png)

## 1.4 Data Quality and metadata

<aside>
💡 Metadata defines what data represents. A Metadata repository can house the results of data quality measurements se that they can be shared and expectations clarified

</aside>

## 1.5 Data Quality ISO Standard

<aside>
💡 **ISO 8000** is the international standard for data quality. ISO 8000 defines the characteristics that can be tested by any organisation in the data supply chain to objectively determine conformance.

</aside>

<aside>
💡

ISO 8000 defines quality data as “**portable data that meets stated requirements**”. Portable means that the data can be separated from a software application. Stated requirements must be clearly defined.

</aside>

## 1.6 Data Quality Improvement Lifecycle

<aside>
💡 Approach data quality improvement based on the technique of quality improvement in physical products. Outputs from one process become input to other processes and can impact data quality. Use “PLAN-DO-CHECK-ACT” from problem solving model

</aside>

![Screenshot 2024-06-20 at 17.10.45.png](Chapter%2013%20Data%20Quality%20ca128e8d534847d598a8c69a7c02eacb/Screenshot_2024-06-20_at_17.10.45.png)

- **Plan Stage**:
    - Data Quality team assesses scope, impact and priority of known issues, and evaluates alternatives to address them at the root cause
- **Do/deploy stage**:
    - Data Quality team leads efforts to **address issues at the root cause** and plans for ongoing monitoring of data
- **Check stage**:
    - **Actively monitor data against standards**. If data falls below, act to bring it to acceptable levels
- **Act stage**:
    - Activities to address emerging data issues. The cycle restarts

## 1.7 Data Quality Business Rule Types

<aside>
💡 Data Quality Business Rules describe how data should exist in order to be useful within the organisation. implemented in software or data entry templates

</aside>

- Common business rule types:
    - **Definitional conformance:**
        - Data definitions used properly across organisation
    - **Value presence and record completeness:**
        - Rules for acceptability of missing values
    - **Format compliance:**
        - Values have a pattern e.g., phone numbers
    - **Value domain membership:**
        - Exists in a defined data domain. (Master and reference data)
    - **Range conformance:**
        - Within a defined range of values
    - **Mapping conformance:**
        - Maps to a domain (Reference data)
    - **Consistency rules:**
        - Maintain a relationship between two attributes based on the values
    - **Accuracy verification:**
        - Compare value to trusted source
    - **Uniqueness verification:**
        - Specify which entities must have unique representation. Primary key
    - **Timeliness validation:**
        - Characteristics associated with expectations for accessibility and availability of data, and also when it was last updated

## 1.8 Common Causes of Data Quality Issues

<aside>
💡 Data Quality issues can arise at any point in the data lifecycle, and may have multiples causes: Data entry, data processing, system design and manual intervention in automated processes.

</aside>

### 1.8.1 Issues Caused by Lack of Leadership

- Barriers to effective manage data quality:
    - Lack of awareness on the part of leadership and staff
    - Lack of business governance
    - Lack of leadership and management
    - Difficulty in justification of improvements
    - Inappropriate or ineffective instruments to measure value
        
        ![Screenshot 2024-06-20 at 17.20.12.png](Chapter%2013%20Data%20Quality%20ca128e8d534847d598a8c69a7c02eacb/Screenshot_2024-06-20_at_17.20.12.png)
        

### 1.8.2 Issues Caused by Data Entry Process

- **Data entry interface issues**: Have edits and controls to prevent input of incorrect data
- **List entry placement**: Order of values in a dropdown list
- **Field overloading**: Reusing fields for different business purposes over time creates confusion
- **Training Issues**: Process knowledge. Awareness of the impact of incorrect data. Incentivise for accuracy, not speed
- **Changes to business processes**: New business rules and data quality requirements need to be incorporated into systems
- **Inconsistent business process execution**: Will produce inconsistent data

### 1.8.3 Issues Caused by Data Processing Functions

- **Incorrect assumptions about data sources**: Not enough known about data sources, details are missed due to poor documentation or inadequate knowledge transfer
- **Stale business rules:** Business rules may change over time, and should be periodically reviewed
- **Changed data structures:** Source system structure changes without informing downstream consumers

### 1.8.4 Issues Caused by System Design

- **Failure to enforce referential integrity**:
    - Duplicate data that breaks uniqueness rules
    - Orphan rows, in some reports and not others, leading to different values for the same calculation
    - Inability to upgrade due to restored or changed referential integrity requirements
    - Inaccurate data due to missing data being assigned default values
- **Failure to enforce uniqueness constraints:** Multiple copies result in overstated aggregation
- **Coding inaccuracies and gaps:** Data mapping or rules for processing incorrect
- **Data model inaccuracies:** Assumptions in data model must be supported by actual data
- **Field overloading:** Reusing fields can also cause structural problems like incorrectly assigned keys, as well as confusing values
- **Temporal data mismatches:** Need a consolidated data dictionary
- **Weak Master Data Management:** Choose unreliable data sources
- **Data duplication:** Two main types:
    - **Single source – Multiple Local instances:** e.g., Instances of the same customer in multiple tables
    - **Multiple sources – Single Instance:** Data instances with multiple authoritative sources

### 1.8.5 Issues Caused by Fixing Issues

- Manual data patches directly to database. Most change the data in place, and can only be undone by a database restore.

## 1.9 Data Profiling

<aside>
💡 Data Profiling is a form of data analysis used to **inspect the data and assess data quality.** Profiling engine produces statistics that can be analysed to indentify patterns in data content and structure

</aside>

- **Counts of NULLS:** Inspect to see if they are allowed
- **Max/Min value:** Identifies outliers
- **Max/Min Length:** Outliers in fields for specific length values
- **Frequency distribution** of values for individual columns
- **Data Type and Format:** Non-conformance or unexpected formats

## 1.10 Data Quality and Data Processing

### 1.10.1 Data Quality and Data Processing

<aside>
💡 Data cleansing or scrubbing transforms data to conform to data standards or domain rules. Detecting and correcting errors.

</aside>

- The need for data cleansing can be addressed by:
    - Implementing controls to prevent data entry errors
    - Correcting the data in the source system
    - Improving the business processes that create data

### 1.10.2 Data Enhancement

Data enhancement or enrichment is the process of a**dding attributes to data to increase its quality or usability.**

- **Time/Date Stamp:** Root cause analysis to isolate the timeframe of the issue
- **Audit data:** Adds lineage for historical tracking and validation
- **Reference vocabularies:** Enhance understanding and control
- **Contextual information:** Tagging
- **Geographic information:** Address standardisation and geocoding
- **Demographic information:** Customer data enhanced through demographic information
- **Psychographic information:** Segment target populations by behaviours
- **Valuation information:** Asset valuation, inventory and sale

### 1.10.3 Data parsing and formatting

<aside>
💡 Data Parsing is the process of analysing data using predetermined rules to define its content or value

</aside>

### 1.10.4 Data Transformation and Standardisation

<aside>
💡 Rule based transformations map data values in their original formats and patterns into target representation. Standardisation employs rules that capture context, linguistics and idioms recognised as common over time.

</aside>

# 2. Activities

## 2.1 Define High Quality data

<aside>
💡 High quality data is fit for purpose of data consumers. Understand business needs, define terms, identify pain points and start to find consensus about drivers and data quality priorities. Ask questions of stakeholders th determine the understanding of the business benefits of high-quality data and the impact of poor quality data

</aside>

- understand the current state of data quality:
    - Understand business strategy and goals
    - Pain points, risks and business drivers
    - direct assessment of data (profiling)
    - Documentation of data dependencies in business process

<aside>
💡 Prioritise opportunities based on benefits to the organisation

</aside>

## 2.2 Define data quality strategy

<aside>
💡 Data quality priorities must align with business strategy

</aside>

- develop a framework which includes methods to:
    - understand and prioritise business needs
    - identify data critical to business needs
    - define business rules and data quality standards based on business requirements
    - Assess data against expectations
    - share findings and get feedback from shareholders
    - prioritise and manage issues
    - identify and prioritise opportunities for improvement
    - measure, monitor and report on data quality
    - manage metadata produced through quality processes

## 2.3 Identify Critical data and Business rules

- Critical data
    - If it were of higher quality, it would provide greater value
    - regulatory requirements
    - financial value
    - direct impact to customers
    - start with master data
    - ranked list of data for Data Quality team
- business rules
    - Describe expectations about the quality of the data
    - often not documented - need to reverse engineer
    - how data is collected or created
    - measurements describe if data is fit for use
    - discovery and refinement of rules is an ongoing process

## 2.4 Perform an Initial Data Quality Assessment

<aside>
💡 query the data to understand content and relationships. data stewards, SMEs, data consumers and Data Quality analysts prioritise finding

</aside>

- the goal of the initial assessment is to learn about the data to make an actionable plan for improvement:
    - define goals to drive the work
    - identify data to be assessed. start small
    - identify uses of theta and consumers of the data
    - identify known risks of the data
    - inspect data based on known and proposed rules
    - document levels of non-conformance and types of issues
    - perform in depth analysis to prioritise issues and develop root cause hypotheses
    - Confirm issues and priorities with stakeholders
    - planning

## 2.5 Identify and prioritise Potential Improvements

- Prioritise actions based on business impact
- Develop preventative and corrective actions
- Confirm planned actions with stakeholders
- Large-scale profiling efforts should focus on the most critical data
- Profiling identifies issues, but not root causes

## 2.6 Define Goals for data Quality Improvement

- quick hits as well as long term strategic changes
- address root causes
- set achievable goals based on quantification of the business value of Data Quality improvements
- determine ROI of fixes of issues based on
    - criticality of the data
    - amount of affected data
    - number and type of business processes impacted
    - No of stakeholders affected
    - associated risks
    - cost of root cause remediation
    - cost of work arounds

## 2.7 Develop and deploy data quality operations

### 2.7.1 Manage data quality rules

- Define rules upfront to
    - set clear expectations
    - provide requirements for edits and controls to prevent data issues from being introduced
    - provide Data Quality requirements to vendors
    - foundation for Data Quality measurement
- Data Quality rules should be managed as metadata and should be:
    - **Documented consistently** templates
    - **Defined in terms of data quality dimensions** help people understand what is being measured
    - **Tied to business impact** connect standards and rules to organisational success
    - **backed by data analysis** test rules on actual data
    - **confirmed by SMEs**
    - **Accessible to all data consumers**

### 2.7.2 Measure and monitor data quality

- tow reasons to implement operational data quality measurements:
    - to inform consumers about levels of quality
    - manage risk that may be introduced by technical or business changes
- express as a percentage where (r) is the rule being tested
    
    ![Screenshot 2024-06-25 at 13.09.14.png](Chapter%2013%20Data%20Quality%20ca128e8d534847d598a8c69a7c02eacb/Screenshot_2024-06-25_at_13.09.14.png)
    
    ![Screenshot 2024-06-25 at 13.09.55.png](Chapter%2013%20Data%20Quality%20ca128e8d534847d598a8c69a7c02eacb/Screenshot_2024-06-25_at_13.09.55.png)
    
- Measurements can be taken at three levels of granularity:
    
    
    | Granularity | in-stream treatment | Batch treatment |
    | --- | --- | --- |
    | Data element | Edit checks in application
    Data element validation services
    Specially programmed applications | direct queries. 
    data profiling or analyser tool |
    | Data reccord | Edit checks in application
    Data record validation services
    Specially programmed applications | direct queries. 
    data profiling or analyser tool |
    | Data set | Inspection inserted between processing stages | direct queries. 
    data profiling or analyser tool |

### 2.7.3 Develop operational procedures for managing data issues

<aside>
💡 The data quality team respond to issues timorously and effectively. design and implement operational procedures for:

</aside>

- **Diagnosing issues** root cause analysis requires input from technical and business SMEs
    - review issues in context of processing flows to isolate point where flaw is introduced
    - evaluate whether there been environment changes that could have caused errors
    - evaluate whether other process issues contributed
    - determine whether there are issues whit external data that could have affected this data
- **Formulating options for remediation** based on diagnosis, evaluate alternatives for addressing the issues:
    - /Non-technical such as lack of training, leadership, support, accountability
    - modification of systems to eliminate root causes
    - developing controls to prevent issue
    - additional inspecting and monitoring
    - directly correcting flawed data
    - take no action based on cost and impact of correction versus the value of data correction
- **Resolving issues** Data quality team and business data owners determine the best way to solve issues

**Incident tracking system usage example**

- Standardize data quality issues and activities
- provide an assignment process for data issues
- manage issue escalation procedures
- manage data quality resolution workflow

### 2.7.4 Establish data Quality Service Level Agreements

<aside>
💡 Data Quality Service level agreements (SLA) specifies the organisation’s expectation for response and remediation for data quality issues in each system. the SLA defines roles and responsabilities associated with performance data quality procedures

</aside>

- SLA establish time limits for notification generation, the names in the management chain and when escalation should occur
- SLA reporting can be scheduled or driven by business

### 2.7.5 Develop data quality reporting

- reporting should focus around:
    - DQ Scorecard
    - DQ trends
    - SLA metrics
    - DQ Issue management focussing on the status of issues and resolutions
    - Conformance of the DQ team to governance policies
    - Conformance of IT and business teams to DQ policies
    - Positive effects of improvement projects

# 3. Tools

- **Data Profiling Tools**
    - produce high level statistics to identify patterns in the data
    - perform initial assessment of data quality
    - enable assessment of large data sets
- **Data Queuing tools**
    - Query more deeply to answer questions raised by profiling
- **Modelling and ETL tools**
    - Can improve quality if used with the data in mind
    - can be detrimental to data if used without knowledge of the data
- **Data Quality Rule templates**
    - metadata repositories: definitions of high quality data is metadata

# 4. Techniques

## 4.1 Preventative actions

- ways to prevent poor quality data entry an organisation
    - establish data entry controls:
        - data entry rules
    - train data producers
        - value accuracy rather than speed
    - define and enforce rules
        - create a data firewall, a table with all the business rules, to check quality before the data is used
    - Demand high quality data from data suppliers
        - Examine processes to check structures, data sources and provenance
    - Implement data governance and stewardship
        - define roles and responsabilities
    - institute formal change control
        - ensure changes are tested before implementing

## 4.2 Corrective Actions

- **Automated correction**
    - Rule based standardisation, normalisation and correction
    - No manual intervention
    - Requires environmental with well-defined standards, rules and known error patterns
- **Manually-driven correction**
    - Use automated tools with manual review before committing modified values to persistent storage
    - environment where data sets require human oversight, e.g. MDM
- **Manual Correction**
    - Best done through an interface with controls and edits which produces an audit trail
    - avoid making manual corrections directly to the production environment

## 4.3 Quality check and audit code modules

<aside>
💡 Create shareable, linkable and reusable quality check modules that developers can get from a library

</aside>

## 4.4 Effective data quality metrics

- Characteristics of informative metrics
    - Measurability
    - Quantifiable within a discrete range
    - Business relevance
    - Correlate with the influence of the data on the key business expectations
    - acceptability
    - data meets business expectation based on acceptability thresholds
    - accountability/stewardship
    - understood and approved by key stakeholders
    - controllability
    - should trigger an action to improve data
    - trending
    - measure data quality over time

## 4.5 Statistical Process Control

<aside>
💡 Method to manage processes by analysing measurements of variation in process inputs, outputs or steps

</aside>

- a process is a series of steps to turn inputs to outputs. SPC is based on the assumption that when a process with consistent inputs is executed consistently it will produce consistent outputs
- uses measures of central tendency (mean, median ,mode) and variability around a central value (range, variance, standard deviation) to establish tolerances for variances within a process
- two types of variance:
    - common causes:
        - inherent in the process
        - process is in statistical control when only common causes and range of variation is establish
    - spacial causes: unpredictable or intermitten

<aside>
💡 SPC uses for control, detection and improvement. Early detection of unexpected variation simplifies root cause investigation

</aside>

![Screenshot 2024-06-25 at 15.50.24.png](Chapter%2013%20Data%20Quality%20ca128e8d534847d598a8c69a7c02eacb/Screenshot_2024-06-25_at_15.50.24.png)

## 4.6 Root Cause Analysis

- common techniques
    - Pareto analysis (the 80/20 rule)
    - Fishbone diagram analysis
    - Track and trace
    - Process analysis
    - Five Whys (McGilvray, 2008)

# 5.  Implementation guidelines

<aside>
💡 improving Data quality in an organisation requires changing how the people think and behave towards data.

</aside>

- plan for implementing Data Quality:
    - **Operating mode for IT/Business interactions:**
        - Business people know how important the data is and IT can translate definitions of data quality into queries that identify records which don’t comply
    - **Changes in how projects are executed:**
        - Identify issues early and build data quality expectations into projects
    - **Changes to business processes:**
        - DQ team assesses processes and recommends changes
    - **Funding for remediation and improvement projects:**
        - Document costs and benefits of fixing data so that it can be prioritised
    - **Funding for DQ operations:**
        - Ongoing monitoring, reporting and fixing DQ issues

## 5.1 Readiness Assessment / Risk Assessment

- consider the following to asses the organisational readiness to accept data quality practices
    - **Management commitment to managing data as a strategic asset:**
        - How much do they know about data as an asset, risks of poor-quality data, importance of data governance?
    - **The organisation’s current understanding of the quality of its data:**
        - Pain points – helps identify and prioritise improvement projects
    - **The actual state of the data:**
        - Profiling, analysis and quantification of known pain points
    - **Risks associated with data creation, processing or use:**
        - Identify what can go wrong, and the potential damage to the organisation
    - **Cultural and technical readiness for scalable data quality monitoring:**
        - Requires a good collaborative relationship between IT and business teams

## 5.2 Organisation and cultural change

Promote awareness of the role and importance of data in the organisation.

All employees raise DQ issues, ask for good quality data as consumers, and provide good quality data to others. Every person who touches the data can impact its quality.

Employees need to think and act differently to produce and manage better quality data. This requires training focussing on:

- Common causes of data problems
- Relationships and why DQ requires an enterprise approach
- Consequences of poor quality data
- Necessity for ongoing improvement
- Becoming data lingual
- Introduce process changes

# 6. Data Quality and Data Governance

<aside>
💡 A data quality program is more effective when part of a data governance program

</aside>

## 6.1 Data Quality Policy

- all data management knowledge areas require a data policy, especially if they touch on regulatory areas
    - purpose, scope and applicability of the policy
    - definition of terms
    - responsabilities of the data quality program
    - responsabilities of other stakeholders
    - reporting
    - implementation of the policy, including links to risk, preventative measures, compliance, data protection and data security

## 6.2 Metrics

- High level categories of DQ metrics:
    - Return on investment
    - Levels of quality
    - Data Quality trends
    - Data issue management metrics
    - Conformance to service levels
    - Data Quality plan rollout

# Bonus

- **data quality oversight board** roles
    - establish communications & feedback mechanisms
    - Producing certification & compliance policies
    - Setting data quality improvement priorities
    - developing and maintaining data quality
    - **NO → data profiling & analysis**