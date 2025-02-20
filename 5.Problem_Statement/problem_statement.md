# Problem Background
## Company Overview and Requirements Context

### Fictional historical perspective
- IT professions and architects must be licensed like doctors
- SALB - Software Architecture Licensing board, administers software architect licensing
- Laws passed in UK, Europe and Asia to match the US laws
- Certifiable Inc - a market leader in admistering certification tests 
  - Product name - SoftArchCert	

### Certification Process
- Two tests
    - Aptitude test
        - Mutiple choice and short answer questions
        - Answers stored in the database
        - Multiple choice questions are autograded
        - Short answers are graded by expert software architects within 1 week of submission
        - Passing score required is 80% or more
        - Candidates are notified why they did not pass, if they fail
        - Candidates are notified if they pass to move on the second test
        - 3 hrs spent on the short answers review.
		
    - Architecture submission
        - Create an architecture for a case study
        - One of five case studies is randomly assigned for an architecture solution
        - Two weeks given to upload the architectural solution
            - Distinct criteria used to grade the architectural solution manually by the expert software architects within 1 week of submission
        - Passing grade required is 80% or more
        - Failure to score 80%, candidates can reapply for the architectural submission portion of the test
        - 8 hrs spent on the architecure submission review by the experts

- Candidate have 30 days from the first test to start their second test.
- Certification info is saved in a verification database for candidates scoring 80% in both exams
	
### Administrative Process
- Experts grade tests, but analyse reports and results to modify certification test questions
- New tech patterns, practices are incorporated in the questions periodically
- Case studies are periodically added and replaced for the second portion of the test
- Experts are contractors that work hourly with varying demand
- Administrator maintains the expert architect credentials in the system
- There is a UI to View certification results for candidates, employers and HR

### Current Infrastructure and Demand
- Company currently employees 300 experts. 5 of these are designated experts who can modify tests, earning $50 per hr.
- 200 candidates per week 
- Expected to grow 5-10x with overseas expansion
- anticipated growth 21% over the next 4 years
- Licensing fee $800
- 120K software architects certified by Certifiable Inc. right now.
- Certifiable has a 80% market share
- Certifiable is willing to spend the money to incorporate AI solutions due to expected growth

### Growth Projections
  - Expected increase in volume - 5-10x to certify and license architects
  - Apply Generative AI to assist with the manual processes to keep up with the demand
  - Identify opportunities to use AI and redesign the architecture to hande the surge in demand

    #### Real stats
    - 176K software architects in the US
    - 300K job openings yet to be filled
    - 600K job openings in UK, Asia and Europe
    - 21% growth expected over the next 4 years

## Requirements

- The company wants to see how generative AI could be used to help with anticipated growth of 5-10 times due to EU market expansion and 21% due to YoY growth

## Opportunities -
- By deploying an AI based solution - Reduce Experts intervention in improving and maintaining aptitude test questions.
- By deploying an AI based solution - Reduce experts intervention in updating the case studies options for the architecture submission part of the test. 
- Pre-screen short answers with the help of AI to reduce time spent by experts in the manual review. Currently 3 hours per test.
- Pre-screen architecture submissions with the help of AI to reduce time spent by experts in the manual review. Currently 8 hours per test.
- Reduce turn around time for test results - currently over 30 + 21 or 51 days combined for the two tests.

## Constraints -
 
- The gross profit margin before infrastructure costs is $800 - $550 ($50 X 11 expert hrs) = $250.
- The growth projections and the additional AI system costs must improve the profit margin not reduce it.
- Maintain data security by securely saving all data on corporate managed, isolated systems (not exposed to public cloud infrastructure).

## Goals

- Learn How to apply AI
- Learn the tools and Catagories of the AI ecosystem
- Learn AI architectural patterns and how to apply them
- Understand limitations and risks associated with AI in architecture
- Undertsand how AI impacts the structure of a system