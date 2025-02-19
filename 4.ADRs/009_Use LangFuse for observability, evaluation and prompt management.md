# Architecture Decision Record: Use of Langfuse for AI observability

## Status

Accepted

## Context

Observability need to be integrated into our architecture from the beginning rather than added later as an afterthought, so that Architecture can be evolved using metrics and other insights from AI system. Observability is crucial for projects of all sizes, and its importance grows with the complexity of the system.

We need a observability tool where we can asess our Architceture looking at costs, efficienicy, latency  of the system and continiuosly evolve our architecture.

The Observality tool need to be hosted in a in-house envioronment and need to  work with different AI models and frameworks seamlessly.

## Decision

We will use Langfuse  as our Observality solution in AI Pipeline.

## Rationale

### Performance \& Scalability

- Real time Observavility to detect Performance bottlenecks.
- Analyses Token consumtion and API costs.
- Sclaes for Productions workloads in AI driven applications.
- Supports both self hosted and cloud envioroments.

### Technical Features

- LANGFuse SDK supports Pyhton, Java Script, Open AI and other popular langauage sources and frameworks.
- Stores logs for training and Re tuning the models.
- Tracks errors like hallucinations, API failures and incorrect responses.



### Integration Capabilities

- Seamlessly integrates with embedding models.
- Integartes with RAG architecture.
-Integartes with different embedding models seamlessly.

## Alternatives Considered

1. **Langsmith**: While simpler to implement, it does not have cost tracking.
also performance monitoring is limited.
2. **Helicone**: Helicone is similar to Langfuse, but only cloud hosted and performance monitoring is limited.
3. **Datadog**: General application observability platform for infrastructure, logs, APM (Application Performance Monitoring), and security.not specialized for LLM applications. No Cost tracking.


## **Conclusion**

Langfuse provides the right fit of certifiable business goals of scability and high peformance. Langfuse can monitor cost and performance of the system and will give insights of re tuning the LLM models. 

## References

- Hugging space spaces  for Langfuse, Langsmith
- Helicone GitHub repository
- Datadog GitHub repository



