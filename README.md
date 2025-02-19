# **AI Archies Team's - Augmenting Human Intelligence for Certifiable, Inc. (Architectural Kata Winter 2025)**

### Welcome to the Augmenting Human Intelligence for Certifiable repository!

In a world where software architects must be licensed professionals in the same way doctors, nurses, building architects, and lawyers are licensed, Certifiable, Inc. is the market leader in certifying and licensing new and existing software architects.  Facing the opportunity for growth, it utilizes generative AI to augment human intelligence so that AI is not replacing humans, but becoming their assistance. This provides a great example of how to use responsible AI to build a better world.

## **Table of Contents**

- [Overview](#overview)
  - [About the Project](#about-the-project)
  - [Team Members](#team-members)
- [Requirements](#requirements)
  - [Functional Requirements](#functional-requirements)
  - [Architectural Characteristics](#architectural-characteristics)
  - [Assumptions and Constraints](#assumptions-and-constraints)
- [Appendix](#appendix)
  - [Kata Goals](#kata-goals)
  - [Judging Criteria](#judging-criteria)
  - [Deliverables](#deliverables)

## **Overview**

### **About the Project**

Our **Augmenting Human Intelligence solution** effectively and reliably automates key manual steps in the company's certification process. It enables:

- **Brainstorming** ideas for both aptitude tests and architecture solution tests
- **Summarizing** short answers in aptitude tests and architecture submissions in architecture solution tests
- **Generating** architecture submission feedback
- **Plagiarism detection**, including AI content detection
- Keeping **humans in the loop** to review and validate all generated content and perform the final scoring

### **Team members**

* [Abhishek Bansal](https://www.linkedin.com/in/bansala/)
* [Jerzy Bilchuk](https://www.linkedin.com/in/jerzybilchuk/)
* [Preeti Gupta](https://www.linkedin.com/in/pep/)
* [Somenath Mukherjee](https://www.linkedin.com/in/somenathmukherjee/)
* [Christina Zhong](https://www.linkedin.com/in/zhongchristina/)

## **Requirements** 

### Functional Requirements
[View Functional Requirements](1.Requirements/01_Functional_Requirements.md)  
Defines core features such as Ema, the agent, plagiarism detection, and feedback generation.

### Architectural Characteristics
[View Architectural Characteristics](1.Requirements/02_Architectural_Characteristics.md)  
Outlines accuracy, security, and observability requirements.

### Assumptions and Constraints
[View Assumptions and Constraints](1.Requirements/03_Assumption_and_Constraints.md)  
Details the assumptions and system limitations.

## **Use Cases**

[View Use Cases](2.Features/Use_Cases.md)

Lists some use cases.

## **Architecture and Design**

## **Architecture Decision Records (ADRs)** 

Capture every aspect of the architectural decisions made in designing the system.

### ADRs List

[001: Use Retrieval-Augmented Generation (RAG) to Scale Certifiable Platform](4.ADRs/001_Use_Retrieval-Augmented_Generation(RAG)_to_Scale_Certifiable_Platform.md)
 

## **Appendix**

### Kata Goals

- Analyse the existing system's architecture to **identify manual steps and likely bottlenecks** 
- Determine how GenAI could address **the growth in demand and potential scalability problems** 
- Select opportunities for adding AI to the existing system and **how** it can be applied
- **Redesign the existing** architecture to support these changes
  
### Judging Criteria

1. Innovative use of GenAI
2. Suitability of solution given the constraints
3. Provide an appropriate level of details
4. Use of AI architecture patterns and avoidance of AI architecture anti-patterns 
5. Match the current solution's architectural characteristics (a.k.a qualities, non-functional requirements) in the AI additions

### Deliverables: 
- AI perspective of the solution: how the team used AI, what data and UIs are required to implement the certification solution 
- More details in the diagrams
- ADRs of AI implementation; including trade-off analysis and consequences
- [optional] pertinent implementation details
- [semi-finalists] five minutes videos describing

Important use cases visualized on sequence diagrams
Deployment
Fitness functions
Constraints Known issues
Observability
