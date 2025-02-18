<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" class="logo" width="120"/>

# what is the preferred self hosted embedding model for a self hosted gpt-neox rag system for a small or medium enterprise where cost per use is to be minimized compared to performance

---
For a self-hosted GPT-NeoX RAG system aimed at small or medium enterprises where minimizing cost per use is critical, open-source embedding models are the optimal choice. Below are the most suitable open-source embedding models and tools to consider:

## Recommended Open-Source Embedding Models

1. **intfloat/e5-large-v2**
    - **Description**: A high-performing model designed for text embeddings, optimized for retrieval tasks.
    - **Advantages**: Efficient and cost-effective while maintaining strong performance in RAG systems.
    - **Use Case**: General-purpose text retrieval with good trade-offs between performance and resource requirements[^2][^9][^13].
2. **Stella**
    - **Description**: An open-source model that is lightweight and easy to fine-tune.
    - **Advantages**: Small size makes it ideal for SMEs with limited computational resources.
    - **Use Case**: Applications requiring domain-specific fine-tuning or lightweight deployment[^4][^9].
3. **all-MiniLM-L6-v2**
    - **Description**: A compact model offering fast inference and low resource usage.
    - **Advantages**: Ideal for CPU-based deployments, making it cost-efficient for small-scale operations.
    - **Use Case**: Scenarios where latency and cost are prioritized over absolute retrieval accuracy[^8][^19].
4. **BAAI/bge-large-en-v1.5**
    - **Description**: A robust embedding model with strong performance across a variety of NLP tasks.
    - **Advantages**: Balances performance and cost well, suitable for SMEs needing high-quality embeddings without vendor lock-in.
    - **Use Case**: RAG systems requiring high retrieval accuracy on diverse datasets[^9][^14].

## Tools for Simplified Deployment

1. **Ollama**
    - Provides an easy way to run open-source models locally with minimal setup.
    - Bundles configuration, data, and weights, ensuring full control over data privacy and costs[^1].
2. **pgai Vectorizer**
    - Automates embedding generation and management directly in PostgreSQL databases, reducing infrastructure complexity[^1].
3. **pgvector**
    - A PostgreSQL extension that enables vector storage and similarity search, perfect for embedding-based retrieval tasks.

## Why These Models Are Suitable for SMEs

- **Cost-Effectiveness**: Open-source models eliminate API costs associated with proprietary solutions like OpenAI or Cohere.
- **Data Privacy**: Running models locally ensures full control over sensitive data.
- **Flexibility**: Many of these models can be fine-tuned or adapted to specific business needs without incurring additional costs.


## Recommendation

For most small or medium enterprises, starting with `intfloat/e5-large-v2` or `all-MiniLM-L6-v2` is recommended due to their balance of performance and efficiency. Pairing these models with tools like Ollama and pgai Vectorizer simplifies deployment while minimizing operational costs.

<div style="text-align: center">⁂</div>

[^1]: https://www.timescale.com/blog/finding-the-best-open-source-embedding-model-for-rag

[^2]: https://modal.com/blog/embedding-models-article

[^3]: https://softwaremill.com/embedding-models-comparison/

[^4]: https://www.datastax.com/blog/best-embedding-models-information-retrieval-2025

[^5]: https://www.reddit.com/r/LocalLLaMA/comments/18j39qt/what_embedding_models_are_you_using_for_rag/

[^6]: https://www.graft.com/blog/open-source-text-embedding-models

[^7]: https://github.com/EleutherAI/gpt-neox

[^8]: https://www.reddit.com/r/Supabase/comments/13x0nwt/what_is_the_most_costefficient_way_to_have_an/

[^9]: https://www.pragnakalp.com/open-source-embedding-models-which-one-performs-best/

[^10]: https://writingmate.ai/blog/the-best-embedding-models

[^11]: https://huggingface.co/docs/transformers/en/model_doc/gpt_neox

[^12]: https://huggingface.co/docs/transformers/en/model_doc/gpt_neo

[^13]: https://www.pinecone.io/learn/series/rag/embedding-models-rundown/

[^14]: https://www.bentoml.com/blog/a-guide-to-open-source-embedding-models

[^15]: https://www.mongodb.com/developer/products/atlas/choose-embedding-model-rag/

[^16]: https://towardsdatascience.com/openai-vs-open-source-multilingual-embedding-models-e5ccb7c90f05/

[^17]: https://vectorize.io/picking-the-best-embedding-model-for-rag/

[^18]: https://www.enterprisebot.ai/blog/choose-the-best-embedding-model-for-your-retrieval-augmented-generation-rag-system

[^19]: https://blog.getzep.com/text-embedding-latency-a-semi-scientific-look/

[^20]: https://ai.plainenglish.io/choosing-an-embedding-model-for-retrieval-augmented-generation-rag-705dbb8a9e12

