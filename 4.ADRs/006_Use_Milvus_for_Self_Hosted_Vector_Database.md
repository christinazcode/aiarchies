## Title

006: Technology for Self-Hosted Vector Database

## Status

Accepted

## Context

We need a vector database solution that integrates with our self-hosted AI infrastructure, which includes the GPT-NeoX LLM, the All-MiniLM-L6-v2 embedding model, and various MLOps tools.

## Decision

We will use Milvus (Milvas) as our self-hosted vector database solution.

## Rationale

### Performance \& Scalability

- Delivers high-performance vector search, operating up to 10x faster than vector search plugins[^2]
- Scales horizontally to handle billions of vectors with minimal performance loss[^13]
- Supports both in-memory and on-disk index types for flexible resource management[^7]


### Technical Features

- Provides flexible deployment options from single-machine to distributed setups[^13]
- Offers multiple index types including HNSW and DiskANN[^7]
- Supports real-time updates and maintains data freshness[^7]
- Enables efficient metadata filtering and high query throughput[^7]


### Integration Capabilities

- Seamlessly integrates with embedding models[^6]
- Compatible with modern AI development tools and frameworks[^13]
- Supports both CPU and GPU optimization[^18]


### Cost Analysis

Total annual cost of ownership for the complete stack: \$8,000, broken down as:

- Milvas: \$1,000
- GPT-Neox LLM: \$2,000
- All-MiniLM-L6-v2: \$500
- Langfuse: \$1,500
- BM25: \$800
- MLflow: \$1,200
- DeepEval: \$1,000


## Consequences

### Positive

- Enterprise-grade scalability and reliability[^18]
- Comprehensive feature set for AI applications[^13]
- Active community support with over 33,000 GitHub stars[^18]
- High-performance vector similarity searches for efficient information retrieval
- Flexibility in deployment options to match our current and future needs
- Strong integration with AI ecosystem tools and libraries
- Potential for GPU acceleration to enhance overall system performance

### Negative

- Requires operational expertise for distributed deployment
- Initial setup complexity for integration with multiple components

### Risks

- Ensuring proper configuration and optimization of Milvus for our specific use case
- Managing resource requirements, especially in distributed deployments

## Alternatives Considered

1. **pgvector**: While simpler to implement, it may face scalability challenges with extremely large datasets[^21].
2. **Faiss**: Another popular vector database, but Milvus outperforms it by 30%-70% in many scenarios[^20].
3. **Redis**: Limited scalability for vectors (>1B) and higher latency in hybrid queries[^22][^11].
4. **Pinecone**: Managed service costs (~\$70k/year for similar scale) and lack of control over data governance[^23][^13].

## **Conclusion**

Milvus provides the optimal balance of speed, scalability, and cost for a self-hosted AI stack, enabling full data control and customization. Combined with GPT-NeoX and guardrails, this architecture supports enterprise-scale generative AI applications while avoiding vendor dependencies[^1],[^11],[^13].

## References

- Milvus documentation and benchmarks
- GPT-NeoX GitHub repository
- all-MiniLM-L6-v2 model documentation
- Langfuse documentation

## Implementation Notes

The system will be deployed as a distributed setup to ensure scalability and reliability, with integration points to all other self-hosted components in our AI stack.

<div style="text-align: center">⁂</div>

[^1]: https://milvus.io/docs/overview.md

[^2]: https://milvus.io/blog/why-and-when-you-need-a-purpose-built-vector-database.md

[^3]: https://www.tessell.com/blogs/what-is-milvus

[^4]: https://github.com/EleutherAI/gpt-neox

[^5]: https://www.youtube.com/watch?v=M1LkGpFI5SQ

[^6]: https://milvus.io/blog/introducing-pymilvus-integrations-with-embedding-models.md

[^7]: https://www.reddit.com/r/vectordatabase/comments/1gltrx6/i_found_milvus_to_be_the_fastest_opensource/

[^8]: https://360digitmg.com/blog/milvus-tutorial-step-by-step-guide

[^9]: https://milvus.io/use-cases

[^10]: https://www.comet.com/docs/v2/integrations/third-party-tools/gpt-neox/

[^11]: https://airbyte.com/data-engineering-resources/integrating-vector-databases-with-llm

[^12]: https://milvus.io/docs/embeddings.md

[^13]: https://milvus.io

[^14]: https://zilliz.com/blog/harnessing-vector-databases-to-empower-autogpt

[^15]: https://dev.to/simplr_sh/milvus-your-vector-database-powerhouse-a-deep-dive-2d6h

[^16]: https://www.reddit.com/r/LocalLLaMA/comments/1e63m16/vector_database_pgvector_vs_milvus_vs_weaviate/

[^17]: https://milvus.io/intro

[^18]: https://zilliz.com/what-is-milvus

[^19]: https://www.ibm.com/think/topics/milvus

[^20]: https://milvus.io/docs/overview.md

[^21]: https://myscale.com/blog/pgvector-vs-milvus-choosing-right-vector-database/

[^22]: https://myscale.com/blog/milvus-vs-redis-vector-database-benchmarks/


