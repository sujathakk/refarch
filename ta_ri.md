# Testing Automation Reference Implementation

**Department: Enterprise Architecture**
\
**Organization: Technology Strategy and Innovation**
\
**Domain: Autonomous Systems**
\
**Documentation Identifier: RI-AS-02002**
\
**Template Version 1.01**
\
**Last Modified 06/06/2023**
\
**Author: Sujatha Sivaraman, Sujan Gautam**
\
**Collaborators: Vivek Sangana, Marielyn Untalan**
\
**Sponsor: Keith Neilsen**
\
**Adoption Status: DRAFT IN PROGRESS**
<!-- Suggested statuses are as follows:
    DRAFT IN PROGRESS - Document and/or AoA are still being worked
    UNDER REVIEW - Document has been submitted for formal review
    APPROVED - Document has been approved and adopted
    OBSOLETE - Document has been superseded with a subsequent opinion -->

[Test Automation Roadmap](#Test-Automation-roadmap)</br>
[Test Automation](#test-automation)</br>
[Test Automation Tools](##Test-Automation-Tools)</br>


## Requirements - Problem statement
- Test automation is crucial and essential part of SDLC. Manual tests are prone to error requires lot of training and lack of standarized flow and process results in time consuming test cycle, unpredictable/predictable results,  stale testcases and stale testdata and day late and penny short releases. 
- The automation of test design, development, execution, data preparation and handling and appropriate governance implemented to maintain quality and support and selection and onboard of right tools. Test automation can streamline and accelerate the software development lifecycle (SDLC). 
- Test automation is the practice of automating the test cycle from its inception to reporting. Test automation must integrate with security, compliance and regulation in addition to development and operations to be functional in any regulated industry. It is impossible to release anything to production consistently without a fully functional test automtion system that provides automated governance. 
- The main goal of test automation is to establish a standard process which is auditable, repeatable and predictable in addition to providing easy collaboration and early feedback. The intent of this reference architecture is to provide high level capabilities (platform and pipeline) that enable a delivery team to achieve proper CI/CD starting from source code management to going live in production.

### Test Automation roadmap
![TA Roadmap](images/RI-AS-04001_roadmap.png)

### Future state 
    * Publicize the test automation artifact repository and setup DIY portal to "Frankenstein" the test automation E-2-E and optional sandbox to test out the flow. 
    * Orchestration setup to automate test to do certification testing, vendor onboarding, merchant onboarding, DN, DCI and Hydra.
    * Attestation from product owner to ensure that any new tool onboarded for testing is filtered through exisiting tools and after ADR,AOA and their approval has been saught. 
    * Streamline test tool intake and mandate stakeholder sign off to avoid duplicate tools.
    * Setup intake for new tools via Test automation consultancy requests via SNOW.
    * AI enabled DTA page dedicated to search about TA and available tools and their functionality and point of contacts and FAQs.
    
## TA Platform 
![TA](images/RI-AS-04001_bcap.png)
------------------------------------------------------------------------------------------------------------------------------------------
[Click here : Test Automation Framework ](#TA-Framework)

### TA framework

| Framework | Desc| Required | Recommended | Comment | 
|-------| ------------------| ---| --| -------------|
| Karate | API, Performance and end to end testing tool | Y| | [Karate](https://dta.discoverfinancial.com/products/tap-karate/docs/karate-starter-kit)|
| Selenium, Serenity | Web Testing and Automation framework|Y | |  [Selenium](https://dta.discoverfinancial.com/tutorials/ui-validation-by-selenium-serenity-bdd)|
|Serenity| Web Testing, API Testing framework | Y | 
| Playwright | Web Testing, API Testing library  | Y | | [Playwright](https://dta.discoverfinancial.com/products/tap-playwright/docs/playwright-starter-kit)|
| Cypress | End-to-end testing framework for Web applications which run on Angular and React.js | Y | | [Cypress](https://dta.discoverfinancial.com/products/tap-cypress/docs/cypress-starter-kit/cypress)|
| Appium | Native,Hybrid, webapps framework|Y| |[Appium](https://dta.discoverfinancial.com/products/mobile-regression-pipeline/articles/Appium)|
| Cucumber | BDD framework | Y | | [Cucumber](https://dta.discoverfinancial.com/products/mobile-regression-pipeline/articles/Cucumber)|
|Katalon | Web,Mobile,API testing Framework | Y| |[Katalon](https://github.discoverfinancial.com/esqm-org/katalon-studio-system-docs/blob/master/system-docs-template.md)|
|Blazmeter Taurus| 	Performance testing platform  | Y| | [Taurus]()|
|Allure | Test reporting framework | Y | | [Qameta Allure](https://allurereport.org/docs/)|
------------------------------------------------------ 
## Component Diagram
-------------------------------------------------------------------------------------------------------------------------------------------

## Test Automation 
1. **Test Generation**
    - Test planning
    - Test case Development
    - Test Data
    - Test Script generation
2. **Test Execution**
    - Test tool
    - Test Execution
    - CICD orchestration, pipeline
3. **Test Reporting**
     - Test results
     - Test Reports
     - Test Defects
     - Deliverables.
---------------------------------------------------------------------------------------------------
## Test Generation
![TA Test Generation](images/RI-AS-04001_testgen.png)
* Test Generation involves test plan- development, test data preparation and test script generation.
* Every release is mandated in DFS to be tested through Selenium/Cucumber.
* TDM - Test Data Management has the primary goal of providing data for testing.
* Below steps ensure that testing teams have right correct data
    *  **Automation** - Automating the E-2-E process. Data refresh via extraction and then masking and obfuscating the data and loading into right environment.
    *  **Data Quality** - Data can be extracted from varied sources like Oracle, Db2, Teradata or SQL server. Data obfuscation should be complete and consistent while maintaining data integrity with robust sub-setting process. All the while making sure that we preserve encryption.
    *  **Data Security** - Ensuring enhanced protection with advanced encryption. 
    *  **Speed** - Faster turnout is implemented by increasing the refresh cycle, using right tools, and using out of the box algorthims. 
    *  **Test Data coverage** - Validation of data as one of main steps , improving the coverage of data regardless of hybrid/on-prem/cloud datacenters, centralized repository for test data and continously improving and optimizing with autoscaling.
* Production and Non-production
#### TDM flow
* Identify the source for data fetch.
* Using right tools like IBM DPU optim, the data goes through the below cycle.
    -   Extraction
    - Obfuscation
    - Validation 
 * Generate the gold copy. Move the data from production into test environments.
 * Data is made available for testing and development teams
 * Data can be selected, filtered and customized to meet testers,users,business needs.
 * Synthetic data is generated using the right tools like GenRocket.

![TA Test Generation](images/RI-AS-04001_tdmf.png)
------------------------------------------------------------------------------------------------------------------------------------------
</br>[Click here : Tools used in Test Generation](#Test-Generation-Tools)</br>
</br>
-------------------------------------------------------------------------------------------------------------------------------------------
## Test Execution
![TA Test Execution](images/RI-AS-04001_te.png)

* Test execution involves testing tools selection, setting up orchestration and pipeline for test automation in trident/CICD, executing the testplan
* Sonarqube plugins in developer systems scans to capture unit tests run locally in their systems. Jenkins looks for JUnit testing result to estimate the coverage of testing
* Health checks and validity for setup smoke test are performed before test automation cycle is initiated.
* Quality Engineering team performs manual test validations to ensure the component is throughly vetted and all the criteria's/scenarios satisfy the requirement
* Once the code/build is promoted to higher environment the test validations are performed automated test suites and each of these results are tracked and defects if any are logged in Xray.
* Upon successful functional validations , non functional validations such as load and performance tests are performed on production like environment
to evaluate how well an application performs under different workloads
* Test automation performs both functional and non-functional testing cycle and validates the test results and provides approval to move to next stages.

![TA Test Execution](images/RI-AS-04001_ut.png)

------------------------------------------------------------------------------------------------------------------------------------------
</br>[Click here : Orchestration and Pipeline tools list](#Orchestration-and-Pipeline)
</br>
-------------------------------------------------------------------------------------------------------------------------------------------

### Functional testing
![TA Functional testing](images/RI-AS-04001_ft.png)
* Functional testing includes UI testing, api testing, various acceptance testing including business acceptance, regulatory acceptance etc., 
    * UI testing
    * Regulatory Testing
    * Accessibility
        * WCAG
    * Banking and Payments related testing are automated and run in their respective test environments in PSI and zone 3 zones.
    * Industry specific testing
        - Banking and Payments related testing are automated and run in their respective test environments in PSI and zone 3 zones.
        *   Bank
        *   Finance
        *   Compliance
-------------------------------------------
[Click here : UI testing tools](#ui-testing)</br>
[Click here : Regulatory and Accessibility](#Regulatory-and-Accessibility-Testing)</br>
[Click here : Bank/Finance/Compliance Testing tools]([#Bank-Finance-Compliance-Testing)</br>

-------------------------------------------

### Non-functional testing
![TA Non-Functional Tools](images/RI-AS-04001_nft.png)

* Non-Functional testing includes perfomance testing including smoke testing,  acceptance testing including compliance, security testing both SAST and DAST 
    *   Security
        * SAST
        * DAST
        * IAST
    * Performance testing
        * Smoke
        * Sanity
        * Load

##### Prod/Non-prod

-------------------------------------------
[Click here : Security testing tools](#Security-Testing)
</br>
-------------------------------------------
 
 ## Test Reporting
 * Test reporting is a process in software testing that involves gathering, analyzing, and presenting essential test results and statistics to stakeholders.
 * Test reporting contains a summary of the test, including what was tested, when and how it was tested, and the test environment utilized
 ![TA Test Reporting](images/RI-AS-04001_tr.png)
 #### Test Results
 * After executing and monitoring test cases, you evaluate and interpret the results against test quality criteria
    * Collect test results
    * Analyze test results 
 #### Test reports
 * A test report is a summary of testing objectives, activities, and results to help stakeholders better understand both the testing and the product quality. 
    * Preparing test reports: Create comprehensive test reports that communicate the test results and status to the project team and stakeholders.
    * Reviewing test reports: Identify defects in the test reports.
    * Tracking and reporting progress: Track and report the progress of defect resolution

------------------------------
[Click here : Reports List](#Type-of-reports) 
</br>
-------------------------------
 #### Test Defects 
* Analyze defects: Begin defect analysis with QA services taking over the requirements of the product. 
* Measure defect density: Measure the number of defects discovered in software or other parts over the period of a development cycle. 
* Increase test coverage: Increase test coverage to decrease the number of defects present in the end-user experience. 
* Configure test environment: Configure the test environment to provide insights into the turnaround time for fixing defects    
----------------------------------
[Click here : Defects List](#Type-of-Defects)</br>

 ---------------------------------
 #### Deliverables
 * Prepare final test reports for stakeholders
* Test cases and test scripts executed are logged in test management tools like ALM/X-ray and the corresponding JIRA issues are marked with correct stage and status based on the outcome.
* Testing frameworks used create the test report with status, defect, reports and reason for the failed testcases and details about testcase and test defects etc.,
* Allure is reporting framework which can consolidate all the reports from other framework and generate customized consolidated report.
![TA Test Reporting](images/RI-AS-04001_trflow.png)
<!--
```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
-->
## Test Automation Tools
#### Test Generation Tools
------------------------------------------------------
| Tool | Category | Desc| Required | Recommended | Comment | 
|-------| ------| ------------------| ---| --| -------------|
|  GenRocket | Data source | "GenRocket’s Test Data Generation platform is capable of generating thousands of rows of synthetic test data per second | Y | |[Genrocket](https://dta.discoverfinancial.com/products/genrocket/pages/gettingstarted) |
| Acxiom | | |Y | | [Acxiom Snowflake](https://github.discoverfinancial.com/entdata-arch-solutions-org/snowflake-data-sharing-with-axiom-system-docs) |
| Customer360 | Data source |A Customer 360 journey provides a trusted, complete, and actionable view of individual and organizational customer data (master data and insights) which is used for analytics and operations to deliver highly personalized experiences across marketing, sales and support| | | [Customer360](https://github.discoverfinancial.com/cbuchha/Informatica--SaaS/blob/master/system-docs-template.md) |
| CDS/Sage prime | Datasource | Data source SOT for all customer data across all Discover LOBs |Y | | [Sage](https://dta.discoverfinancial.com/products/sage),[SAGE Prime](https://github.discoverfinancial.com/customer-profile-org/customer-profile-system-docs/blob/master/CustomerProfileSysDoc.md)|
| Terradata | Data source | RDBMS that drives companys dataware house| Y| | [Teradata](https://dta.discoverfinancial.com/products/Teradata) |
| IDS Integrated Data Stage| Data Source| | | |
| IBM infosphere | Data extraction, Data masking |  Test Data Management Solution is used to extract, copy, obfuscate, and move sets of relationally intact data from source tables to corresponding destination tables| | | [IBM Infosphere](https://dta.discoverfinancial.com/orgs/ESQM_Services/docs/test_data_management/tools/ibm-infosphere-optim/overview)| |
| Delphix| Data Masking | | | | |
| IBM optim| Data extraction, masking |Test data Platform initiative, EDP (Decisioning Platform) is to have data obfuscation of unstructured data/semi structured while provisioning data from prod into lower environment | | | [IBM Optim DPU](https://github.discoverfinancial.com/qep-tdp-org/qep-tdp-org-system-docs/blob/master/system-docs-template.md)|
| Broadcom| Data Masking |  Broadcom solutions for mainframe databases and database management use an open-first approach to ensure efficient management and reliability of enterprise data | | | | |
| Gartner| Data source, Data masking | Data Collection: Gartner collects data from various sources to gather relevant information for their analysis. These sources may include surveys, interviews, market research, vendor briefings, industry events, and publicly available data.| | | | |
| Informatica| Data Masking | | | | |
| Tableau| Data visualization | Tableau is a Data Visualization tool for self-service creation of Workbooks/Dashboards. Workbooks/Dashboards are published to the Tableau server environment, for consumption by enterprise users. Tableau On-Premise Server is hosted internally in a Secured Zone (IS1)|Y||[On-prem tableau  ](https://github.discoverfinancial.com/tableau-org/Tableau-OnPrem-System-Docs/blob/master/Tableau-onprem-system-docs-template.md), [  Cloud tableau](https://github.discoverfinancial.com/tableau-org/tableau-server-cloud-system-docs)|
| Datawrapper | | | | | |
| Power BI| Data Visualization| | | | [Data and BI platform](https://dta.discoverfinancial.com/orgs/Data_and_BI_Platform)|
| Qlik| Data Visualization | Qlik Enterprise Manager provides a single point of control for designing, executing, and monitoring Qlik Replicate and analytics, tasks, server health | Y|| [Qlik](https://github.discoverfinancial.com/sde-org/qlik-data-integration-system-docs/blob/master/system-docs-template.md)|
| Toad datapoint| Data Preparation  |Self-Service Data Preparation Tool. Toad® Data Point is a cross-platform, self-service, data-integration tool that simplifies data access, preparation and provisioning | | | [Toad Datapoint](https://dta.discoverfinancial.com/orgs/BI_Foundational_Capabilities/pages/toad/toad-helix)|
| Kofax | Data extraction (OCR) |  Kofax TotalAgility Core , Kofax TotalAgility SaaS  |Y | | [Kofax Total agility](https://github.discoverfinancial.com/idms-org/Kofax-TotalAgility-system-docs/blob/master/system-docs-template.md) |
| Talend | Data source, Data extraction | Talend is a comprehensive collection of services and software solutions for managing data from multiple sources. Talend's data integration tools make it easy for businesses to quickly combine data from various sources, such as databases, flat files, online services and web API Management| | | |
| Tesseract| Data extraction OCR |Tesseract is an optical character recognition engine for various operating systems. It is free software, released under the Apache License. | | | |
| Weblink crawler| Data extraction |A web crawler, spider, or search engine bot downloads and indexes content from all over the Internet.| | Maybe | [weblink crawler](https://dta.discoverfinancial.com/products/tap-weblink/docs/weblink-starter-kit) |
| Wipedrive | Data disposal|WipeDrive completely erases ALL hard drive or external storage information including your personal data, programs, viruses and malware. | | | |
| Srm(Storage Resource Managment) |Data Disposal | software provides near-real-time and historical information for the storage infrastructure regarding availability, capacity and performance, device management, problem determination, configuration planning and change management | | | | |
| Eracent| Data disposal| Offers data disposal as well as ITMC lifecycle , data normalization, Integrated Disposition Management| | | |
| Eraser | Data disposal |Eraser is an advanced security tool for Windows which allows you to completely remove sensitive data from your hard drive by overwriting it several times. | | | |
| Proton | Data disposal | Instantly and permanently erase data on electronic media, ensuring compliance with electronic waste disposal regulations| | | |
| Sdelete| Data disposal | Microsoft sysinternals provides a utility called SDelete that can securely delete files and free space on a drive | | | |
| | | | | | |
| | | | | | |
-----------------------------------------------------------------------------------------------------------
#### Orchestration and Pipeline [Code coverage, Config mgmt, Acceptance testing, Release]
------------------------------------------------------
| Tool | Desc| Required | Recommended | Comment | 
|-------| ------------------| ---| --| -------------|
| Armorcode | Application security orchestration and correlation (ASOC) is a category of application security (AppSec) solution that helps streamline vulnerability testing and remediation through workflow automation. | Y | | [Armorcode](https://github.discoverfinancial.com/cs-eng-org/asoc-system-docs/blob/asoc-rpatha1/system-docs-template.md) |
| Sealights |SeaLights is a Quality Intelligence Platform which collects the code changes in each build. It will collect the details of the tests executed and their code coverage. Code coverage tool. | Y | |[Sealights](https://github.discoverfinancial.com/esqm-org/sealights-system-docs/blob/master/system-docs-template.md) Test Coverage,Test Gap Analytics (TGA), Test Impact Analysis (TIA) , Release Quality Analytics,Test optimization|
| Nexus IQ| Nexus IQ provides you to scan open source libraries for all popular formats. to store application binaries and other published artifacts. Application dependencies are sourced from nexus repository for builds.| Y| | [Nexus](https://github.discoverfinancial.com/scm-org/cicd-system-docs/blob/main/nexus/README.md), [Nexus IQ](https://dta.discoverfinancial.com/products/nexus-iq)|
| Gitlab | Sourcecode repository | Y |
| Chef/Ansible | Ansible Automation Platform (AAP) is an enterprise level framework provided by RedHat for building and operating IT automation at scale, from hybrid cloud to the edge | Y | | [Ansible](https://github.discoverfinancial.com/cloud-build-org/ansible-system-docs/blob/master/system-docs-template.md)|
| Jenkins | Configuration management.CloudBees Jenkins is used as an orchestrator for Discovers continuous integration and delivery. It provides a shared, centrally managed, self-service experience for all development teams to build and deploy their applications | Y | | [Jenkins](https://github.discoverfinancial.com/scm-org/cicd-system-docs/tree/main/jenkins) |
| JFrog| The JFrog Platform gives you an end-to-end pipeline to control the flow of your binaries from build to production| Y | |[JFrog](https://dta.discoverfinancial.com/products/artifactory)|
| SonarQube | SonarQube is an open source platform for continuous inspection of code quality to perform automatic reviews with static analysis of code to detect bugs, code smells and security vulnerabilities.| Y| | [SonarQube](https://github.discoverfinancial.com/scm-org/cicd-system-docs/tree/main/sonarqube) |
| Junit| JUnit 5 is the current generation of the JUnit testing framework, which provides a modern foundation for developer-side testing on the JVM| Y |
| Jasmine | Jasmine is a framework for testing JavaScript code |
| Jest | Jest is a JavaScript testing framework designed to ensure correctness of any JavaScript codebase. | | | [Jest](https://dta.discoverfinancial.com/products/customer-portal/docs/customer-portal-web-spa/testing/jest)|
| Mocha | MOCHA is a project management framework that defines the roles and responsibilities within a project|
| Gradle |Gradle is a build automation tool used to automate the creation of applications. The building process includes compiling, linking, and packaging the code | Y || [Gradle](https://dta.discoverfinancial.com/products/tap-gradle/docs/gradle-starter-kit)|
| Lambdatest | Cloud Test Platform (LambdaTest) helps us to verify the software quality on a cross browser, Emulator/Simulator & real-device cloud. Value Stream teams can access thousands of real desktop, Simulators/Emulators and mobile devices for testing websites and apps in real time| Y | | [Lambdatest](https://github.discoverfinancial.com/esqm-org/cloud-test-platform-system-docs/blob/master/system-docs-template.md)|
| Playwright | Playwright provides the ability to automate browser tasks in Chromium, Firefox and WebKit with a single API| Y| | [Playwright](https://dta.discoverfinancial.com/products/tap-playwright-java/docs/playwright-java-starter-kit)|
|Postman| API testing tool | Y | |[Postman](https://dta.discoverfinancial.com/products/postman)|
| Squish | Squish features dedicated support for automated testing of native Mobile Apps, mobile Web Apps as well as a mixture of both |Y| |[Squish](https://dta.discoverfinancial.com/products/tap-squish/docs/squish-starter-kit)
| Protractor | Protractor is an end-to-end test framework for Angular and AngularJS applications.| Y| |[Protractor](https://dta.discoverfinancial.com/products/tap-protractor/docs/protractor-starter-kit)|
| X-ray | | Y | | replaced ALM. [Xraykit](https://dta.discoverfinancial.com/orgs/ESQM_Services/docs/products/xray-starter-kit), [Xray](https://github.discoverfinancial.com/esqm-org/xray-test-case-management-system-docs/blob/master/README.md) |
|NPM | NPM is a package manager for the JavaScript programming language maintained by npm, Inc., a subsidiary of GitHub
| Nunit | NUnit is a unit-testing framework for all .Net languages |
| Xunit | The xUnit frameworks are often used for unit testing – testing an isolated unit of code|
| Hoverfly| 
| Mockito |
| Wiremock|
| Easymockito | Mockito is a Java-based framework used for unit testing of Java applications |
| Emma | EMMA is an open-source toolkit for measuring and reporting Java code coverage|
| TestNG | TestNG is a testing framework for the Java programming language |
| Perfecto| Perfecto is the leading testing platform for web and mobile apps. Access the cloud for end-to-end testing from anywhere in the world|
| Browserstack| BrowserStack testing platform to test websites, and mobile applications across on-demand browsers, operating systems and real mobile devices|
| SmartBear | Provides lot of tools to build, test, release and monitor software|
| Tricentis | Used to automate E-2-E xtesting across SAP and associated applications|
--------------------------------------------------------------------------------------------------------
#### UI testing
| Tool | Desc| Required | Recommended | Comment | 
|---------| -----| ------| ------| ------|
| Squish | GUI testing tool that enables cross-platform testing of desktop, web and mobile applications. | Y | |[Squish](https://dta.discoverfinancial.com/products/tap-squish/docs/squish-starter-kit)|
| Lambatest | Cloud testing platform allowing users to run automated and manual tests on their platform |Y | |[Lambdatest](https://github.discoverfinancial.com/esqm-org/cloud-test-platform-system-docs/blob/master/system-docs-template.md)|
|Puppeteer | Puppeteer is a JavaScript library which provides a high-level API to control Chrome or Firefox over the DevTools Protocol or WebDriver BiDi.| Y |
| Jmeter |JMeter is a free, open-source Java application that tests and measures the performance of software and applications | Y| | [Jmeter](https://dta.discoverfinancial.com/products/tap-jmeter/docs/jmeter-starter-kit)|
| Lighthouse |Lighthouse is a tool that analyzes web apps and web pages, collecting modern performance metrics and insights on developer best practices. |Y| | [Lighthouse](https://dta.discoverfinancial.com/products/tap-playwright-lighthouse/docs/lighthouse-starter-kit)|
| Protractor | 	Protractor is an end-to-end test framework for Angular and AngularJS applications.Its primarily used in Webtesting of an application| Y| |[Protractor](https://dta.discoverfinancial.com/products/tap-protractor/docs/protractor-starter-kit)|
| Saucelabs | Cloud testing platform allowing users to run automated and manual tests on their platform | Y | | [Discover Mobile Testing](https://github.discoverfinancial.com/digital-mobile-org/discover-mobile-regression-system-docs)|

#### Regulatory and Accessibility Testing
| Tool | Desc| Required | Recommended | Comment | 
|---------| -----| ------| ------| ------|
| Level Access | Accessibility, ADA chrome extension tool | Y| |[Level Access](https://github.discoverfinancial.com/digital-web-platform-org/level-access-system-dcos)|
|Playwright(Axe) and A11y| Desktop reader| | | [Axe](https://github.discoverfinancial.com/pages/digital-web-platform-org/docs/research/libraries/accessibility/accessibility-axe-a11y/)<br> [A11y](https://github.discoverfinancial.com/pages/digital-web-platform-org/docs/research/libraries/accessibility/accessibility-eslint-a11y-plugin/)
|Google Lighthouse| Web apps and pages | | | [Lighthouse](https://github.discoverfinancial.com/pages/digital-web-platform-org/docs/research/libraries/accessibility/accessibility-google-lighthouse/)
|JAWS and NVDA [Manual] | Desktop screen reader Accessiblity | Y | | [JAWS](https://dta.discoverfinancial.com/articles/know-your-discover-accessibility-tools) |
|Talkback and Voiceover| Mobile screen reader  | | | Talkback/Voiceover


#### Bank Finance Compliance Testing

| Tool | Desc| Required | Recommended | Comment | 
|---------| -----| ------| ------| ------|
| Clear2pay | Open Test Solutions OTS: Host allows you to build simulator scripts more quickly and improves testing accuracy.|Y | | [Clear2pay](https://github.discoverfinancial.com/pulse-switch-org/PULSE-Switch-Clear2Pay-system-docs/blob/master/system-docs-template.md)|
| FIS | Fidelity National Information Services (FIS) is a global provider of financial services technology and outsourcing solutions | Y| | [FIS OPF](https://github.discoverfinancial.com/ent-finance-org/open-payments-framework-system-docs/blob/master/system-docs-template.md) |
| FIS | Fidelity National Information Services, Inc FIS AFFN Simulator / Professional Services for AFFN Simulator | Y|| [AFFN simulator](https://github.discoverfinancial.com/mknauff/payment-services-architecture-governance/issues/188)|
| EFTlabs |
| Auditboard |The Auditboard Internal Audit workpaper system will be used for improved functional, related processing for internal audit scheduling, executing audits, and storing internal audit information with associated workpapers as well as providing a system to build and define reports to assist with the Internal Audit business processes |Y| |[Auditboard](https://github.discoverfinancial.com/corp-services-hr-org/auditboard-system-docs/blob/AuditBoard/system-docs-template.md)|
| Wolters Kluwer |
| Diligent |software-as-a-service tool focused on the governance, risk and compliance market | Y | | |
| Workiva | Workiva offers the only unified SaaS platform that brings customers’ financial reporting, Environmental, Social, and Governance (ESG), and Governance, Risk, and Compliance (GRC) together in a controlled, secure, audit-ready platform. Workiva Sync Excel Plugin and Adobe In-Design Plugin| Y| | [workiva](https://github.discoverfinancial.com/finance-modernization-org/workiva-system-docs/blob/master/system-docs-template.md) 
| Workiva[obsolete]| | Y| | [workiva2](https://github.discoverfinancial.com/ent-finance-org/workiva-system-docs)|
|Lithos-Payhuddle| Acquirer Simulator | Y | | [Lithos](https://github.discoverfinancial.com/esqm-org/acquirer-simulator-system-docs)|
|Onetrust| Privacy Aggregator | Y | |[Onetrust](https://github.discoverfinancial.com/ent-privacy-aggregator-org/privacy-aggregator-system-docs/blob/master/system-docs-template.md)|
| KaNest |KaNest® terminal simulator (KN-R) is used to test hosts in a transactional environment | y | |
| Paragon | Bank/Finance simulator tool | Y||[Paragon](https://github.discoverfinancial.com/pulse-switch-org/paragon-system-docs/blob/master/system-docs-template.md)|
| Loadrunner |LoadRunner is a software testing tool that measures how applications perform under load | | |
|Fime| Reliable and secure transaction experiences across payments, banking and urban mobility tool | Y | | [Fime]()|
|IBM BPM| Business Automation Workflow | | Maybenot | [IBM BPM](https://github.discoverfinancial.com/ggodwi1/ibm-bpm-sys-docs/blob/master/ibm-bpm-sys-doc.md)|

### Security Testing
| Tool | Status | Desc | Environment | Comments
| ------------| ------------| --------------| ---------| -----------| 
| Sonarqube | Active |SonarQube is an open source platform for continuous inspection of code quality to perform automatic reviews with static analysis of code to detect bugs, code smells and security vulnerabilities. | | [](https://github.discoverfinancial.com/scm-org/cicd-system-docs/tree/main/sonarqube)
| Sonatype | Active | Supply Chain Management? Sonatype CI build will package, commit, and publish to the official helm repository. | | |
| Black duck| | The all-in-one application security platform optimized for DevSecOps.Black Duck allows teams that package and deliver applications using Docker (and other) containers to confirm and attest that any open source in their containers meets use and security policies, is free of vulnerabilities, and fulfills license obligations| | |
|Snyk| |Snyk builds security into  IDE, scanning your code, open source code, containers, and cloud for vulnerabilities and providing actionable fix advice. Snyk integrates with a variety of source control managers (SCMs) to help you track, monitor, and fix the issues and vulnerabilities in your code|  | |
|Zap| | Zed Attack Proxy (ZAP) by Checkmarx is a free, open-source penetration testing tool. ZAP is designed specifically for testing web applications and is both flexible and extensible| | |
|SQLmap| |sqlmap is an open source penetration testing tool that automates the process of detecting and exploiting SQL injection flaws and taking over of database| | |
|Acunetix| | Acunetix is an end-to-end web security scanner that offers a 360 view of an organization's security| | |
|Qualys| | Qualys supports the Vulnerability Management program, Platform Security team program| | [Qualys](https://github.discoverfinancial.com/vulnmgmt-org/qualys-system-docs/blob/master/system-docs-template.md)|
|Censys| | Censys helps organizations, individuals, and researchers find and monitor every server on the Internet to reduce exposure and improve security| | [Censys](https://github.discoverfinancial.com/vulnmgmt-org/censys-system-docs/blob/master/system-docs-template.md)|
|Arachni| | Web Application Security Scanner Framework| | |
|Nmap| |  Security Scanner, Port Scanner, & Network Exploration Tool| | |
|Netsparker| | Web Application Security Scanner.Netsparker is a leading web vulnerability management software tool used by information technology, security operations, and development teams worldwide | | |
|Fortify| | Static Application Security Testing| | [Fortify]()|
|Gitlab|
|Contrast| Active |Contrast is an interactive application security testing tool that blends static analysis security testing(SAST) and dynamic analysis security testing(DAST) techniques | |[Contrast](https://github.discoverfinancial.com/cs-eng-org/contrast)|
|Rapid7| 
|Wireshark| | Vulnerability Scanner.Wireshark is a real-time network protocol analyzer that continuously scans network traffic for vulnerabilities and suspicious activities| | |
|Appscan(HCL)| | application security testing|  
|Synopsys| | EDA tool. Semiconductor chip testing verification tool | | |
|Veracode| | Veracode is a cloud-based application security platform used to identify and remediate security vulnerabilities in software applications| | |
|Portswigger(Burp Suite)| |Web Application Security, Testing, & Scanning| | 
| Expanse | | Cybersecurity intellegence tool.Expanse indexes the entire global Internet to discover, track, and monitor what belongs to your organization| | |
| NowSecure | | DAST and SAST.The NowSecure tool integrates into Mobile Software Delivery pipelines via CI/CD processes | | [NowSecure](https://dta.discoverfinancial.com/products/nowsecure)|
|Pact| | consumer driven contrast testing tool| | [Pact](https://dta.discoverfinancial.com/products/pact)|
 ---------------------------------------------------------------------------


#### Type of Reports
| Report Type	| Purpose	| Additional Info |
| -----------| --------------| -------------| 
|Aggregate/Summary Reports | Jmeter,The aggregate report is the same as the summary report except the aggregate listener provides some additional parameters such as median | The Aggregate Report displays outcomes in a table format, with a line for each example independently and displays data about: </br> Throughput </br> KB/Sec worth </br> Average time</br>Median worth</br>90% line, 95% line,almost 100% line</br>Minimum response time</br>Maximum response time</br>Error %|
|Synthesis Report| A Synthesis Report is a mix between a Summary Report and Aggregate Report | It offers information about the following elements:</br>Samples</br>Average</br>Min</br>Max</br>90%</br>Line</br>Std. Dev</br>Error %</br>Throughout</br>KB/sec</br>Avg.Bytes</br>|
|HTML reports| Jmeter, graph view HTML | graphs</br>response time</br> Hits per second</br>Errors |
|Detailed test case reports |	Present specific details about individual test cases	| Status (pass/fail), execution time, associated issues/errors |
|Coverage reports	| Show code/functionality coverage by tests	| Metrics like code coverage, requirement coverage, or specified criteria |
|Trend analysis reports |	Display trends over time in test results	| Track progress, identify patterns, gauge improvements or regressions in software quality |
|Failure analysis reports| Focus on failed test cases and their details |	Detailed information on reasons for failure, error logs, screenshots for debugging |
| Execution history reports |	Showcase historical test run data |	Past executions, outcomes, changes/trends in test performance over time |
-----------------------------------------------

#### Type of Defects

| Defect Type	| Purpose	| Additional Info |
| -----------| --------------| -------------| 
| Functional defects| | |
| Usability defects | | |
| Performance defects | | |
| Security defects | | |
| Compatability defects | | |
----------------------------------------------------
 #### DFS specific TA frameworks/practices
| Practice | Desc| Required | Recommended | Comment | 
|-------| ------------------| ---| --| -------------|
| One-click(DFS) | One-Click Regression test suite has been implemented by Dollar-Bills Agile team to generate the Finance reports and validate them |Y| | [One-click regression test suite](https://dta.discoverfinancial.com/orgs/Dollar-Bills/articles/one-click_test-suite)
|Unit testing(DFS) | |Y| | [Unit Testing](https://dta.discoverfinancial.com/product/craftworx/practices/unit-testing?tab=conversations&page=1)|
|Regression testing(DFS)| |Y ||[Regression testing](https://dta.discoverfinancial.com/solutions/integrating-regression-testing-trident-pipeline)|
|Reflective testing(DFS)| | Y| | [Reflective testing](https://dta.discoverfinancial.com/products/digital-pymt-platform/docs/bestpractices/reflective-testing)|
|Mobile app testing(DFS) | | Y| |[Mobile app testing](https://dta.discoverfinancial.com/communities/test-guild/articles/mobile-app-security-testing)|
--------------------------------------------------------------------------
 

### Considerations
- **Security** - Need to ensure all security and privacy controls are present to harden CI/CD deployments and pipelines
- **Availability** - CI/CD systems should have proper availability SLAs defined and 
- **Governance, Compliance and Audit** - CI/CD system should meet all required governance, compliance and audit requirements.
- **Developer Experience** - CI/CD systems should be user friendly and not require steep learning curve so that Developers can focus on solving business problems. A unified single paint of glass system where Developers are not required to context switch constantly is desired.

### Glossary

* **CICD**: Continuous Integration and Continuous Delivery
* **Delivery Pipeline**: A delivery pipeline is a workflow that executes in an underlying orchestrator with a set of stages that describes how software will move from execution tool to deployment target in production for end users to consume. 
* **Artifact**: An artifact is a deployable component of an application, it can either ve an archive file or an image. 
* **GRC**: Governance, Risk and Compliance 
* **SBOM**: Software bill of material
* **VCS**: Version control system
* **SCA**: Software composition analysis
* **CI**: Continuous Integration
* **CD**: Continuous Delivery (manual gate to deploy to prod)
* **Continuous Deployment**: Deployment to production happens automatically, and requires mature automated testing and feature flag capabilities
* **DevOps**: DevOps is the combination of cultural philosophies, practices, and tools that increases an organization’s ability to deliver applications and services at high velocity: evolving and improving products at a faster pace than organizations using traditional software development and infrastructure management processes (AWS definition)
* **DevSecRegOps**: The practice of integrating development, security, regulation and compliance, and operations in each stage of software development life cycle process.
* **SDLC**: Software development life cycle
* **SAST**: Static application security testing
* **IAST**: Interactive application security testing
* **DAST**: Dynamic application security testing

### References 

1. DevOps Automated Governance Reference Architecture - IT Revolution Press, LLC, Portland, OR 97210
2. Continuous Delivery - Jez Humble, David Farley
3. CloudBees Modern CICD 
4. Continuous Integration, Delivery and Deployment: A Systematic Review on Approaches, Tools, Challenges
and Practices -  Mojtaba Shahin, Muhammad Ali Babar, Liming Zhu
5. https://aws.amazon.com/builders-library/automating-safe-hands-off-deployments/ - Clare Liguori 
6. https://aws.amazon.com/builders-library/going-faster-with-continuous-delivery/ - Mark Mansour
7. https://cloud.google.com/anthos-config-management/docs/tutorials/modern-cicd-anthos-reference-architecture
8. https://aws.amazon.com/devops/what-is-devops/#:~:text=DevOps%20is%20the%20combination%20of,development%20and%20infrastructure%20management%20processes.
9. [National Security Agency- NSA](https://media.defense.gov/2023/Jun/28/2003249466/-1/-1/0/CSI_DEFENDING_CI_CD_ENVIRONMENTS.PDF) 
