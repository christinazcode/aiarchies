## Title

008: Selecting BM25 as the Initial Ranking Model for a Self-Hosted RAG System

## Status
Accepted

## **Context**

The proposed Retrieval-Augmented Generation (RAG) system integrates the following components:

- **Embedding model**: `all-MiniLM-L6-v2` for semantic vectorization.
- **LLM**: A self-hosted GPT-NeoX model for text generation.
- **Vector database**: Milvus for storing and retrieving embeddings.
- **Observability**: Langfuse for monitoring and analytics.
- **Guardrails**: MLflow and DeepEval for ensuring quality and reliability.

The system aims to balance cost-efficiency, scalability, and performance while supporting domain-specific queries. The choice of an initial ranking model is critical to ensure effective document retrieval, as it directly influences the quality of the LLM's outputs.

## **Decision**

BM25 (Best Matching 25) is selected as the initial ranking model for the RAG system.

## **Rationale**

1. **Advantages of BM25**:
    - **Efficiency and Simplicity**: BM25 is computationally lightweight compared to dense vector-based retrieval methods, making it suitable for self-hosted systems with limited resources[^1][^9].
    - **Term-based Retrieval**: It excels at handling keyword-based queries, especially when exact matches or term importance (e.g., frequency) are crucial[^2][^10].
    - **Document Length Normalization**: BM25 adjusts scores based on document length, reducing bias toward longer documents[^1][^10].
    - **Interpretability**: BM25's scoring mechanism is straightforward, making it easier to debug and optimize compared to opaque neural models[^1][^9].
    - **Cost Efficiency**: Unlike embedding-based retrieval, BM25 does not require pre-computed embeddings or GPU acceleration, reducing operational costs[^9][^10].
2. **Complementarity with Vector Search**:
    - While BM25 focuses on term frequency and inverse document frequency, the embedding model (`all-MiniLM-L6-v2`) provides semantic understanding. This hybrid approach ensures both lexical precision and semantic relevance in retrieval[^9][^12].
3. **Performance in RAG Systems**:
    - Studies show that combining BM25 with LLMs in RAG pipelines improves response accuracy by leveraging BM25's ability to retrieve contextually relevant documents[^7][^9]. For example, BM25 can effectively handle rare or domain-specific terms that embeddings might overlook[^1][^10].
4. **Cost Considerations**:
    - Self-hosting a GPT-NeoX model and Milvus database incurs significant GPU and storage costs. Using BM25 reduces the need for frequent embedding updates and high-dimensional vector searches, lowering overall system expenses[^3][^4].
    - Estimated annual costs include:
        - GPU server for GPT-NeoX: ~\$17,520 (e.g., \$2/hour for H100 GPUs running ~50% of the time)[^4].
        - Milvus database hosting: ~\$24,000 (assuming 40 million vectors with 2 replicas)[^3].
        - Langfuse observability: ~\$5,000 annually.
        - Total estimated cost: ~\$46,520/year.
5. **Limitations of BM25**:
    - BM25 lacks semantic understanding and personalization capabilities. However, these limitations are mitigated by combining it with `all-MiniLM-L6-v2` embeddings for deeper semantic matching when needed[^10].

## **Summary of Results Across LLM Engines**

- RAG systems using open-source models like GPT-NeoX achieve competitive performance compared to proprietary models like GPT-4 when paired with retrieval mechanisms like BM25. For instance:
    - RAG improved response accuracy by up to 35% in search scenarios compared to standalone LLMs[^7][^13].
    - Open-source LLMs combined with RAG pipelines achieved similar "faithfulness" scores as GPT-4 at a fraction of the cost[^7].


## **Consequences**

- The system will initially rely on BM25 for efficient term-based retrieval. As the system scales or requires more advanced capabilities (e.g., personalization), hybrid search techniques combining BM25 with vector-based methods can be explored.
- This decision supports cost-effective scaling while maintaining high-quality responses in domain-specific applications.


## **Conclusion**

BM25 is an optimal choice as the initial ranking model due to its efficiency, interpretability, and cost-effectiveness. It complements the embedding-based retrieval provided by `all-MiniLM-L6-v2`, ensuring a robust foundation for the self-hosted RAG system.

<div style="text-align: center">⁂</div>

[^1]: https://aiengineering.academy/RAG/01_BM25_RAG/notebook/

[^2]: https://training.continuumlabs.ai/disruption/search/bm25-search-engine-ranking-function

[^3]: https://myscale.com/blog/what-to-expect-rag/

[^4]: https://www.e2enetworks.com/blog/why-self-hosting-small-llms-are-cheaper-than-gpt-4-a-breakdown

[^5]: https://www.willowtreeapps.com/craft/retrieval-augmented-generation

[^6]: https://www.promptingguide.ai/research/rag

[^7]: https://www.pinecone.io/blog/rag-study/

[^8]: https://dev.to/vectorpodcast/7-ai-open-source-libraries-to-build-rag-agents-ai-search-27bm?bb=192032

[^9]: https://adasci.org/understanding-okapi-bm25-a-guide-to-modern-information-retrieval/

[^10]: https://www.confidentialmind.com/post/okapi-bm25

[^11]: https://langfuse.com/docs/model-usage-and-cost

[^12]: https://rahullokurte.com/overview-of-rag

[^13]: https://www.pingcap.com/article/how-rag-and-fine-tuning-enhance-llm-performance-case-studies/

[^14]: https://www.reddit.com/r/selfhosted/comments/1dsyfs2/introducing_r2r_a_fully_open_source_rag_engine/

[^15]: https://towardsdatascience.com/retrieval-augmented-generation-rag-inference-engines-with-langchain-on-cpus-d5d55f398502/

[^16]: https://en.wikipedia.org/wiki/Okapi_BM25

[^17]: https://news.ycombinator.com/item?id=42190650

[^18]: https://ai.plainenglish.io/bm25-distilled-unraveling-the-essence-of-a-robust-ranking-function-5a0a6393c058

[^19]: https://pub.aimind.so/understanding-the-bm25-ranking-algorithm-19f6d45c6ce

[^20]: https://docs.llamaindex.ai/en/stable/examples/retrievers/bm25_retriever/

[^21]: https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/LearningBM25MSRTechReport.pdf

[^22]: https://www.elastic.co/blog/practical-bm25-part-2-the-bm25-algorithm-and-its-variables

[^23]: https://www.fuzzylabs.ai/blog-post/improving-rag-performance-hybrid-search

[^24]: https://datascience.stackexchange.com/questions/75839/using-bm25-to-rank-words

[^25]: https://learn.microsoft.com/en-us/azure/search/index-ranking-similarity

[^26]: https://python.langchain.com/docs/integrations/retrievers/bm25/

[^27]: https://kmwllc.com/index.php/2020/03/20/understanding-tf-idf-and-bm-25/

[^28]: https://www.tensorops.ai/post/understanding-the-cost-of-large-language-models-llms

[^29]: https://www.reddit.com/r/Rag/comments/1h2iitk/what_is_a_range_of_costs_for_a_rag_project/

[^30]: https://blog.stackademic.com/rag-systems-made-easy-a-step-by-step-cost-and-implementation-guide-1213f908f590

[^31]: https://raga.ai/blogs/self-hosted-llm

[^32]: https://www.youtube.com/watch?v=WpkVmfTzyJg

[^33]: https://arxiv.org/html/2407.11638v1

[^34]: https://www.iguazio.com/blog/commercial-vs-self-hosted-llms/

[^35]: https://langfuse.com/self-hosting/infrastructure/llm-api

[^36]: https://pub.towardsai.net/a-taxonomy-of-retrieval-augmented-generation-a39eb2c4e2ab

[^37]: https://www.reddit.com/r/LangChain/comments/1benf40/rag_is_too_slow_with_100k_pdfs_what_do_you/

[^38]: https://mlflow.org/docs/latest/llms/rag/notebooks/question-generation-retrieval-evaluation.html

[^39]: https://sirocco.ai/retrieval-augmented-generation

[^40]: https://www.databricks.com/blog/long-context-rag-performance-llms

[^41]: https://weaviate.io/blog/rag-evaluation

[^42]: https://addepto.com/blog/rag-vs-fine-tuning-a-comparative-analysis-of-llm-learning-techniques/

[^43]: https://lakefs.io/rag-tools/

[^44]: https://arize.com/blog-course/llm-rag-retrieval-augmented-generation-roadmap/

[^45]: https://www.reddit.com/r/MachineLearning/comments/1ck0tnk/d_how_reliable_is_rag_currently/

[^46]: https://www.bentoml.com/blog/building-rag-with-open-source-and-custom-ai-models

[^47]: https://stackoverflow.blog/2023/10/18/retrieval-augmented-generation-keeping-llms-relevant-and-current/

[^48]: https://www.protecto.ai/blog/understanding-llm-evaluation-metrics-for-better-rag-performance

[^49]: https://forum.level1techs.com/t/is-there-a-user-friendly-self-hosted-ai-guide-low-or-no-code/211200

[^50]: https://research.ibm.com/blog/retrieval-augmented-generation-RAG

[^51]: https://aisera.com/blog/llm-fine-tuning-vs-rag/

[^52]: https://bendersky.github.io/pubs/2013-1.pdf

[^53]: https://www.youtube.com/watch?v=wW5OtLjKr90

[^54]: https://www.anthropic.com/news/contextual-retrieval

[^55]: https://deconvoluteai.com/blog/information-retrieval-introduction

[^56]: https://blog.ori.co/how-to-perform-a-cost-per-token-analysis-of-self-hosted-llms-dbrx-from-databricks

[^57]: https://incubity.ambilio.com/how-to-optimize-the-cost-of-a-rag-pipeline/

[^58]: https://www.reddit.com/r/SaaS/comments/1b92w5o/how_i_reduced_our_startups_llm_costs_by_almost_90/

[^59]: https://tinyml.substack.com/p/openai-vs-self-hosted-llms-a-cost

[^60]: https://getstream.io/blog/best-local-llm-tools/

