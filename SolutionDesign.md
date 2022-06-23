# Solution Design - Spotlight Platform
#### Created by WrightStuffNJ
A **Solution Design** is the repository for storing, managing, and communicating the knowledge of the intended solution's makeup in detail. In short, the Solution Design should describe *how* we will build the solution.

## Goal Design
The design at its heart is simple: Web users connect to the static content storage or workflow engine and are served up pages of content. The workflow engine is supported by the microservices (called a Back End for Front End) as well as a Graph database. Telephone users connect to the Interactive Voice Response server which pulls content from the static content storage. <BR>
Layered on top of that is Cognito, which handles authentication and authorization.<BR>
We added in an API Gateway to allow web pages to be responsive, active entities for an engaging experience. <BR>
A content delivery network component rounds out the collection, ensuring performance at the edge remains strong.<BR>
The following diagram details the high-level solution design:
<figure>
  <img src="/assets/images/DiversityCyberCouncil-HighLevelSolutiondiagram.jpeg" width="800">
  <figcaption>Solution Diagram</figcaption>
</figure>

## Component Diagram
The following diagram illustrates the solution at a component level.
<figure>
  <img src="/assets/images/DiversityCyberCouncil-ComponentDiagram.jpeg" width="800">
  <figcaption>Component Diagram</figcaption>
</figure>

## User Interface Diagrams
#### Site Map
The following diagram illustrates the flow through web pages as users exercise the site.
<figure>
  <img src="/assets/images/DiversityCyberCouncil-SiteMap.jpeg" width="1000">
  <figcaption>Site Map Diagram</figcaption>
</figure>

#### Wireframes
The following diagram shows the simplified mockups of the web pages in the system. 
<figure>
  <img src="/assets/images/DiversityCyberCouncil-Wireframes.jpeg" width="1000">
  <figcaption>Wireframe Diagram</figcaption>
</figure>

#### Interactive Voice Response (IVR) Map
The following diagram shows the flow through menus for users connecting to the interactive voice response system. 
<figure>
  <img src="/assets/images/DiversityCyberCouncil-IVRMap.jpeg" width="1000">
  <figcaption>IVR Map Diagram</figcaption>
</figure>

## Workflow Diagrams
The following diagrams show the workflow used when candidate and non-profit users register with the system. Note that these workflows are triggered by events raised by the Graph Db.
<figure>
  <img src="/assets/images/DiversityCyberCouncil-WorkflowDiagram.png" width="800">
  <figcaption>Workflow Diagram</figcaption>
</figure>

## Data Diagram - Graph Model
The following diagram shows the nodes and connections that make up the Graph Db.
<figure>
  <img src="/assets/images/DiversityCyberCouncil-GraphModel.jpeg" width="1000">
  <figcaption>Graph Data Model Diagram</figcaption>
</figure>

## Data Analytics
Data analytics will be used to enhance the system value for participants in a number of ways, including:

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
<figure>
  <img src="/assets/images/DiversityCyberCouncil-SequenceDiagrams.jpeg" width="1000">
  <figcaption>Sequence Diagram</figcaption>
</figure>

## Deployment Diagram  
The following diagram shows the deployment location of components using AWS as a cloud provider. The model can easily be adapted to reflect other cloud providers (Microsoft Azure, Google Cloud Platform, etc.) if needed.
<figure>
  <img src="/assets/images/DiversityCyberCouncil-DeploymentDiagram.jpeg" width="1000">
</figure>

### Glossary for deployment elements
#### [AWS Simple Storage Service (S3)](https://aws.amazon.com/s3/)
Amazon S3 is an object storage service that offers high redundancy and availability of data. We will be using S3 to store the content for our Web Pages.

#### [AWS Lambda](https://aws.amazon.com/lambda/)
AWS Lambdas are serverless compute services often referred to as Functions as a Service. We will be using lambdas in our solution to provide the logic for the APIs that will talk between the GraphDB datastore, and our web interface.

#### [AWS Simple Workflow Service](https://docs.aws.amazon.com/swf/index.html)
AWS Simple Workflow Service is managed service that will allow us to easily create workflows for onboarding new candidates and connecting them with mentors.

#### [AWS Step Function](https://aws.amazon.com/step-functions/?step-functions.sort-by=item.additionalFields.postDateTime&step-functions.sort-order=desc)
AWS Step Functions are a visual, low code service for creating workflows. We will be using step functions to coordinate and execute Lambda functions that will handle mentor assignment.

#### [Amazon Simple Notification Service (SNS)](https://aws.amazon.com/sns/)
Amazon SNS is a managed notification service that enables communications through various mediums. We will use SNS to send email to Candidates and Non-Profit Organizations.

#### [AWS API Gateway](https://aws.amazon.com/api-gateway/)
API Gateway is a fully managed service used to maintain API endpoints for various types of protocols. Our solution will use API Gateway as the secured endpoint to communicate with and trigger lambda functions.

#### [AWS Cloudfront](https://aws.amazon.com/cloudfront/)
Amazon Cloudfront is a content delivery network service that is used for optimizing delivery of web content globally no matter where the web server is running. We will be using Cloudfront to be the front end for our Single Page Application website for the Spotlight platform.

#### [Amazon Elastic Kubernetes Service (EKS)](https://aws.amazon.com/eks/)
Amazon EKS is a managed container service used to run and scale Kubernetes applications in the cloud or on-premises.

#### [Amazon Cognito](https://aws.amazon.com/cognito/)
Amazon Cognito is a service used to manage authentication of users and includes built-in support for social identity providers like Facebook, Google, Apple and Amazon.

#### [Amazon Connect](https://aws.amazon.com/connect/?nc2=h_ql_prod_ce_con)
Amazon Connect is a managed service used to provide a full omnichannel cloud contact center

#### [Containerized Graph Database](#)
This is a database that meetts the GraphQL specification. There are many options for this, but based on team experience we would recommend [Neo4j](https://neo4j.com/) based on it’s maturity as a product.

#### [Marketo](https://www.marketo.com/)
Marketo is a marketing automation platform used to simplify marketing communications with potential customers.

## Test Plan
### Purpose
This section describes the plan for testing the Spotlight system. It will:
  - Identify the test requirements at a high level
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
### Test Deliverables
  - Test Plan
  - Test Suite
  - Test Data Sets
  - Test Scripts
  - Test Results and Evaluation


### Glossary
#### Administrator
  An employee of the Diversity Council who manages administrative tasks such as approving new non-profit service providers.
#### Back End for Front End
  Back end for front end is a microservices pattern that breaks away from monolithic systems that utilize a single API for all clients and breaks them up into specific client type API's that provide just the services needed for the consuming client.
#### Candidate
  Users who wish to utilize the services provided by one of the Diversity Council's non-profit organizations.
#### Content Delivery Network (CDN)
  A geographically distributed group of servers that work together to provide fast delivery of Internet content. A CDN provides faster access and delivery of content over the internet by placing the content closer to the users.
#### Email Service
  A system that handles the generation and delivery on email messages to clients at scale.
#### Graph Database
  Graph databases are purpose-built to store and navigate relationships. Relationships are first-class citizens in graph databases, and most of the value of graph databases is derived from these relationships. Graph databases use nodes to store data entities, and edges to store relationships between entities. An edge always has a start node, end node, type, and direction, and an edge can describe parent-child relationships, actions, ownership, and the like.
#### Interactive Voice Recognition (IVR)
  An automated telephony system that interacts with callers, gathers information and routes calls to the appropriate recipients and services.
#### IVR Server
  Server based software system for providing Interactive Voice Recognition services, such as AWS Connect.
#### Microservices
  An architecture design for building a distributed application using containers. Each service of the system is independent. 
#### NPO
  Non-Profit Organization that provides services or can apply to provides services through the Diversity Councils website.
#### Offerings
  Services provided by the registered non-profits of the Diversity Council.
#### Provider
  A registered NPO that is providing services to the Diversity Council's clients.
#### Static Content
  Static content is any file stored on a server that is the same every time it is delivered to users. The system utilizes AWS S3 (Simple Storage Service) for storing all static content.
#### Step Functions
  A step function is a series of serverless lambda functions executed in a specific order to perform a given set of tasks.
#### Workflow Engine
  A software application that manages business process. 
