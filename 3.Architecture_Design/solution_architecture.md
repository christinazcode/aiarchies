## Architecture Principles
A few core architecture principles to make sure that our architecture and system design align with strategic business objectives and existing systems' qualities.  [Placeholder]

| Principle              | Description                    |
| ---------------------- | ------------------------------ |
| Reuse over Buy over Build | We prefer to use existing solutions if they provide the necessary support to address business needs. Otherwise, we look first at vendor or open-source alternatives before developing custom software ourselves. 
| Separation of Concerns | Divide the components of the system into specific features so that there is no overlapping among the components' functionality. This will provide high cohesion and low coupling. This approach avoids the interdependency among components of the system which helps in maintaining the system easy.
| Cloud over Self Hosted | We minimize the dependencies on hardware resources and cost while increasing agility and efficiencies by leveraging SaaS, PaaS, and IaaS hosting platforms over owned data center hosting.

## Architecture Guidelines

Software Architecture shall have a data pipeline to have continous update of  test questions and answers database for RAG systems. 

Software Architecture shall need to have prompt geneartion tightly coupled to vector database for up to date and relevant prompt generation

software architecture shall ensure that Architecture is designed in such a way not to load LLM for repeated queries to control costs.

software architecure shall need to have a monitoring system for costs incurred with LLM usage(Token usage etc.)

Software architecture shall need to have a guideline for prompt responses back from LLM.

Software architecture shall need to have a process of filtering/guradrailing  user responses to LLM.

Software architecture shall have a way  of structured response generation from LLM as per user need.

Software Architecture shall have a way of automtically quering the vector database without any human assistance like an agentic AI system.

Software Architecture shall have a way of evaluating the models used in AI assisted grading system.

## Architecture Component Model
The system architecture consists of five subsystems responsible for Administration, Running the Tests, Assessment and Scoring, Learning and Recommendation as well as Candidate Status.  The existing system will be extended with an RAG approach to enhance large language models (LLMs) through query-dependent retrievals based on the architectural test relevant context.

![image](assets/High%20Level%20System%20Context%20Diagram.png)

## Main Architectural Quanta and Qualities
- User and Test Administration Sub-System
  - Availability
  - Security
  - Performance
- Testing System
  - Availability
  - Scalability
  - Performance
- Learning and Recommendation System
  - Accuracy
  - Reliability
- Candidate Status and Certification System
  - Scalability
  - Security

## User and Test Administration Architecture
The Administration architecture will be modified by adding AI model training functions allowing designated expert users to introduce "best" answers to the RAG model and case study context with "preferred" solutions.  The new user interface functions and integration into the AI data Pipeline will be added to the current administration application subsystem.

![image](assets/Administration%20System%20Architecture.png)

## Testing System Architecture 
The existing Testing subsystem will be enhanced by integrating AutoGrader service components to provide grading summaries and recommendations for the Expert users to review, adjust, and approve the final test grades.
Aptitude Test Subsystem Components and Integrations
![image](assets/Test%201%20Subsystem.png)

Architecture Solution (Case Study) Testing Subsystem Components and Integrations
![image](assets/Test%202%20Subsystem.png)

## Learning and Recommendation System Architecture 
The new Learning and Recommendation System will be created and integrated into the other sub-systems for summarization and grading of Candidate answer submissions, as well as for context learning and fine-tuning purposes.  

![image](assets/Autograder%20and%20Data%20Pipeline.png)

