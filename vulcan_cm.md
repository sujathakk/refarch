# Vulcan Capabilties

## Definition

A capability is an ability that an organization, person, or system possesses. [src](https://pubs.opengroup.org/architecture/togaf9-doc/arch/chap03.html#tag_03_30)

Capabilities are unique, atomic, and can only exist once in an     
organization


## Attributes

###  1. Maturity (Yes - Required)

While maturity for capabilities is fine in helping to drive planning, maturity is best suited as an attribute of the relationship between a capability (logical) and technology/product (physical) and belongs on the product side of the relationship. Discover's metadmodel may require it be associated with a capability. Further complicating maturity at a capability level is that a capability may be satisfied by numerous products. The figure below is a good representation of the different levels and is not to dissimilar to that from another common capability maturty model (CMM)


|  | **Basic** | Intermediate | Advanced| Avant-garde |
| ----| ----| -----| -----| -----|
| Technique | Prompt engineering | Feature Engineering, Transfer learning, Fine tuning | RAG | Self-trained models ,Reinforcement Learning HF| 
| Models| Light LLMs, Opensource LLMs (Hugging face) | LLMs ( Amazon Bedrock )| DFS's own embedded model and vector DB | Diffusion, (Amazon Sagemaker)|
| Applications | Chatbots, Workflow tools and agents | Modeling, Code generation| GenAI virtual agents|  Propriterary DFS models, DFS Mechanical Turks|
| Data | Pdfs, Texts, jpgs | DFS databases RDBMS, Nosql | RAG - Vector db, embedded db, Graph DB | Scalable vector db|
| Problem averted | Hallunication mgmt, Basic chat | Provenance detectors | Bias and Variance | User-in-loop | 
|Time-frame | 1-3months | 1-3 years | 5-10 years| 10+ years|
| Organizational Support| | | | |
| Feature availability| | | | |
| Testing | | | | |
| Engineering maturity| | | | |
| Financials | | | | 

![](images/ITCMF2.png)
<!--
    ALthough assessing maturity is somewhat subjective it should include in addition to the qualities listed in the above figure, the following:

    * Organizational Support - is there an adequately staffed and skilled production team. Are the operational processes in place?
    * Feature Availability - where is the product in the crawl, walk, run lifecycle, i.e. is the product in a pilot, limited availability, MVP stage
    * Testing - how sophisticated is testing, including but not limited to performance, functional & failure tests
    * Engineering Maturity - while products may support a great degree of non-functional robustness, itn hybrid/multi-cloud architectures this often takes significant 
      engineering effort
    * Financials - are the financial conducive to a broad adoption, or is contained to specific limited use cases  -->


### 2.	Disposition (No)
This is included here for clarity given all the debate around this quality. Unlike technologies and products which have a disposition, annotating capabilities with such a status is not meaningful. Capabilities are generally very static than the technologies and products that implement them.
| **Responsibilites** | Security | Governance| Compliance and Risk |
| --| ---| --| --|
| Transparency and Trustworthy| Safe and Protected | Well managed | Regulatory workloads|
| Transparent <br/> Fairness<br/> Explainability <br/> Controllability <br/> | Threat detection<br/>  Vulnerability management<br/> Infrastructure protection<br/> Prompt injection<br/>   | AI board<br/> GenAI council <br/> Roles and Responsibilities<br/> implementation <br/> | Policies and Procedures<br/> Monitoring <br/> Privacy, Bias, Misinformation <br/> Dynamic and Adaptable<br/> |

### 3.	Dependencies (Yes - Optional)
Ideally capabilities are exclusive of other capabilities but there may be times that they may have a dependency on other capabilities
Responsibilities
* Ethical concerns
* User control
* Legal constraints
* AI responsibilities

### 4.	Level (Yes – Required)
Given a target of 4 levels of granularity at most, only the leaf capabilities do not have subs, i.e. L0->L1->L2-L3, so both L0,L1 & L2 would have subs or be composites.
#### Level 1
| Capability| Description | Assessment |
| --------| --------| ------|
|Text Generation | SMS alerts, Emails, Social media posts <br/>| Auto generation of headlines and customized communication alerts to customers |
| Image, Video, Gif generation | AI generated images for latest news, offers  | Posters and Placards with mascot, spokesperson |
| Summarization | Meetings auto transcribed and sent as MOM after everymeeting <br/>New ACTs, laws, regulations, policy changes summarized | New legal updates related to work being summaried automatically|
| Q&A | General chatbot to answer DFS internal questions and answers |  Use DFS data - sharepoint, DTA, Servicenow, Dlife, emails, local drives , shared drives| 
#### Level 2
| Capability| Description | Assessment |
| --------| --------| ------|
| Chat bot | Customer aiding chatbots  | to use both public and dfs customer data |
| Prompt activated Report, Graphs | Auto generated tableau reports <br/> Self progress tracking  | eg. Send end of month accomplishments and missed deadlines <br/> Auto blocking calendars |
| Customer Personal assistant - | Money mgmt , investment alerts, pay bills | Track insurance, vehicle renewals, deposits, holiday savings  |
| Biometrics integration | Voice activated approvals, denials  | 1 touch payment, report etc., |

#### Level 3
| Capability| Description | Assessment |
| --------| --------|------|
|Coding assistant | Scanning, Debugging, text-to-code | |
| Testing assistant | ADA testing, Device testing, Fwd/Bwd compatability testing | |
| Demo video generation | Auto generated commercials, reels and shorts about new offers | | 
| Discover Virtual human agent | Personalized VR agent for every customer|

### 5.	Description (Yes – Required)
General description of the capability, absolutely no references to technology or products

### 6.	Owner (Yes – Optional)
Owner of the capability. Owner is best suited to the technology/product implementing the capability. Discover’s metamodel may require this.

### 7.  Uplift (Yes - Required)
Uplift indicates of the capability needs investment (funding, people) in support of a business intiiative/strategy. Like maturity, specifying uplift for a capability is fine where there is a one to one relationship between capability and technology/product but better suited on the product side of the relationship

### 8.  Financials (Yes - Required)
Like maturity, financials is best suited to the technology/product implementing the capability. Where there is a one to one relationship  articulating for the capability is fine. Financials can articulate whether new funding is required based on it being required in supoort of business initiative/strategy. Discover’s metamodel may require this.

## Capability Creation Guidance

1.	Capabilities are nouns

2.	Capabilities are unique, atomic, and should only exist once in an     
    organization. Pillars may need to coordinate as some capabilities could make sense in multiple domains

3.	Capabilities may be delivered by more than 1 technology/product

4.	Organization structure does not affect capabilities and your     
    capability layout should not mimic that of the supporting org

5.	Target no more than 3 to 4 levels of capabilities, i.e. getting to  
    granular will be hard to manage and often doesn’t add additional value/clarity
    
6.  Align top level capability (L0) in a hierarchy/map to a domain level  
    (e.g. Hybrid Cloud Network/App Observability)

7. LeanIX is the system of record and owns the [datamodel](https://discoverfinancial.sharepoint.com/:p:/s/EnterpriseArchitectureTool-LeanIX/EaTqdgoW5dxClW2LgZ_jeYABy3pGTuJ-lIfbBB6vybN2cg?e=v5j9cm)

7.	Keep it as simple as possible, the more detail you add may add short 
    term clarity but will ultimately not be maintainable, adding confusion down the road.

## Capability Uses

Figure below highlights how capabilities are intended to be used. 

  ![](images/capability-relationships.png)

### Capability Maps

Capability Maps have numerous uses:

* Used and owned by the business to layout business capabilities that can be leveraged to evaluate the degree to which the capabilities support the business strategy 

* Generated within Discover's Architecture Strategy and Innovation capability maps are used to illustrate enterprise technical capabilities provided within a technology domain 

* Depict maturity across numerous sectors, including but not limited to engineering/operational maturity. Maturity provides justification for prioritization & funding where capability uplift is targeted, usually in support of business initiatves/strategy

For clarity capability maps should limit subs to two levels

Dependencies and composition should be avoided in this view

TODO: Does LeanIX provide a widget/visualization?

![](images/capability-map.png)


*Aggregated to TSI Pillar*

 ![](images/capability-map-pillar.png)
 

### Capability Tree

A capability tree will be created for each Technology Domain within Discover's TSI pillars. Capabilty trees  are different than capability maps in the following ways:

* They fully depict all sub-capabilities

* Dependencies and composition if they exist should be depicted in this  
  view

* May optionally show implementing technology/products (software in 
  LeanIX)

* May optionally show realtionship to business capabilities   

TODO: Check on the visualization capabilities within LeanIX


### Reference Architecture

  * A capability is the primary reason for the existence of the domain

  * Each capability is foundational to the rest of the sub capabilities, technology and processes

  * A capability is architectural governed by a [Reference Architecture]; for which all implementation of said capability are correlated

  * Template for reference architecture can be found [here](https://github.discoverfinancial.com/entarch-org/technology-strategy-innovation/blob/master/templates/reference-architecture-template.md) and examples can be found [here](https://github.discoverfinancial.com/entarch-org/technology-strategy-innovation/tree/master/reference-architectures)

  * TSI repository will be source of completed reference architectures

  
### Reference implementations

  * Technology and processes are the implementation of a capability

  * Each technology and/or processes combination is documented as a   
    Reference Implementation
  
### Technology Radars

  * A technology radar will be created for each technology and/or process combination

  * Feature/Technology exploration: A developer seeking to leverage a capability would look to the tech radar for a technology/process and research feature sets within those products

  * Technology Radars will be generated within LeanIX

### Strategies

  * A technology domain has a strategy that is inclusive of the capabilities/sub

  * [TSI repository](https://github.discoverfinancial.com/entarch-org/technology-strategy-innovation/tree/master/strategies) will be source of completed technology strategies


### Capability Base Planning

1. Capability Analysis

  * Maturity Ratings: Each mapped capability is given a maturity rating against a defined benchmark (e.g. DFS Runway Criteria; operational excellence/etc.). Benchmarks are 'scored' for maturation of a capability.

  * Matrix: A matrix is created for to address each benchmark per capability. How a capability scores within a benchmark against ATS required maturity of a capability.

  * Funding: Given the business capability alignment (perceived value of the capability) and the current matrix; ATS can easily express the necessity of funding or not funding a particular capability with dollar amount X.

2. Business Capability Alignment
  * Aligned to ATS domains/capabilities and puts additional requirements of technology and process on the capability/sub. This then impacts the maturity rating and matrix; thus helps to justify need for added technology/processes. Business capabilities can also provide no impact if technology/process are already addressed within capability/sub.

3. Strategy
  * The alignment of business capabilities to ATS domain ensures the domain's strategy is inclusive/considerate of the business capabilities' strategy and/or roadmap. 

## References

Open Group: https://pubs.opengroup.org/architecture/togaf9-doc/arch/chap28.html

Modern Analyst: https://www.modernanalyst.com/Resources/Articles/tabid/115/ID/5248/Capability-Based-Planning-with-ArchiMate.aspx

Harvard Business Review: https://hbr.org/2004/06/capitalizing-on-capabilities