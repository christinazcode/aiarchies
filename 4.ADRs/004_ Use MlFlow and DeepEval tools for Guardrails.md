## Title: 

003: Technology for guardrails and validations for AI prompt invocation and results. 

## Status: 

Proposed

## Context:

- The system needs to ensure that prompts submitted to Prompt Orchestrator from Auto Grader Service are within the boundaries of architecture-concerned topics
- The system needs to ensure that the results produced by the AI-enhanced search Engine are accurate and consumable by human evaluators.

## Decision:

- Use MlFlow and DeepEval tools for screening of Auto Grader search prompts and returned results.

The MlFlow and DeepEval provide superior features, maturity, support infrastructure, and a low-cost option: Open Source.
 
## Consequences:

- Product ownership and operational cost.
- Implementation installation, configuration, and integration.
- Run time  availability, process flow observability, and connectivity.
- Maintainability and tuning
