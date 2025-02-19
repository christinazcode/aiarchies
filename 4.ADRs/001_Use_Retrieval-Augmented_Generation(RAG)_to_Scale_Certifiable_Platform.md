## Title: 

001: Use Retrieval-Augmented Generation (RAG) to Scale Certifiable Platform

## Status: 

Accepted

## Context:

Certifiable Platform supports 200 candidates per week.  The user base is projected to grow five to ten times with international expansion and 21% annual growth over the next four years. Maintaining the accuracy of the certification process is critical.  The two options for scaling the platform are using RAG/GenAI to automate some manual processes and expanding the current team of 300 expert software architect consultants.

## Decision:

We will use RAG/GenAI.

RAG/GenAI can be implemented to summarize short answers and architecture design submissions, generate feedback for both Test 1 and Test 2, verify the integrity of the submissions, brainstorm ideas for modifying tests and changing/adding design cases, and even provide a private chat assistant to answer relevant questions. A consultant spends 11 hours grading a candidate's submission and writing feedback. With RAG/GenAI automation and assistance, this effort can be reasonably reduced to less than two hours.  It can provide reasonable accuracy compared to expanding the team to 3,000 or more. 


## Consequences:

The ethical implications of GenAI development and deployment include bias mitigation, fairness, transparency, and responsible AI practices. We need to adjust the current workflow to ensure all test changes/additions are reviewed by the five designated subject matter experts and all submission summaries and feedback are reviewed by the 300 consultants. Appropriate evaluation, guardrails, and observability should be part of the design.