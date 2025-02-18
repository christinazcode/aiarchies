<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" class="logo" width="120"/>

# what is the preferred self hosted vector database for a self hosted embedding model for a self hosted gpt-neox rag system for a small or medium enterprise where cost per use is to be minimized compared to performance

---
For a small or medium enterprise (SME) aiming to minimize cost per use in a self-hosted GPT-NeoX RAG system, several open-source vector databases stand out[^1][^2][^5][^6][^9]. These options provide a balance of performance and cost-effectiveness.

Here are the recommended choices:

1. **Milvus**:
    * **Strengths**: Designed for AI applications and similarity searches[^1]. It is a powerful open-source vector database[^1].
    * **Cost Efficiency**: It's free to use and self-host, which reduces operational costs[^1][^2].
2. **Weaviate**:
    * **Strengths**: Combines vector search with structured filtering, allowing complex queries[^2]. It is cloud-native and open-source[^11].
    * **Cost Efficiency**: Open-source and self-hostable, thereby minimizing costs[^2].
3. **Qdrant**:
    * **Strengths**: Written in Rust, it is a fast and scalable vector similarity search service. Supports advanced filtering and payload management[^2][^14].
    * **Cost Efficiency**: As a free and open-source solution, it reduces operational expenses[^2].
4. **PostgreSQL with pgvector**:
    * **Strengths**: It leverages the robustness of PostgreSQL and adds vector capabilities[^4].
    * **Cost Efficiency**: It is free to use and integrates well with existing PostgreSQL infrastructure[^4].

When evaluating open-source vector databases, it's important to consider the hardware costs associated with running them[^10]. Setting up a distributed database like Milvus involves WAL deployment, secure metadata storage, and orchestration with Kubernetes, which can impact the hardware budget, especially for smaller projects[^10]. Performance tests are crucial to understanding how the database handles real-life workloads[^10].

Ultimately, the decision should be based on a clear comparison of the costs involved in handling specific data volumes and query rates to determine the most cost-effective option[^10]. Using dynamic scaling can help avoid paying for unused resources, but it's important to balance this with the potential for under-provisioning[^10].

Considering these factors, Milvus, Weaviate, Qdrant, and PostgreSQL with pgvector are excellent choices for SMEs looking to minimize costs in a self-hosted GPT-NeoX RAG system[^2][^5][^9].

<div style="text-align: center">⁂</div>

[^1]: https://www.amax.com/top-5-open-source-vector-databases-for-scalable-ai-solutions/

[^2]: https://www.sabrepc.com/blog/deep-learning-ai/top-open-source-vector-databases

[^3]: https://www.shakudo.io/blog/top-9-vector-databases

[^4]: https://www.reddit.com/r/dataengineering/comments/1gi26mq/cheapest_hosting_options_for_rag_setup_with/

[^5]: https://www.reddit.com/r/vectordatabase/comments/1hzovpy/best_vector_database_for_rag/

[^6]: https://research.aimultiple.com/open-source-vector-databases/

[^7]: https://www.digitalocean.com/community/conceptual-articles/how-to-choose-the-right-vector-database

[^8]: https://www.timescale.com/blog/finding-the-best-open-source-embedding-model-for-rag

[^9]: https://celerdata.com/glossary/best-vector-databases

[^10]: https://zilliz.com/blog/cost-of-open-source-vector-databases-an-engineer-guide

[^11]: https://lakefs.io/blog/12-vector-databases-2023/

[^12]: https://slashdot.org/software/vector-databases/f-small-business/?page=2

[^13]: https://myscale.com/blog/what-to-expect-rag/

[^14]: https://community.openai.com/t/best-vector-database-to-use-with-rag/615350

[^15]: https://www.peerspot.com/categories/vector-databases

[^16]: https://www.aimon.ai/posts/comparison-of-vector-databases-for-retrieval-augmented-generation-rag-systems

[^17]: https://community.openai.com/t/what-is-the-best-database-for-retrieval-augmented-generation-rag/718536

[^18]: https://www.thebusinessresearchcompany.com/report/vector-database-global-market-report

[^19]: https://www.linkedin.com/posts/geetakakrani_chatbot-genrativeai-ai-activity-7277225484210311168-XwO7

[^20]: https://www.langchain.ca/blog/top-5-open-source-vector-databases-2024/

