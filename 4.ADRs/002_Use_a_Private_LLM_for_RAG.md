## Title: 

002: Use a Private LLM for RAG

## Status: 

Accepted

## Context:

With Retrieval Augmented Generation (RAG), information about aptitude tests and case study tests is stored in a vector database. For a given prompt, the database is queried, relevant documents are retrieved, and the prompt is augmented with the content of those documents, thereby providing richer context to the LLM.  The two choices for LLM access are a private LLM accessed through an API and public platform LLM APIs.

## Decision:

We will use a private LLM.

Data privacy and security are crucial for our business. With a private LLM, our test data remains under our control.  Ownership gives us full control over the model's selection, deployment, and usage.

## Consequences:

We need to manage observability, prompt engineering, and model evaluation for the private LLM. When a better version of the LLM becomes available, we can swap the existing LLM with the newer version while keeping the remaining architectural components unchanged.