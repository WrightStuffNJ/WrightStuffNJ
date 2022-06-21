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
   - Administrator: An employee of the Diversity Counsil who manages administrative tasks such as approving new non-profit service providers.
   - API Gateway: A proxy that sits between a client and a collection of back-end services that directs api calls to the proper service and returns the appropriate results.
   - AWS Connect: Amazon Web Service Connect is an coud based IVR server provided by AWS for creating phone based customer contact systems.
   - Back End for Front End: Back end for front end is a microservices pattern that breaks away from monolithic systems that utilize a single api for all clients and breaks them up into specific client type api's that provide just the services needed for the consuming client.
   - Candidate: Users who wish to utilized the services provided by one of the Diversity Counsil's non-profit orgranizations.
   - Content Delivery Network (CDN): A geographically distributed group of servers that work together to provide fast delivery of Internet content. A CDN provides faster access and delivery of content over the internet by placing the content closer to the users.
   - Email Service: A system that handles the generation and delivery on email messages to clients at scale.
   - Graph Database: Graph databases are purpose-built to store and navigate relationships. Relationships are first-class citizens in graph databases, and most of the value of graph databases is derived from these relationships. Graph databases use nodes to store data entities, and edges to store relationships between entities. An edge always has a start node, end node, type, and direction, and an edge can describe parent-child relationships, actions, ownership, and the like.
   - Identity and Access Management (IAM):  provides fine-grained access control across all of AWS. With IAM, you can specify who can access which services and resources, and under which conditions. With IAM policies, you manage permissions to your workforce and systems to ensure least-privilege permissions. Note, other cloud providers have similar authentication and authorization that could be used as well, this is the AWS implementation.
   - Interactive Voice Recognition (IVR): is an automated telephony system that interacts with callers, gathers information and routes calls to the appropriate recipients and services.
   - IVR Server: Server based software system for providing Interactive Voice Recognition services, such as AWS Connect.
   - Microservices: An architecture design for building a distributed application using containers. Each service of the system is independent. 
   - NPO: Non-Profit Organization that provides services or can apply to provides services through the Diversity Counsils website.
   - Offerings: Services provided by the registered non-profits of the Diversity Counsil.
   - Provider: A registered NPO that is providing services to the Diversity Counsil's clients.
   - Serverless (Lambda) Functions: AWS Lambda is a serverless compute service that runs your code in response to events and automatically manages the underlying compute resources for you. 
   - Simple Notification Service (SNS): SNS is an AWS email service that allows management and delivery of email messages to clients at scale.
   - Static Content: Static content is any file stored on a server that is the same every time it is delivered to users. The system utilizes AWS S3 (Simple Storage Service) for storing all static contect.
   - Step Functions: A step function is a series of serverless lambda functions executed in a specific order to perform a given set of tasks.
   - Workflow Engine: A software application that manages business process. 
