## Title: 

003: Technology for Self-Hosted LLM

## Status: 

Accepted

## Context:

- The recommendation system needs an LLM model for baseline processing
- Requirements considerations are cost, reliability, accuracy, and performance
- Select something that works with Sage Maker used for hosting of our RAG system.

## Decision:

- We will use the **GTP NeoX** tool for self-hosted LLM capabilities.

If the primary concern is minimizing costs, and we have the technical capability to handle setup and maintenance, GPT-NeoX is a strong choice.  
GPT-NeoXT-Chat-Base-20B language foundation model is available for customers using Amazon SageMaker JumpStart.
 
## Consequences:

- Managing product instance ownership and cost.
- Implementation installation, configuration, and integration.
- Support of run time process flow exceptions and connectivity.
- On-going maintainance and model tuning
