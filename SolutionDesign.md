# Solution Design - Spotlight Platform
#### Created by WrightStuffNJ
A **Solution Design** is the repository for storing, managing, and communicating the knowledge of the intended solution's makeup in detail. In short, the Solution Design should describe *how* we will build the solution.

## Goal Design
The following diagram details the solution design:
![Solution Diagram](/assets/images/DiversityCyberCouncil-HighLevelSolutiondiagram.jpeg)

## Component Diagram
The following diagram illustrates the solution at a component level.
![Site Map diagram](/assets/images/DiversityCyberCouncil-ComponentDiagram.jpeg)

## User Interface Diagrams
#### Site Map
The following diagram illustrates the flow through web pages as users exercise the site.
![Site Map diagram](/assets/images/DiversityCyberCouncil-SiteMap.jpeg)

#### Wireframes
The following diagram shows the simplified mockups of the web pages in the system. 
![Wireframe diagram](/assets/images/DiversityCyberCouncil-Wireframes.jpeg)

#### Interactive Voice Response (IVR) Map
The following diagram shows the flow through menus for users connecting to the interactive voice response system. 
![IVR Map diagram](/assets/images/DiversityCyberCouncil-IVRMap.jpeg)

## Workflow Diagrams
The following diagrams show the workflow used when candidate and non-profit users register with the system. Note that these workflows are triggered by events raised by the Graph Db.
![Workflow diagram](/assets/images/DiversityCyberCouncil-WorkflowDiagram.png)

## Data Diagram - Graph Model
The following diagram shows the nodes and connections that make up the Graph Db.
![Graph data model diagram](/assets/images/DiversityCyberCouncil-GraphModel.jpeg)


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

## Sequence Diagram  
The following diagram shows the operational flow between components.
![Sequence diagram](/assets/images/DiversityCyberCouncil-SequenceDiagrams.jpeg)
![Sequence Diagram](/assets/images/DiversityCyberCouncil-SequenceDiagrams2.jpeg)

## Test Plan
### Purpose
This section describes the plan for testing the Spotlight system. It will:
  - Identify the test requirments at a high level
  - Describe the test strategies to be used
  - List the resources required
  - Detail the deliverables for the test phase
### Test Requirements
  - Verify the functional requirements are met
  - Verify database functionality
  - Verify the user interfaces
  - Verify performance and scaling
  - Verify security and access control
### Test Strategy
  - Execute each use case, workflow, and function 
  - Execute database queries to exercise each domain element with valid and invalid data, verifying end state
  - Exercise each UI element, verifying they perform properly while meeting the requirements
  - Validate system performance under minimal and increasing load, verifying the system scales appropriately
  - Validate that access security meets specifications, and that each user role is appropriately represented
### Test Resources
   - Test Manager: Provides oversight, direction and reporting
   - Test Designer: Creates test plan and implements test cases
   - System Tester: executes the tests
### Test Deliverablers
  - Test Plan
  - Test Suite
  - Test Data Sets
  - Test Scripts
  - Test Results and Evaluation


### Glossary
   - Administrator:
   - Back End for Front End:
   - Candidate:
   - Graph Database: 
   - IVR: 
   - Microservices:
   - NPO: Non-Profit Organization
   - Provider:
