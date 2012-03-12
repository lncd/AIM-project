## Cover sheet

See separate file

## Our proposal

The Linkey project will provide JISC and the community with a Case Study and related technical outputs of the implementation of the OAuth 2.0 standard as part of an institution-wide strategy for access and identity management at the University of Lincoln. 

The primary driver for this is to improve the student experience and meet the following objectives:

1. Richer sharing of data between applications: A student or lecturer should be able to identity themselves to multiple applications and approve access to the sharing of personal data between those applications.

2. A consistent user experience (UX): We are aiming for ‘consistent sign on’ rather than 'single sign on', where the user is presented with a consistent UX when signing into disparate applications.

3. Rapid deployment: New applications that we develop or purchase should be easier to implement, plugging into either OAuth or the UAG and immediately benefiting from 1) and 2).

## Context

One of the lasting outcomes of our Total Recal ‘rapid innovation’ project in 2010, was that Alex Bilbie wrote the first (and only) OAuth 2.0 server for the CodeIgniter PHP development framework that we use. Since then, he’s been refining it and with every new project, we’ve been using it as part of our API-driven approach to development. As far as we know, the use of the OAuth 2.0 specification, which should be finalised at a forthcoming IETF meeting, is not yet being used by any other university in the UK. There are some examples of OAuth revision A in use in the sector, but not OAuth 2.0, which is a major revision currently in its 23rd draft.

Following a recent meeting between ICT and the Library, we agreed to take the following steps to achieving our stated objectives:

1. All library (and ICT) applications that we operate internally must have Active Directory sign-in instead of local databases. Almost all of our applications achieve this already. This is the first step towards step (3).

2. All web-based applications must offer a consistent looking sign-in screen based on the current http://sso.lincoln.ac.uk design (which uses the Common Web Design). This is the second step towards (3).

3. All systems must implement web-based single sign on via OAuth, SAML or ADFS, using either the Microsoft Unified Access Gateway (UAG) or the OAuth server, which will include the 'SAML 2.0 Bearer Assertion Profiles for OAuth 2.0' specification.


## Building on recent innovation

Since the Total Recal project, we’ve used OAuth 2.0 for Jerome, data.lincoln.ac.uk, Zendesk, Get Satisfaction, and more recently Orbital and ON Course projects.  Our single sign-on (SSO) service at https://sso.lincoln.ac.uk is the gateway to our current OAuth 2.0 implementation, which will soon be upgraded to run across two servers for redundancy. Having been research, developed and implemented under early JISC-funded projects, OAuth 2.0 has been formally adopted by central ICT Services, and staff and students are gradually being given control over what services their identity is bound to and what permissions those services have.

Most recently, the Orbital project has extended our OAuth 2.0 server to include some of the optional parts of the specification which we’ve not been using at Lincoln, such as refresh tokens and using HTTP Authentication with the client credentials flow. This means that the server is able to drop straight in to a wider range of projects and services. However, many of our larger applications, such as Exchange, Blackboard, OpenAthens, EPrints and Sharepoint, remain disparate from one another, with no sharing of data, except for that provided by the Active Directory. 

Drawing of current AIM process: https://github.com/lncd/AIM-project/raw/master/SSOCurrentSituation.png

## Quality of Proposal and Robustness of Workplan

### Methodology

We use an agile approach to developing our web services, relying on regular, active input from users, working iteratively on short 1-2 week code sprints. To support this methodology, we use a tool-set incorporating Codeigniter, a PHP development framework, Github, a distributed source-code repository and Pivotal Tracker, for project and personal task management. For this project, we will also use our institutional Get Satisfaction account for supporting and managing user feedback and requests and Zen Desk for long-term support. Each of these tools is integrated at the API level, allowing us to easily tie user feedback to project tasks and to the development of code in a way that is transparent. Because we use an ‘agile’ approach to project management, much of our work will be performed iteratively, relying on close engagement with our users.

Dissemination will be both informal and formal. Community engagement will be ongoing through the project through our project blog and Twitter accounts. We have demonstrated in past projects that we maintain active project websites and use social media effectively. More formal dissemination will take place through the use of Press Releases, workshops, case studies, conference and journal papers.



### High-level Workplan

### Anticipated Technical Approach

In the Total Recal project, we released version 1 of the server code but have learned a lot since that project through integrating OAuth with other services. Version 2 of our OAuth server is more representative of our current implementation and fully implements the latest draft (23) of the specification.

At the time of writing, the current institution-wide use of OAuth is limited to Zen Desk, Gateway, Staff Directory, Student Union website and Posters@Lincoln. Projects such as Jerome, Orbital, and ON Course, as well as three 3rd year Computer Science student dissertation projects are using it, too. The plan is to use OAuth alongside Microsoft’s Unified Access Gateway (UAG), which can talk SAML to OAuth via the OAuth SAML 2.0 specification. 

Drawing of intended implementation: https://github.com/lncd/AIM-project/raw/master/SSOIdealSituation.png

### Benefits

We believe this is a distinctive bid that clearly builds on previous JISC-funded projects. It offers a number of benefits to project stakeholders:
6.2 To students and academic staff: Researchers will benefit from a state-of-the-art research data management infrastructure with supporting training, documentation and policy. Through the re-use and integration with other services such as the Institutional Repository, My Calendar and the Jerome discovery tool, researchers will enjoy a richer, more integrated research environment that helps foster cross-disciplinary collaboration internal and external to the university. Researchers and their partners will be assured that their data is stored and transported securely, conforming to third-party certification where appropriate. A web-based service will provide tools for accessing, querying and downloading the data where appropriate.6.3 To technical staff: An opportunity to further learn, develop and embed recently adopted technologies (MongoDB, OAuth, HTML5, etc.) and provide appropriate training to staff outside the immediate project team resulting in broader staff development opportunities. The prestige of receiving funding for the project would provide us with further leverage to introduce new ideas, technologies and practices in our day-to-day work. We recognise the need for continued innovation in our online services and welcome the opportunity for peer-review that the community engagement and dissemination requirements of externally funded projects bring to our work.6.4 To the University of Lincoln: As with our Institutional Repository project, the Orbital project will provide the opportunity to both develop the requisite policy and technical infrastructure for managing research data at the university as well as lead to institutional change in terms of researcher practices and broadening the skills and experience of our ICT staff. Whereas some of our previous JISC-funded projects have focused on ‘rapid innovation’, the remit of the Orbital project is much broader and with high-level endorsement will lead to the long-term adoption of new practices, policy and technologies. The Orbital project will also provide the university with a clearer framework for managing research data, making it more straightforward to provide assurances to funders of our research, such as the Research Councils.6.5 To the university sector: We aim to demonstrate efficiency through the re-use of previous JISC-funded projects at the University and offer an assurance that the project will lead to￼6
a service that is used. We will also re-use other funded work such as the ERIM, IDMB26 and DPM- ESRC27 projects, as well as adapting the training materials produced under the MRD programme.6.6 To the public: Where appropriate, data will be publicly accessible from our http://data.lincoln.ac.uk service, possibly pre-empting the need for FOI requests and ensuring the upmost transparency with regards to our research processes. Consumers of open data will benefit from attractive, well-documented APIs.

### Stakeholder Analysis

### Deliverables

Two of the outputs we’ll propose to JISC are a case study of this work, as well as further development of the open source server Alex and Nick have been developing including an implementation of the OAuth SAML specification that we’ll share. Like our related work on staff profiles, the need to get access and identity right is becoming increasingly apparent as staff and students become accustomed to the way access and identity works elsewhere on the web. For Lincoln, a combination of OAuth and UAG is the preferred route to achieving consistent sign on across all applications, bridging both the internally facing business applications managed by ICT (e.g. Sharepoint, Exchange, Blackboard) and the more outward facing academic and social applications such as those developed and run by the Library and the Centre for Educational Research and Development.

### Risks

### Sustainability

### IPR

### Engagement with the Community

foo

## Budget

bar

## Previous Experience of the Project Team

foo

## FOI Tick List

bar

## Supporting Letter

foo