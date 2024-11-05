# Brand Guidelines and Enterprise Design Reference Architecture

The reference architecture template is a template model that represents the current or future/target state an architecture will rely on.

**Department:** Enterprise Architecture
\
**Organization:** Research and Development
\
**Domain:** Digital Experience
\
**Documentation Identifier:** RA-DE-05001
\
**Template Version** 1.03
\
**Template Last Modified** 08/23/2024
\
**Author:** Sujatha Sivaraman, Tom Makula, Lise Noble
\
**Sponsor:** Dan Gisolfi
\
**Jira Initiative [optional]:**
\
**Adoption Status:** DRAFT.

 <br>

## Requirements - Problem statement
DFS is looking to have a single source of truth for designing the digital UI/UX experience and to follow brand guidelines. Having a reference architecture to implement a standard and unified UI/UX experience and documenting brand guidelines would improve our product ecosystem and automate design standards and brand signature and save cost and time.

This reference architecture would help us deliver our brand promise by creating exceptional product experiences that meet and exceed our customer wants, needs and expectations. A standardized enterprise design approach would resolve legal repercussions and help us automate our design to meet regulatory needs and help the design team focus on delivering the best UI/UX experience.

The success of the design for standardization approach depends heavily on how successful designers are at implementing and using the current available set of tools and reusing them for creating new browser applications by minimizing the total number of tools used.

Unified Design System will support and improve the customer-centered design-thinking process to solve problems. Inclusive design and unified and compatible IOT device experiences and different modes and adapting to emerging technologies and keeping up with market trends without dedicating time to redoing all design to the latest technology,​ but autoscale and auto adapt.
### Roadmap
![Roadmap](images/UDS_Roadmap.png)
#### Fundamentals
* DFS as an organization with higher CSAT score should reflect the same commitment in the product design as well. 
* UDS would make DFS brand instantly recognizable in a crowded market landscape.
*  UDS focuses on foundational design elements that make up a brand’s visual identity. DFS core values should translate to UI/UX and Design goals.
* Equity incorporated via accessibility in design products.
* Investing in the interaction with customers as goal by enabling sharing in our product design will increase the visibility for our product in the market.
#### Design Research
* "Design research" in user design refers to the process of systematically gathering and analyzing data about potential users to understand their needs, behaviors, and pain points, which then informs the design process of a product or service, ensuring it is user-centered and effectively solves their problems; essentially, it's the practice of conducting research to directly inform design decisions by putting the user at the center of the development process
* Design decisions made with inputs from below as requirements
  * Inputs from customer via SWOT analysis, customer survey
  * Social media monitoring and market analysis and competition watch
  * Alpha , Beta testing and direct from customer outreach channels
#### User Experience
* User experience (UX) design is the process of creating products that are easy and enjoyable for users to interact with. Focusing on improving and refining the userexperience 
  * Using enterprise wide design tools to implement user design
  * Streamlining prototype creation where designer, engineers could work together
  * Using enterprise wide wireframing tools to standardize UI/UX
#### User Interface
* User interface (UI) design is the process designers use to build interfaces in software or computerized devices, focusing on looks or style. UI design refers to graphical user interfaces and other forms—e.g., voice-controlled interfaces. User interface should match skills, expectations and needs of customers, all users.
  * Design principles 
  * Experience, empathy mapping
  * Data handling
#### Communication and Colloboration
* Collaboration in user design, also known as participatory design, co-design, or cooperative design, is a holistic approach that involves multiple stakeholders to create better design solutions
  * Application Development and Engineering team develops application with customer use in mind.
  * Design team focuses on customer interaction and partnering with development team would help better userfriendly deliverables in parallel.
  * Automation and integrating design with CICD pipelines will ease the separate effort needs in testing and ensuring compliance, accessibility challenges we have today.
#### Brand/Design
* Branding in user experience design (UX design) is the process to create a unique and cohesive identity for a product or service to resonate with users. It encompasses elements such as logo, color scheme and tone of voice.
  * Brand design is the process of crafting a brand’s visual identity by creating a unified system of design elements, including a logo, colors, typography, illustration, and photography
  * Brand design acts as the bridge between research, strategy and brand experience, including touchpoints like website, marketing collateral, packaging, presentations, etc.,
  * Creating DFS specific branding not only makes DFS brand stand out but enhances the possibility of increasing design patents.

-------------------------------------------------------------------
### Unified Design System to Design ops journey
![Roadmap](images/UDS_to_DO.png)


UDS | Design Ops | Entity | Desc | Tools |
----------| ----------| --------| --------| -------|
**Desirable** | UI/UX elements | Gestalt | Getsalt theory describes how things are put together to form a whole object. Objects that are visually similar in size, shape and / or colour will be visually grouped together, even if those objects are not near each other  | Figma |
| | |  Contrast	| The design principle contrast refers to the use of visually different elements.  In addition to capturing attention, contrast can guide the viewer's eye to a focal point, highlight important information and add variety, or even drama, to a design | Figma |
| | | Proportion| Proportion is about the balance or harmony between elements that are scaled. UX designers often use scale to make the most important elements in a design bigger than less important elements, which helps create emphasis and contrast | |
| | | Hierarchy | 	The hierarchy principle in UI/UX design is a fundamental design principle that arranges elements on a page to guide users' attention to the most important information | |
| | | Emphasis |	Emphasis, as a design principle, works hand-in-hand with hierarchy to highlight information in a design. The goal of emphasis is to call the viewer's attention to a particular design element | |
| | | Proximity |	The proximity principle of design is a visual grouping principle that states that items that are close together are likely to be perceived as related| |
**Agnostic** | 	Compatibility |	Device |	Compatibility issues refer to the problems that arise when different devices, operating systems, software, or hardware components do not work well together or cause errors, glitches, or crashes. Either we could handle it as prevention as part of UDS or as part of cure during testing phase | Lambdatest </br>BrowserStack</br></br>CBT
| | | Network|	"Network Compatibility" means product shall comply, with industry standards, ANSI,ISO, ETSI, NEBS etc, | |
| | | Version | | |
| | | Browser | | |
| | | Hardware/Software| | |
### SMART objectives
* Reliability
* Flexibility
* Customization, Personalization, Standardization
* Compliance adherent
* Brand recognition
* Less training
* Customer satisfaction
* Revenue
* Fast delivery
### Component Diagram

This diagram will demonstrate how components of the reference architecture are connected to form a system, application, platform or service.  Flow through the reference architecture might be included to further describe the architecture.

![DesignOps](images/UDS_component.png)


### Potential Use Cases

* Improving and automating UI/UX experience designing
* Accessibility, ADA, WCAG Compliance checker
* Integration with other development tools
* Code generation
* Whiteboarding and Collaboration
* GAAP compliance
* Automation,CICD pipeline
* Content and Digital Assest Management
* Standarized compliant presentation and animation

### Tools and functionality
| Tool | Prototyping | Wireframing | Collaboration | Plugins | UI design | OS |
|--------- | --------- | ------- | ------- | ------- | ------ | -------| 
| Figma | x | x | x | x | x | windows, Mac |
| Adobe XD | x | | x | x | x| Browser based |
| Adobe Express | | | | | | |
| Sketch | x|x | x|x |x| Mac |
| Wireframes | | x | | | |
Bluerush | | | x | |Animation, Video | Windows, Mac| 
| Invision | | | x | | x | Windows, Mac, Linux |
| Zeplin | | | x | | x(focus on delivery) | Windows, Mac |
| Miro | | | x | | | Windows, Mac|
| Axure | x | x | x | | | Windows, Mac|
| Lucid chart | | | x | | |  Windows, Mac |
| Webflow | | | | | x(website) | Windows, Mac|
| Canva | | | | | x| Windows, Mac|
| QuarkXpress | | | | | x| Windows, Mac|
| Anima | | | x | |AI | Windows, Mac| 

### Components and Capability Narrative 
As the intention of this artifact is to depict a design workflow through the enterprise, many of the components are shared / common across the enterprise and ultimately increase the inclusivity and improve the UI/UX experience of all DFS customers.  The design capabilities here are also generalized at a high level as the intent is to indicate where they are relevant to DFS design and brand standard and the developers and engineers can get access they require to perform their intended function. 
List each component or capability and a description of each.
#### Design system
* Standard agnostic collaborative design tool would be ideal across roles and valuestreams. Engineers can develop and focus on applications while collaborating with designers who can translate their vision in parallel. Standard design tools make it inclusive. Makes user friendly, personalized and customer focused designs possible. 
#### Code generation
* Standard design tools are very userfriendly and doesnt depend on technical savy or constant upskill through explicit training. GUI- drag and drop functionality can automatically be converted to code snippets which makes it easier to scale, adapt, modify. Customization doesnt require explicit efforts.
#### Token shared integration 
* Design tools like Figma for example allow integration with development tools, animation tools via exchange of tokens which makes it easier to collaborate and exchange ideas realtime and bring in best input from experts in their respective areas..
* Integrating with our current VCS,  the design guidelines and standards can be shared efficiently and effectively across value streams. Different roles can colloborate together to provide user-focused inclusive delivery of web applications.  
#### Single source of truth for brand standards and design needs
* Collections of these tools will represent single source to satisfy all the needs and references required to deliver customer-focused inclusive need.
#### Artifical Intelligence 
* Design tools are constantly upkeeping with latest technology and market trends. Animation and prototyping tools offer verbal conversation to code conversion functionality.
#### Version control
* Apart from plugin possibility with version control tools, design tools also provide inbuilt version control that can be shared across enterprise.
#### Whiteboarding and Collaboration
* Design tools provide real time collaboration. Designers and Engineers can collaborate together and design the best user experience for customers. Design tools being part of automation can reduce impact analysis and retrospective and proactive fixing. Testing efforts related to web accessibility can be covered and autocorrected in design phase.
#### Quality Assurance and Compliance 
*  Application development with design tools can proactively fix accessibility WCAG  needs. Any change in code affecting the web layout and UI layout can automatically be adjusted to meet the WCAG standards. 
#### Project Management , Ticketing and Tracking system
* Integration of design tools and project management tools saves time and increases productivity. Ticket and Tracking integration makes task completion and tracking easier and efficient.
#### Realtime feedback sharing
* Design tool also offer sections to track comments and instant feedbacks. The feedback can help collaborate better and deliver the best version of the product.


### Considerations
Considerations critical to the intended consumption of the reference architecture will be listed here by section.  Considerations most used are as follows:
#### Governance
* Unified design system using approved enterprise tools helps scale faster, implement sooner. 
* Everytime there is application change, enterprise approved tools and plugins remove the need for the additional steps that need to explicitly done by developers and design engineers. 
* Compliance team doesnt need to explicitly approve everytime there is a change. The appropriate compliance plugins will implement the guidelines via all IoT devices.
#### Availability, Reliability, Resiliency
* Enterprise tools - can autoscale and concurrently support multiple designers and developers. They can be used and reused simultaneoulsy across the board. 
#### Data 
* Design tools dont deal with customer data.
* Design pattern artifacts available in repository can serve as architecture and solution building blocks and can be reused efficiently.
 #### Integration
 * Enterprise design tools support lot of plugins and can integrate with almost every other version control tool, compliance checker tool, animation tools, project management tool, tracking tool available in DFS today. 
 * This makes the design team deliver cohesive designs that are user-focused and compatible across platforms, products.
 #### Efficency
 * Unified design system and enterprise tools integrated well with all other tools that can auto adapt and autoscale.
 * Our guidelines will improve efficiency across various value streams and not just Design but R&D, Technology innovation, Enterprise stratergy, compliance, application development, automation and testing teams etc., 

### Glossary

Terms and acronyms described
* UI/UX - User Interaction, User Experience
* UDS - Unified Design system
* CICD - Continuous Integration and Continuous Delivery/Continuous deployment
* CSAT - Customer Satisfaction Score

### Example template - Not an actual Discover architecture

Example [template](https://github.discoverfinancial.com/spete13/citizen-ai/blob/master/index.md)
