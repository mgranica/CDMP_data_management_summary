# Chapter 14: Big data and Data Science

# 1. Introduction

- Generate, store and analyse larger amounts of data:
    - **BIG data**
        - Volume, variety and the velocity at which it is produced
    - **Data Scientists**
        - People how mine and develop predictive, machine learning and prescriptive models and analytics
    - **Data Science**
        - Applies data mining, statistical analysis and machine learning with data integration and data modelling to predict behaviours. Forward looking. BI describes past trends - rear-window view

![Screenshot 2024-06-26 at 16.07.14.png](Chapter%2014%20Big%20data%20and%20Data%20Science%202643978177be4451916db9983d4708b9/Screenshot_2024-06-26_at_16.07.14.png)

<aside>
💡 Different management and storage. Big data relies on ELT (Loading and then transforming). Is not stored in the relational model. Speed and volume of data requires different approaches to integration, metadata and data quality management

</aside>

## 1.1 Business Drivers

- The desire to discover and act on business opportunities through applying techniques on diversely generated data
- Data Science can improve operations
- Machine learning for automation of complex time-consuming activities

![Screenshot 2024-06-26 at 16.13.45.png](Chapter%2014%20Big%20data%20and%20Data%20Science%202643978177be4451916db9983d4708b9/Screenshot_2024-06-26_at_16.13.45.png)

## 1.2 Principles

<aside>
💡 Important to manage Metadata related to Big Data sources for inventory, their origins and value.

</aside>

## 1.3 Essential Concepts

### 1.3.1 Data Science

<aside>
💡 Developing predictive models that explore data content patterns. Based on hypothesis which may be statistically confirmed by historical data. Iterative inclusion of data sources into models that develop insights.

</aside>

- Data Science depends on:
    - **Rich data sources:** Potential to show otherwise invisible patterns in organisational or customer behaviour
    - **Information alignment and analysis:** Techniques to understand data content and combine data sets for meaningful patterns
    - **Information delivery:** Visualisations of results of insight gained from mathematical models
    - **Presentation of findings and data insights:** Presentation and sharing of insights

![Screenshot 2024-06-26 at 16.46.16.png](Chapter%2014%20Big%20data%20and%20Data%20Science%202643978177be4451916db9983d4708b9/Screenshot_2024-06-26_at_16.46.16.png)

### 1.3.2 The Data Science Process

<aside>
💡 Data Science follows the scientific method of refining knowledge by making observations and testing hypotheses, observing results and formulating theories to explain results. The output of each phase in the diagram is input to the next.

</aside>

![Screenshot 2024-06-26 at 16.46.06.png](Chapter%2014%20Big%20data%20and%20Data%20Science%202643978177be4451916db9983d4708b9/Screenshot_2024-06-26_at_16.46.06.png)

- **Define Big Data strategy and business needs:** Requirements that identify desired outcomes with measurable benefits
- **Choose data sources:** Identify gaps in current data base and find sources
- **Acquire and ingest data stores**
- **Develop Data Science hypotheses and methods**
- **Integrate and align data for analysis:** Data integration and cleansing for quality (Wrangling and Munging)
- **Explore data using models:**
    - Apply statistical analysis and machine learning algorithms
    - Validate, train and evolve model
    - New hypotheses may be introduced
- **Deploy and monitor:** Often becomes a warehousing project

### 1.3.3 Big Data

![Screenshot 2024-06-26 at 16.47.14.png](Chapter%2014%20Big%20data%20and%20Data%20Science%202643978177be4451916db9983d4708b9/Screenshot_2024-06-26_at_16.47.14.png)

- **Volume:** Amount – billions of records - >100 Terabytes
- **Velocity:** Speed at which data is captured, generated or shared – often analysed at real-time
- **Variety / Variability:** Forms data is captured or delivered
- **Viscosity:** How difficult the data is to use and integrate
- **Volatility:** How often the data changes
- **Veracity:** How trustworthy the data is

### 1.3.4 Big data Architecture Components

![Screenshot 2024-06-26 at 16.47.46.png](Chapter%2014%20Big%20data%20and%20Data%20Science%202643978177be4451916db9983d4708b9/Screenshot_2024-06-26_at_16.47.46.png)

### 1.3.5 Sources of Big Data

<aside>
💡 Internet of Things, email, social media, online orders, video games, phones, POS devices, surveillance systems, sensors, medical monitoring, satellites, military etc.

</aside>

### 1.3.6 Data Lake

<aside>
💡 An environment where a vast amount of data of various types and structures can be ingested, stored, assessed and analysed:

</aside>

- Environment for Data Scientists to mine and analyse data
- Central storage for raw data with minimal transformation
- Alternate storage for detailed historical data warehouse data
- Online archive for records
- Environment to ingest streaming data with automated pattern identification

<aside>
💡 Manage Metadata to prevent it to become a data swamp

</aside>

### 1.3.7 Services-Based Architecture

![Screenshot 2024-06-26 at 16.50.30.png](Chapter%2014%20Big%20data%20and%20Data%20Science%202643978177be4451916db9983d4708b9/Screenshot_2024-06-26_at_16.50.30.png)

<aside>
💡 also called Lambda architecture, referred in chap 5: Brewers Theorem

</aside>

- SBA provides immediate (maybe not complete or accurate) data. Updates complete, accurate historical data set using same source.
- SBA has # main components
    - **Batch layer:** A data lake, historical, structure-over-time component, every transaction is an **insert**
    - **Speed layer:** Only real-time data, Operational Data Store (ODS), all transactions are **updates** or **inserts**
    - **Serving layer:** Interface to join batch and speed layers, uses Metadata to determine where to **serve** the data

<aside>
💡 Data is loaded into both Batch and Speed layers simultaneously, creating a current state, and a history layer.

</aside>

### 1.3.8 Machine Learning

<aside>
💡 The construction and study of learning algorithms. Subfield of artificial intelligence

</aside>

- three types:
    - **Supervised learning:** Based on generalised rules e.g., separating SPAM emails
    - **Unsupervised Learning:** Identifying hidden patterns i.e., data mining
    - **Reinforcement learning:** Based on achieving a goal e.g., beating a chess opponent
- Ethical implications:
    - Transparency:
        - It is not clear how Deep Learning Neural Networks (DLNN) learn
        - Need to see how decisions are made

### 1.3.9 Sentiment Analysis

<aside>
💡 Looking for key words in semi-structured data using Natural Language Processing (NLP) to look for sentiment. Requires understanding of the meaning of a post.

</aside>

### 1.3.10 Data and Text Mining

<aside>
💡 **Data Mining** is an offshoot of machine learning that reveals patterns in data using algorithms. Unsupervised learning where algorithms are applied to a data set without knowledge of outcomes, to reveal patterns and relationships.

</aside>

<aside>
💡 **Text mining** analyses documents with text analysis and data mining techniques to classify content automatically into workflow guided and SME-directed ontologies.

</aside>

- Data and text mining techniques:
    - **Profiling:** Characterise behaviour norms of an individual, group or population for anomaly detection (e.g., fraud)
    - **Data reduction:** Make a similar smaller data set from a large one for easier analysis
    - **Association:** Unsupervised learning process to find relationships based on transactions
    - **Clustering:** Group elements by shared characteristics
    - **Self-organising maps:** Neural network method of cluster analysis by reducing dimensionality in the evaluation space. Also called Kohonen Maps or topologically ordered maps

### 1.3.11 Predictive Analytics

<aside>
💡 Subtype of supervised learning. The development of probability models based on variables related to possible events. When it receives some information, the model triggers a response by the organisation. I.E. a forecast

</aside>

### 1.3.12 Perspective Analytics

<aside>
💡 Prescriptive analytics anticipates what will happen, when it will happen and implies why it will happen. Shows implications of various decisions and can suggest how to take advantage of an opportunity or avoid a risk

</aside>

### 1.3.13 Unstructured Data Analytics

<aside>
💡 An iterative process of scanning and tagging to add hooks to unstructured data, to allow filtering and linking to related structured data.

</aside>

### 1.3.14 Operational Analytics

<aside>
💡 BI or streaming analytics

</aside>

### 1.3.15 Data Visualization

<aside>
💡 The process of interpreting concepts, ideas and facts by using pictures or graphical representations.

</aside>

### 1.3.16 Data Mashups

<aside>
💡 Combine data and internet-based services to create visualisation for insight and analysis.

</aside>

# 2 Activities

## 2.1 Define Big Data Strategy and Business Needs

- Must be aligned with overall business strategy
    - What problems does the organisation need analytics to solve?
    - What data sources to use or acquire?
    - The timeliness and scope of the data to provision
    - The impact on and relation to other data structures
    - Influences to existing modelled data

## 2.2 Choose data Sources

<aside>
💡 Big Data comes from many internal and external sources. Evaluate the Quality and reliability, and know its origin (provenance), format, what elements represent, how it connects to other data, and how frequently it will be updated.

</aside>

- Review available data sources, processes that creates the data, and manage the plan for new sources:
    - **Foundational data:** e.g., POS in sales analysis
    - **Granularity:** Most granular form is ideal
    - **Consistency:** Select data that appears appropriately and consistently across visualisations
    - **Reliability:** Use trusted, authoritative sources
    - **Inspect / profile new sources:** Test changes before adding new data sets
- risks:
    - privacy
    - filters which may introduce bias

## 2.3 Acquire and Ingest Data Sources

<aside>
💡 Capture critical Metadata about the source (origin, size, currency and additional knowledge about the content) when ingesting data sources into the Big Data environment. Ingestion engines may profile the data. Provides information on how to integrate with other data sets, such as Master Data or historical warehouse data, also how to train and validate models.

</aside>

## 2.4 Develop Data Hypotheses and methods

<aside>
💡 Data science entails building statistical models that find correlations and trends within and between data sets to find insights within the data. Models should be tested for a range of outcomes. Models depend on the quality of input data.

</aside>

## 2.5 Integrate / Algin Data for analysis

- Preparing data for analysis involves understanding what is in the data and links between data from various sources.
    - Daily data would have to be aggregated to link to monthly data
    - Common key
    - Similarity and record linking algorithms
    - Clustering used to determine groupings

## 2.6 Explore Data Using Models

- **Populate the Predictive Model**
- **Train the Model:** Repeated runs of the model against the data resulting in changes to the model
- **Evaluate the Model:**
    - Evaluated and validated against training sets
    - Ethical training to remove the biases of the creators
- **Create Data Visualisations:** Ensure the visualisation addresses the audience

## 2.7 Deploy and monitor

- Expose Insights and Findings
- Integrate with additional Data Sources

# 3 Tools

## 3.1 MPP (Massively Parallel processing) Shared-nothing technologies and architecture

<aside>
💡 A system that automatically distributes data and parallelises query workload across all available hardware

</aside>

- data is partitioned across multiple processing nodes each processing data locally. Communication is controlled by a master host and occurs over a network. There is no disk sharing or memory contention. Linearly scalable. Distribution of workload to processor level. Speeds up analytical functions.

![Screenshot 2024-06-26 at 17.10.12.png](Chapter%2014%20Big%20data%20and%20Data%20Science%202643978177be4451916db9983d4708b9/Screenshot_2024-06-26_at_17.10.12.png)

## 3.2 Distributed file-based databases

- Open source Hadoop stores files of any type
- Language used is called MapReduce:
    - **Map:** Identify and obtain data to be analysed
    - **Shuffle:** Combine data according to desired analytical patterns
    - **Reduce:** Remove duplication and perform aggregation to reduce the size of the data set to only what is required

## 3.3 In-database Algorithms

<aside>
💡 Each processor in an MPP Shared-nothing platform can run queries independently. Computation close to data reduces time for complex algorithms.

</aside>

## 3.4 Big data cloud solutions

<aside>
💡 Vendors provide cloud storage and enhancement

</aside>

## 3.5 Statistical computing and graphical languages

<aside>
💡 R – scripting language with statistical computing and graphics.

</aside>

## 3.6 Data visualisation tools

- **Traditional visualisation tools:** both data and graphical
- **Information graphics / Infographics:** Insights, changes in data over time. Interactive, sophisticated analysis, adherence to visualisation best practices

# 4 Techniques

- **Analytic Modelling:** Different depths of analysis:
    - **Descriptive modelling:** Summarises data structures in a compact manner
    - **Explanatory modelling:** statistical models for testing a hypothesis
- **Big Data Modelling:** Data needs to be integrated, specified and managed by applying traditional Enterprise Architecture principles

# 5 Implementation Guidelines

## 5.1 Strategy Alignment

Strategically aligned with business objectives. Documents goals, approach and governance principles. Strategy deliverables should account for managing:

- Information lifecycle
- Metadata
- Data Quality
- Data acquisition
- Data access and security
- Data governance
- Data privacy
- Learning and adoption
- Operations

## 5.2 Readiness Assessment / Risk Assessment

Critical success factors:

- **Business relevance:** Big Data/Data Science initiatives must enforce business function
- **Business readiness:**
    - Prepared for long term delivery?
    - Committed to establishing centres of excellence to sustain the product?
    - How broad is the skill gap?
- **Economic viability:** Assessment of ownership costs – buying vs leasing
- **Prototype:** Can the solution be prototyped?

## 5.3 Organisation and Culture change

Need a communications program to engage stakeholders and a centre of excellence to provide training, best practices, knowledge management and communication across developer, designer, analyst and data consumer communities.

Cross functional roles:

- **Big Data platform architect:** Hardware, OS, file systems and services
- **Ingestion architect:** Data analysis, systems of record, modelling
- **Metadata specialist:** Metadata interfaces, architecture and contents
- **Analytic Design Lead:** End user analytic design
- **Data Scientist:** Architectural and model design based on statistical knowledge

# 6 Big Data and Data Science Governance

<aside>
💡 The enterprise view of data should drive decisions on sourcing, sharing, metadata, enrichment and access

</aside>

## 6.1 Visualisation channels management

<aside>
💡 Alignment of the appropriate visualisation tools at the right level of complexity for the user community.

</aside>

## 6.2 Data Science and visualisation Standards

- Vital for customer-facing and regulatory-facing content:
    - Tools standards by analytic paradigm, user community, subject area
    - Requests for new data
    - Data set process standard
    - Processes to avoid biased results:
        - Data inclusion and exclusion
        - Assumptions in the models
        - Statistical validity of results
        - Validity of interpretation of results
        - Appropriate methods applied

## 6.3 Data Security

- Agree upon levels of access for authorised personnel
- Mask data for those not authorised
- Use encryption for highly sensitive data
- Recombination measures the ability to reconstitute sensitive or private data and must be managed
- Outcomes of analysis may violate privacy

## 6.4 Metadata

<aside>
💡 Managed as part of data ingestion else data lake becomes a swamp

</aside>

## 6.5 Data Quality

<aside>
💡 Data Quality is a measure of deviation from expected result, the smaller the difference the higher the quality. Mature Big Data organisations scan data inputs using data quality tools to understand the information within:

</aside>

- **Discovery:** Where information resided in the data set
- **Classification:** What type of information based upon standardised patterns
- **Profiling:** How data is populated and structured
- **Mapping:** What other data sets can be mapped to these values

## 6.6 Metrics

- **Technical Usage Metrics:**
    - Look for data hot spots to manage distribution and performance
    - Growth rates for capacity planning
- **Loading and scanning metrics:**
    - Ingestion rate
    - Interaction with the community
    - Provided by execution logs
- **Learnings and stories:**
    - Counts and accuracy of models and patterns
    - Revenue realised for identified opportunities
    - Cost reduction from avoiding identified threats