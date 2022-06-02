# Solution Intent - Diversity Cyber Council
A **Solution Intent** is the repository for storing, managing, and communicating the knowledge of current and intended solution behavior. In short, the Solution Intent should describe *what* we wish to build.

## Business Vision
### Basic Information
Diversity Cyber Council is a 501c3 Non-Profit Organization (NPO) that serves under-represented demographics in the tech industry by facilitating education, training, and staffing opportunities to establish a sustainable and diverse talent pipeline to the workforce. Our vision is to enhance inclusion and representation in the tech industry through training, mentoring, networking, and visibility programs.

### Business Goal
Our goal is to establish a sustainable and diverse talent pipeline that extends career equity to underrepresented demographics by providing access to competent training programs that lead to direct employment opportunities.

### Program Description - Spotlight App/Platform
The Spotlight App Project is a sustained effort to amass a coalition of nonprofits in order to address specific needs within the communities we serve by leveraging a centralized platform as the base of operations to collaborate and make a collective impact.

### Tagline: Illuminate Possibilities
The Divercity Cyber Council system is designed around illuminating possiblities. Candidates can see what's possible by browsing or searching offerings. Providers can see what other providers offer. Administrators have a wealth of reports available, providing them insight into what providers and offerings are getting the most use and what areas are underserved. Additionaly the system will show recommended offerings to candidates based on their location or past searches and engagement. Non-profits will receive insight into what offerings are hot and spotlight users. Administrators can see which offerings are often taken together, assisting them in creating roadmaps. All of which contributes to illuminating possiblities, not just for candidates but for non-profits as well.

### Problem Statement
1. The decentralization and lack of support between nonprofits create gaps of service and overall impact.
2. The lack of visibility of nonprofit groups and offerings creates a barrier of access to the people we aim to serve.

### Technology Solution Description
Nonprofit Networking Hub & Diverse Candidate Career Case Management Tool

## Scope
### In Scope
?

### Out of Scope
?

### Minimum Viable Product
?

### Additional Features
?

## Specifications
?

## Solution Context
### Goal Context
The Spotlight system is designed to support three types of users; Candidates, Non-Profit Providers, and Administrators. Administrators and Non-Profit users will access the system via web pages, either mobile or desktop. Candidates can access the system via web pages as well. Additionally candidates without access to a browser can use a regular phone to call the Interactive Voice Response (IVR) system. It will allow them to retrieve lists of providers or offerings and to get contact information. The system has the ability to contact any user by email, or candidates via SMS.
![Goal Context diagram](/assets/images/DiversityCyberCouncil-ContextDiagram.jpeg)

### High-Level Solution
The system is designed at a high level to be built on cloud services. This reduces inital cost and reduces the maintenance effort while increasing the ability to handle peak demand. Behind the scenes microserices (called a Back End for Front End) and a workflow engine handle most of the work while a graph database handles persistent storage. 
![High-Level Solution Diagram](/assets/images/DiversityCyberCouncil-HighLevelSolutiondiagram.jpeg)

## Key Performance Indicators
?

## Risks
- Lack of adoption by Nonprofit providers.

## Dependencies
- External 3rd party NPOs will need functional website and/or customer service phone line

## Data Analytics
Data analytics will be used to enhance the system value for participants in a number of ways, inclding:
  - Administrators
    - Which offerings are most used
    - Which geographical areas are underserved
    - Which offerings are often taken together, suggesting a potential roadmap
  - Candidates
    - Recommend offerings based on past engagement and searches
    - Recommend 'hot' offerings in their location
  - Non-Profits
    - Which offerings are most used
    - Which offerings are least used
    - Which candidates have had the most engagement

## Solution Design
While this **Solution Intent** is designed to show *what* we intend to build, the **Solution Design** will show the details on *how* we will build it. 
Click on the following link to view the Solution Design for the [Spotlight Platform](/pages/SolutionDesign.md)

## Acceptance Criteria
?

### Assumptions
Community Leader will be an NPO, assigned by an Admin... in agreement with the NPO
Mentorship will be an offering from an NPO

### Functional Requirements
- Acceptance Criteria
  - Establish a way to incentivize engagement such as sharing of resources, collaboration, networking, facilitating introductions, and partnerships
  - Categorize/tag nonprofit support services to match candidate needs identified in the onboarding assessment
  - Easy to use interface for end-user
  - Candidate progress tracking
  - Engagement tracking
  - Automatic matching of Non-Profit offerings to Candidate requests
  - Platform allows offerings to contain rich text, links, and downloadable readable content such as PDFs (no other download types)
  - Offerings must support:
    - Organization name
    - Organization Description
    - Website
    - Unique Identifier (assigned by admin)
    - Other identification information
  - Operational reports (for use by Admins)
  - Analytical reports (for use by Admins)

### Non-Functional Requirements
- Usability
  - The system must support users with no access to a smart phone or computer
  - All web pages must meet Web Content Accessibility Guidelines WCAG 2.1
- Security
  - All external communications between the system and clients must be encrypted 
  - Only strong passwords will be allowed
- Perfomance
  - Pages must load within 2 seconds
  - System must match capacity with demand elastically
<!---
   Comments
--->
