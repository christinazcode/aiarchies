## Baseline Use Cases

### UC01: User registers

- Architect Certification Candidate: A User registers via Web Application 
- User registers via invitation link sent in a marketing email

Once a user registers in the system, the user is called a Candidate

### UC02: Candidate Makes a Payment

A Candidate makes a payment via online payment systems.

### UC03: Candidate Takes an Aptitude Test

**Pre-Cond:** Once a Candidate makes a payment they are eligible to take the aptitude test.

- A Candidate provides answers to Multiple-Choice questions.
- A Candidate provides answers to Short-Answer questions.

### UC04: Candidate Takes an Architecture Solution Test

**Pre-Cond:** Once a Candidate scores 80% on the Aptitude Test they are eligible for the Architecture Solution test.

- A Candidate obtains details of the Case Study.
- A Candidate provides a document answering the Case Study challenge.

### UC05: Expert Reviews and Approves the Short Answers from the Aptitude Test

**Pre-Cond:** The short answers is ranked by the AI Auto Grader application

- An Expert opens the next item in the manual review queue and confirms or adjusts the recommendation ranking score

### UC06: Expert Reviews and Approves the Candidate Response from the Solution Architecture Test

**Pre-Cond:** The case study submission is ranked by the AI Auto Grader application

- An Expert opens the next item in the manual review queue and confirms or adjusts the recommendation ranking score

### UC07: Candidate views the status or results of the tests

**Pre-Cond:** The Candidate is registered and submitted and Aptitude or Solution Architecture test for grading

- A Candidate user reviews the record of testing progress and test scores

### UC08: An Administrator Maintains Users
- An administrator manages all expert credentials
- An administrator manages candidate user profiles

### UC09: An Expert Maintains Questions and Answers



