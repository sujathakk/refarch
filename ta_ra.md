# Test Automation Reference Architecture 

The reference architecture template is a template model that represents the current or future/target state an architecture will rely on.

**Department: Enterprise Architecture**
\
**Organization: Technology Strategy and Innovation**
\
**Domain: Autonomous Systems**
\
**Documentation Identifier: RA-AS-04001**
\
**Template Version 1.01**
\
**Template Last Modified 9/1/2022**
\
**Author: Sujatha Sivaraman, Sujan Gautam**
\
**Sponsor: \<TBD\>**
\
**Adoption Status: DRAFT IN PROGRESS**
<!-- Suggested statuses are as follows:
    DRAFT IN PROGRESS - Document and/or AoA are still being worked
    UNDER REVIEW - Document has been submitted for formal review
    APPROVED - Document has been approved and adopted
    OBSOLETE - Document has been superseded with a subsequent opinion -->

## Requirements - Problem statement
* As part of our Automation technology radar it is imperative we have Test automation reference architure to standardize test automation across enterprise.
This would be single source of truth for test automation. Currently we have some valuestreams that onboard their own tools without evaluating the existing tools. 
Having one stop to pick and choose the right tool would eliminate dupliclity of tools being onboarded and reduce time and improve efficiency. Also eliminate the need for R&D by app teams to evaluate pleothra of tools in market to chose the one they need and onboard. 
* Test automation can automate some repetitive but necessary tasks in a formalized testing process already in place, or perform additional testing that would be difficult to do manually. 
* Test automation is critical for continuous delivery and continuous testing. 
## Test Automation roadmap
![Test Automation ](images/RA-AS-04001_roadmap.png)

#### Test Automation Platform
<!-- ![Test Automation Capability](images/RA-AS-04001_bcap.png) -->
![Test Automation Capability](images/RA-AS-04001_v.png)

### Potential Use Cases

List where the reference architecture may or will apply.
* Unit testing
* System testing
* Integration testing
* Vendor/Merchant onboarding
* Certification testing
* ADA compliance testing
* Acquirer/Issuer simulator testing
* Compatability, Validity for obsolete testing
* Test and test data preparation
* Test management and quality assurance
* Infrastructure, Network, Security, DevOps, Hybrid and multicloud, and Edge testing
### Component Diagram

This diagram will demonstrate how components of the reference architecture are connected to form a system, application, platform or service.  Flow through the reference architecture might be included to further describe the architecture.

![Test Automation](images/RA-AS-04001_cd.png)


### Components and Capability Narrative 
List each component or capability and a description of each.
#### **Test Automation :**  
    * Functional 
    * Non-functional
 -  _Test Automation is the process of using automation tools to maintain test data, execute tests, and analyze test results to improve software quality. 
 -  _In DFS TA enabled by CI/CD pipelines is acclerating the pace of innovation with increasing efficiency.Every testing tool whether be functional or non-functional is consolidated and available for use across Enterprise.
 -   _Required and also recommended tools choice offers team to pick and choose the appropriate while offering them variety of options. Automating tests saves time and money, reduces cost in training and onboarding duplicates, constantly refine and refresh our inventory and stay current and offer services in par with changing market trends and customer needs._

![Test Automation](images/RA-AS-04001_ut.png)

* **Functional Testing**
 -  **Unit testing** - Manual and Automated.
    - **Manual**
        - Development team after code development perform the unit testing in their own platform. 
        - Before test automation is kicked off, the automation will check for prerequistes like percentage of completion, status and usual suspects.
    - **Automation**
        - Once the prerequistes are completely the unit testing would step into test automation. 
        - The CICD pipeline is configured to continue unitesting in automation cycle. Based on programming language, type of testing, scope of testing, scripts are developed or updated.
        - After review process is completed, the scripts are executed and based on the test results the defects are raised and followed up.
        - Depending on colloboration agreement between product team and testing team the promotion of next phase of testing would continue. The unit testing is usually performed by the developer and always comes before integration testing. 
  - Based on how unit testing is done, these are below types
    - *Black box testing*: This involves UI testing along with input and output.
    - *White box testing*: This tests the functional behavior of the application
    - *Gray box testing*: This testing involves executing test cases, test suites, and performing risk analysis.
-  **Integration testing** - This tests whether all different modules interact with each other as they are supposed to. These are various ways integration testing is performed.
    - *Big bang approach*: combines all the modules or components of a system into a single unit and tests them as a whole.
    - *Top-Down approach*: Begins with the highest level component and works its way down the component hierarchy.
    - *Bottom-up approach*: Begins with the lowest level component and works its way up the component hierarchy.
    -  *Sandwich approach*: a hybrid approach that combines top-down and bottom-up integration testing methods.
 - **UI testing** - UI testing validates the user-friendliness of applications across devices and platforms. This tests the functionality of UI and checks visual aspects, usability, accessibility of UI across devices and cross-browsers. This could be code-based and code-less.
    - **GUI** - Graphical User Interface. Web UIs and other digital products
    - **NLI** - Natural Language UI. Conversational, voice, text etc.,
    - **VRUI** - Virtual Reality, Augumented Reality - AI and ML 
    - **WUI** - Web UI. Browser. testing aspects of any software a user interacts with. 
    - **CLI** - Command Line Interfaces.
 - **Acceptance testing** - Ensures whether system works and addresses concerns of stakeholders. How input is handled and how output is delivered. This is formal testing according to user needs, requirements, and business processes conducted to determine whether a system satisfies the acceptance criteria or not. This testing enables the users, customers, or other authorized entities to determine whether to accept the system or not
    
    - **BAT(Business Acceptance Testing)**: used to determine whether the product meets the business goals and purposes or not, mainly focuses on business profits which are quite challenging due to the changing market conditions and new technologies, so the current implementation may have to being changed which results in extra budgets.
    - **PACT/CAT(Contract Acceptance Testing)**: In DFS this testing is usually referred to as "PACT" testing. Stakeholders may involve sponsors, procurement teams. Ensures meeting the SLAs. Contract that specifies that once the product goes live, within a predetermined period, the acceptance test must be performed, and it should pass all the acceptance use cases.
    - **RAT(Regulation Acceptance Testing)**: Stakeholders are legal, compliance, risk teams etc., Used to determine whether the product violates the rules and regulations that are defined by the government of the country where it is being released.
    - **EAT(End-user Acceptance Testing)**: Stakeholders are end-users. Used to determine whether the product is working for the user correctly.
    - **Alpha** : Alpha testing is used to determine the product in the development testing environment by a specialized testers team usually called alpha testers.
    - **Beta** : Stakeholders sampling, trial customers. Beta testing is used to assess the product by exposing it to the real end-users, typically called beta testers in their environment

* **Non-functional Testing**
-  **Performance testing** - Performance QA practice to track performance under specific workload. Non-functional testing technique that evaluates an application's speed, stability, scalability, and responsiveness
    - *Load testing*: Testing that examines how the application behaves under an expected load of users or transactions.
    - *Stress testing*: Testing conducted to evaluate a system or component at or beyond the limits of its anticipated or specified workloads, or with reduced availability of resources such as access to memory or servers
    - *Smoke testing*: This testing involves executing test cases, test suites, and performing risk analysis.
    - *Volume testing*: Determines how an application performs when it's exposed to a large amount of data or when many people are using it at the same time.
    - *Spike testing*: testing that assesses how a system responds to sudden and significant changes in user activity.
    - *Soak testing*: This testing involves executing test cases, test suites, and performing risk analysis.
-  **Security testing** - Security Testing is the process of scanning the application for vulnerabilities 
    - *SAST*: Static Application Security Testing. Analyzes an application's source code to identify vulnerabilities before deployment. SAST is also known as white-box testing because the developer has access to the software's design, framework, and implementation. SAST can help developers find issues that might not be obvious outside of predictable failure conditions. However, SAST can be dependent on the code language and may produce more false positives.
    - *DAST*: Dynamic Application Security Testing. DAST is a testing tool and a process that uses the results of automated or manual tests to fix security vulnerabilities.   DAST can identify runtime problems that SAST can't, such as authentication and server configuration issues.
-   **Scalability testing**
    - *Horizontal scaling* - Horizontal testing confirms whether a user can navigate through a system, if it works as expected and if there are any unexpected bugs or exceptions.In horizontal scaling (“scaling out”), you get the additional capacity in a system by adding more instances to your environment, sharing the processing and memory workload across multiple devices.
    - *Vertical scaling* -  Vertical end-to-end testing refers to testing in layers, meaning tests happen in a sequential, hierarchal order.Vertical scaling (“scaling up”), you're adding more compute power to your existing instances/nodes.     
-   **Reliability testing**
    - *Test-Retest* - Test-retest reliability is a measure of reliability obtained by administering the same test twice over a period of time to a group of individuals.
    - *Parallel-forms* -  Used to assess the consistency of the results of two tests constructed in the same way from the same content domain.
    - *Internal consistency* -  Internal consistency is a measure of reliability.
    - *Inter-rater* - Measures the degree of agreement between different people observing or assessing the same thing. This type of reliability is used when researchers assign ratings, scores, or categories to one or more variables.
- **Compatability testing** - Compatibility testing is a type of testing that examines and compares functionality over multiple browsers, devices, platforms, and OS to recognize potential discrepancies.
    - *Forward* - Forward(Future) is the assessment of an application or software in upcoming or new versions of hardware/software to verify the performance of the existing hardware/software with the newer build
    - *Backward* - Backward Compatibility Testing is a technique to verify the behavior and compatibility of the developed hardware or software with their older versions of the hardware or software. Backward compatibility testing is much predictable as all the changes from the previous versions are known.
    - *Hardware* - A hardware compatibility test determines the compatibility between various hardware components, such as processor, RAM and GPU, and a piece of software.
    - *Software* -  A software compatibility test is an assessment used to ensure a software application is properly working across different browsers, databases, operating systems (OS), mobile devices, networks and hardware.
- **Resilience testing** - Resilience is a type of software testing that assesses how well a system can recover from failures and continue to operate. Running disaster scenarios, to identify vulnerabilities and analyze simulation consequences data to plan activities and to developing recovery mechanisms. 
    - *Exploratory* - Exploratory testing involves venturing into the unknown to better understand our systems.
    - *Verification* - Verification testing focuses on scenarios where we know what failure looks like and have established ways to mitigate it.
__________________________________________________________
#### **Test Data Management**
    * Data Analysis, Visualization
    * Data Sourcing, Extraction
    * Data Masking, Obfuscation, Transform
    * Data Disposal
    
* _TDM is the process of providing controlled data access and also process of creating, maintaining, and planning data sets used in software testing.Test data management (TDM) systems can automate this process by connecting to production data systems and extracting test data based on predefined rules. TDM involves a number of activities, including: Synchronizing data sources from production, Versioning copies of data, Discovering sensitive data, Masking data to comply with regulations, and Distributing test data to multiple clouds. In DFS TDM enabled by CI/CD pipelines is saving cost and time and offer instant data - clean data for testing._
* _TDM is important because it helps organizations comply with data protection regulations, such as CPRA, GDPR, and HIPAA. These regulations require that sensitive data and Personally Identifiable Information (PII) be anonymized in the test environment._
-  **Types of Data**
    -   Valid test data
    -   Invalid test data
    -   Boundary test data
    -   Absent test data
-  **Data Sourcing** - Involves identifying the sources of data to be used in testing. This is also referred to as data extraction, data collection. 
     - *Database*: We have data stored in multiple DBs, from Mainframe DB2 to on-prem relational to cloud non-relational noSQL etc., Relational and Non-relational databases can be the source.
    - *Datasource*: Production data including backups and subsets. 
    - *Cloud files*: File storage services. 
     - *Classified data*: 
-  **Data masking** - Data masking is a way to create a fake, but a realistic version of your organizational data. The goal is to protect sensitive data, while providing a functional alternative when real data is not needed. Applies static data masking to transform sensitive data values into fictitious yet realistic equivalents, while still preserving the business value and referential integrity of the data for use cases such as development and testing. Varied techniques can be used to achieve this and below are commonly used techniques.
    - *Data Encryption*:    Transforms data into an unreadable form using a secret key or algorithm. Only authorized parties can decrypt the data
    - *Data Obfuscation*:   Process of disguising sensitive data to make it unreadable or unintelligible to unauthorized users.Obfuscation retains the original data structure, just makes it unreadable
     - *Data Tokenization*: Replacing certain data with meaningless values that can be connected to the original data by authorized users.  
     - *Data anonymization/pseudonymization*:  Replaces real, sensitive data with similar but fictitious or false data.
     - *Data redaction*: Involves the removal of particular pieces of data from the whole of it. Redaction is generally a permanent removal or replacement of data.
     - *Data Masking*:  Masks data fields based on user roles and permissions.
     - *Data Generalization,Blurring, Nuling,Perturbation*: Removing identifiable data and generalizing data and blurring data and nullifying fields.Data perturbation is a technique that alters data values or query outputs to protect confidentiality. 
-  **Data Disposal** - 
    - *Deleting or reformatting or overwriting* : Deleting a file or reformatting a disk removes it from the user's view, but the data may still be recoverable
    - *Physically destroying* : Degaussing, Shredding etc.,Destroying a device with heat, a magnetic field, shredding, or pulverizing can remove data.
    - *Data sanitation* : Sanitation methods/algorthium include.
        - *write-zero* : The write-zero data sanitization method replaces regular readable data with zeros, preventing all software-based file recovery methods from extracting information from the drive.
        - *Gutmann* : Peter Gutmann Wiping Method of data erasure uses a grand total of 35 “passes” to ensure that there is no way that the data can be re-accessed
        - *DoD* : The Department of Defense 5220.22-M employs three overwrite passes (0s, 1s, and Random), as well as a 100 percent verification pass.
__________________________________________________________

#### **Test Environment** 
    * Environments
    * Support
    * Services
    * Non-OA environments
    * Dev, UAT, Staging, RME, Preprod
    * Reports

* _A controlled setting where software and hardware are configured to test the functionality of an application.A stable test environment is well-maintained and consistent, so that tests produce reliable results. An automated test environment can speed up the setup and execution of test cases. This helps to avoid false-positive or false-negative results.Access to the test environment should be restricted to prevent accidental tampering with configurations or test data._

-  **Environments**
      - Release environments
        - TSYS - This covers Bank, Card and Payment LOBs. Represents Jan, Apr, Jul and Oct months of the calendar.
        - MST0 - This covers Bank, Card and Payment LOBs. Represents Feb, May, Aug , and Nov months of the calendar.
        - ASYS -  This covers Bank, Card and Payment LOBs.  Represents Mar, Jun, Sep and Dec months of the calendar.
      - Network Release environments
           - OSYS -   This covers  Card and Payment LOBs.  Apr and Oct months of the calendar.
           - ECT0(Certifications) -  Payment LOBs. This environment is used to certify the merchants for readiness to use the Discover Network.
      - Project specific Environments
           - QSYS - Card and Bank. Project specific environment, currently in use by DSL Consent Order Testing
           - VST0 - Card and Bank. Project specific environment, currently being scaled up for SCRA project
      - Performance and Tuning
           - UWTO - Card, Bank and Payments. 
-  **Services offered**
      - Batch : Batch is accumulation of processes/jobs running in production in a day
        -Based on functionality the batches are segregated as below
           - Finacle 
           - Merchant(SOC) 
           - Card(EOC)
      - Health monitoring : Monitors health of servers via CPU, Memory, Swap memory metrics
      - Environment Refresh : Bringning latest production components into testing environment.
        - Initial
        - Mid-cycle
        - End-of-release    
      - Change tracking (CAB) : 
         - Infrastructure changes 
         - Batch schedule 
         - Data refresh
      - Defect management:
         - Assignment : assign defects based on severity, region and aging?
         - Reporting : Providind report dashboard.    
__________________________________________________________    
#### **Test Engineering**
    * Test Design
    * Test Develop
    * Test Execute
    * Test Colloborate
    * Test Report

* _Test automation engineering involves the use of automation tools to execute test cases, with the goal of reducing the need for manual testing1. Automated testing is used throughout software projects, especially in agile and DevOps methods, where tests are run automatically using software tools. Automation test engineers develop codes and programs to automate testing tasks._

_______________________________________________    
#### Banking specific test automation
* Host Simulators
* ISO and Non-ISO message testing and validation
* ATM simulator
* Acquirer and Issuer simulators
- **Bank special testing**
    * Acquirer simulators
    * Issuer simulators
    * Merchant onboard 
    * Certification
    * ISO standards check 

_______________________________________________    
#### Misc
* Reduce and Resuse - Decrease the number of duplicate tools being onboarded and allows value streams to resuse existing tools
* Buffet vs Ordering - Having one stop for test automation gives options to select and sample rather than search and pay and evaluate.
* Uniform testing - allows testing and app team to refine and improve their testing startergies and get better results
* Onboarding hurdles - Identifying and reusing the right tools eliminates the hassles teams have to go through to onboard a new vendor/new tool.
* Eliminate ambiguity - Value streams dont need to re-invent the wheel, they can customize the testing strartegy and tools according to their requirement and peculiraties. Context dependent testcases across enterprises helps eliminate obsolete and irrelevant testcases.
* Pesticide paradox - Reusing tools across value streams and constantly updating and customizing helps reducing pesticide paradox and improves chance of finding more bugs.
* Silo vs colloboration - App teams working with test teams across value streams helps them refine and redefine their priorities and use expertise of those respective teams to the fullest.
* Lean into Pareto principle - Repetition and reuse would help testing teams adapt better and explore paths less travelled to improve their testing capabilities outsourced to them by application teams.

### Entity Relationship

This diagram will present how entities relate to each other.  This is not specific to data entity relationships but any relationship that help describe the reference architecture.

### Considerations

Considerations critical to the intended consumption of the reference architecture will be listed here by section.  Considerations most used are as follows:

 - Governance
    - **Quality assurance**
        * Constant use and reuse by multiple teams helps testimg team have updated and relevent data and discard stale data.
        * Compliance
        * ADA, WCAG Compliance can be automated and validated part of every test cycle and made sure that organizations stays on top of it.
 - Security
    - * Test Automation is controlled environment.
        
 - Availability, Reliability, Resiliency

 - Data
    * TDM makes sure that data privacy is reserved.
    * Data is refreshed and cleaned 
 - Integration
    - **Colloboration**
        * Having single source of truth for all testing needs will help teams collobarte better between multiple verticals. The pros and cons and feedback and dos and donts and merits and demerits can be traced and tracked via feedback and constant updates.
        * FAQs and selfhelp links can be made available
        * Tagging tools with keywords would improve reach and help search and increase visibility
    - **Centralized repository**     
        * Easy to search and find appropriate tools.
        * One-for-all and All-for-one for teams and tools.
        * Decoupling design, compatibility, validity, expenditure burdens from application performance and efficiency
        * Better control over onboarding, staying current and reduce staleness of tool and also scripts
        * Constant update of inventory and reading and being upto date with market trends

 - Devops
 - Finops
 - Performance
- **Reduce tools and Reuse tools**
  * Having onestop destination for all testing needs eliminates the burden of app teams and allows them to reduce duplicate tools being onboarded and have inhouse expertise to be shared among teams to make informed decision. 
 
 - Efficency
    * Having all data obfuscation, data masking, data collection, data sourcing , data tranforming tools will improve efficiency and reduce time.
    * Test automation makes tracking demarcation of testing,development etc., better and helps improve compartmentalized efficiency .
These considerations are not a requirement and will only be included where applicable.
    * Rather than researching a new tool and filtering vendors and onboarding the chosen one, application teams can refer to inventory and save time and improve efficiency.
   * Plug and play prerequistes for any type of testing and customization will reduce time in test automation and help team zero in on priority.



### Glossary

Terms and acronyms described
TTP - Testing Tools platform
TDM - Test Data Management
TEM - Test Environment 
QMS - Quality Management System
QEP - Quality 
ISO - International Standards Organization

