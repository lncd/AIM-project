## Cover sheet

See separate file

## Our proposal

The Linkey project will provide JISC and the community with a Case Study and related technical outputs of the implementation of the OAuth 2.0 standard as part of an institution-wide strategy for access and identity management at the University of Lincoln. 

The primary driver for this is to improve the student experience and meet the following objectives:

1. Richer sharing of data between applications: A student or lecturer should be able to identify themselves to multiple applications and approve access to the sharing of personal data between those applications.
2. A consistent user experience (UX): We are aiming for ‘consistent sign on’ rather than 'single sign on', where the user is presented with a consistent UX when signing into disparate applications.
3. Rapid deployment: New applications that we develop or purchase should be easier to implement, plugging into either OAuth or the UAG and immediately benefiting from 1) and 2).

### Context

One of the lasting outcomes of our Total Recal ‘rapid innovation’ project in 2010, was that Alex Bilbie wrote the first (and only) OAuth 2.0 server for the CodeIgniter PHP development framework that we use. Since then, he’s been refining it and with every new project, we’ve been using it as part of our API-driven approach to development. As far as we know, the use of the OAuth 2.0 specification, which should be finalised at a forthcoming IETF meeting, is not yet being used by any other university in the UK. There are some examples of OAuth revision A in use in the sector, but not OAuth 2.0, which is a major revision currently in its 23rd draft.

Following a recent meeting between ICT and the Library, we agreed to take the following steps to achieving our stated objectives:

1. All library (and ICT) applications that we operate internally must have Active Directory sign-in instead of local databases. Almost all of our applications achieve this already. This is the first step towards step (3).
2. All web-based applications must offer a consistent looking sign-in screen based on the current http://sso.lincoln.ac.uk design (which uses the Common Web Design). This is the second step towards (3).
3. All systems must implement web-based single sign on via OAuth, SAML or ADFS, using either the Microsoft Unified Access Gateway (UAG) or the OAuth server, which will include the 'SAML 2.0 Bearer Assertion Profiles for OAuth 2.0' specification.


### Building on recent innovation

Since the Total Recal project, we’ve used OAuth 2.0 for a number of projects: Jerome, data.lincoln.ac.uk, Zendesk, Get Satisfaction, and more recently Orbital and ON Course projects.  Our single sign-on (SSO) service at https://sso.lincoln.ac.uk is the gateway to our current OAuth 2.0 implementation, which will soon be upgraded to run across two servers for redundancy. Having been researched, developed and implemented under early JISC-funded projects, OAuth 2.0 has been formally adopted by central ICT Services, and so staff and students are gradually being given control over what services their identity is bound to and what permissions those services have.

Most recently, the Orbital project has extended our OAuth 2.0 server to include some of the optional parts of the specification which we’ve not been using at Lincoln, such as refresh tokens and using HTTP Authentication with the client credentials flow. This means that the server is able to drop straight into a wider range of projects and services. However, many of our larger applications, such as WordPress, Exchange, Blackboard, HIP, EPrints and Sharepoint, remain disparate from one another, with no sharing of data, except for that provided by the Active Directory. 

Drawing of current AIM process: 

![Current situation](https://github.com/lncd/AIM-project/raw/master/SSOCurrentSituation.png)

### Anticipated Technical Approach

In the Total Recal project, we released version 1 of the server code but have learned a lot since that project through integrating OAuth with other services. Version 2 of our OAuth server is more representative of our current implementation and fully implements the latest draft (23) of the specification.

At the time of writing, the current institution-wide use of OAuth is limited to Zen Desk, Gateway, the Staff Directory, the Student Union website and Posters@Lincoln. Projects such as Jerome, Orbital, and ON Course, as well as three 3rd year Computer Science student dissertation projects are using it, too. Our intention is to use OAuth alongside Microsoft’s Unified Access Gateway (UAG), using SAML as a bridge to OAuth via the 'SAML 2.0 Bearer Assertion Profiles for OAuth 2.0' specification.

Drawing of intended implementation: 

![Intended situation](https://github.com/lncd/AIM-project/raw/master/SSOIdealSituation.png)

Like our related work on staff profiles, the need to improve access and identity across the institution is becoming increasingly apparent as staff and students become accustomed to the way access and identity works elsewhere on the web. For Lincoln, a combination of OAuth and UAG is the preferred route to achieving consistent sign on across all applications, bridging both the internally facing business applications managed by ICT (e.g. Sharepoint, Exchange, Blackboard) and the more outward facing academic and social applications such as those developed and run by the Library and the Centre for Educational Research and Development.

## Our workplan

### Methodology

This is a 12 month project, largely undertaken by one full-time Web Developer working in the central ICT Online Services Team (Alex Bilbie). The Principal User on the project will be Dave Masterson, Head of Electronic Library Services, who has been charged with improving the usability of our Library's online services. The Principal Investigator/Project Manager for the project will be Joss Winn, Senior Lecturer in CERD and co-ordinator of the LNCD group (http://lncd.lincoln.ac.uk). 

The project will be run using the 'Crystal Clear' agile methodology, which we use on other development projects. Crystal Clear is characterised by the following:

1. Seat people close together, communicating frequently and with goodwill.
2. Get most of the bureaucracy out of their way and let them design.
3. Get a real user directly involved.
4. Have a good automated regression test suite available.
5. Produce shippable functionality early and often.

Within this environment, we practice open development (http://lncd.lincoln.ac.uk/about/how-we-work/), using Github as a source code repository (http://github.com/lncd) and Pivotal Tracker to iteratively manage project tasks (e.g. Our tracker for the Orbital project https://www.pivotaltracker.com/projects/366731). We have recently implemented an automated regression test suite and practice 'Constant integration' using the Jenkins software (http://orbital.blogs.lincoln.ac.uk/2012/01/18/jenkins-build-my-software/). Such an environment will support Alex on this project by ensuring that his code is available for peer-review by colleagues and publicly available for scrutiny. Code will be constantly tested by Jenkins for quality assurance and thereby provide working code for regular user testing. 

Dissemination will be both informal and formal. Community engagement will be ongoing through the project through our project blog and Twitter accounts. We have demonstrated in past projects that we maintain active project websites and use social media effectively. More formal dissemination will take place through the use of Press Releases, a public workshop and the case study.

### High-level Workplan

Table goes here.

### Benefits

We believe this is a distinctive bid that clearly builds on previous JISC-funded projects. It offers a number of benefits to project stakeholders:
To students and academic staff: To technical staff: 
To the University of Lincoln: To the university sector: 
To the public: 

### Stakeholder Analysis

Table goes here.

### Deliverables

The Linkey project will provide two main deliverables:

1. A case study of our implementation of OAuth 2.0 alongside Microsoft's UAG product.
2. Continued development of our open source OAuth 2.0 server, including an implementation of the 'SAML 2.0 Bearer Assertion Profiles for OAuth 2.0' specification and other relevant extensions to the main standard. 

Furthermore, we will

### Risks

bar

### Sustainability

foo

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