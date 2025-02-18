<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" class="logo" width="120"/>

# what is the preferred self hosted embedding model for a self hosted gpt-neox rag system for a small or medium enterprise where cost per use is to be minimized compared to performance

---
For a self-hosted GPT-NeoX RAG system tailored to small or medium enterprises (SMEs) with a focus on minimizing costs while maintaining reasonable performance, open-source embedding models are the preferred choice. These models eliminate recurring API costs, enhance data privacy, and allow full control over the infrastructure. Here are the best options based on cost-efficiency and performance:

## Recommended Open-Source Embedding Models

1. **E5 Models (e.g., `intfloat/e5-large-v2`)**:
    - **Strengths**: High performance in semantic retrieval tasks, competitive with proprietary models.
    - **Use Case**: General-purpose text embeddings for document search or question answering.
    - **Cost Efficiency**: Free to use; requires hosting infrastructure but avoids API charges.
    - **Performance**: Strong results in benchmarks like MTEB (Massive Text Embedding Benchmark)[^1][^5][^10].
2. **BAAI/bge-small-en-v1.5**:
    - **Strengths**: Compact size with good performance for English-language tasks.
    - **Use Case**: Suitable for SMEs with limited computational resources.
    - **Cost Efficiency**: Lightweight model reduces hosting costs.
    - **Performance**: Performs well for context-heavy queries[^5].
3. **MiniLM Models (e.g., `sentence-transformers/all-MiniLM-L6-v2`)**:
    - **Strengths**: Low-dimensional embeddings (368 dimensions), reducing storage requirements.
    - **Use Case**: Ideal for space-constrained setups or applications requiring fast embedding generation.
    - **Cost Efficiency**: Minimal resource requirements and free to use.
    - **Performance**: Good balance of speed and accuracy for smaller datasets[^3][^12].
4. **Instructor Models (e.g., `hkunlp/instructor-xl`)**:
    - **Strengths**: Instruction-tuned embeddings tailored for specific tasks.
    - **Use Case**: Applications requiring task-specific embeddings, such as summarization or classification.
    - **Cost Efficiency**: Free and versatile, though slightly larger in size compared to MiniLM[^5].

## Infrastructure Considerations

- Use tools like **Ollama** to simplify deployment and management of these models locally. Ollama bundles configuration, data, and weights, making it easier to experiment with different models without complex setups[^1][^13].
- Leverage vector databases such as PostgreSQL with extensions like `pgvector` or `pgai Vectorizer` for efficient embedding storage and retrieval[^1][^7].
- Hardware requirements depend on the model size:
    - Smaller models like MiniLM can run efficiently on CPUs.
    - Larger models like E5 may require GPUs for faster embedding generation.


## Why Open-Source Models?

- **Cost Savings**: Avoid recurring API fees from proprietary providers like OpenAI or Cohere.
- **Data Privacy**: Self-hosting ensures sensitive data never leaves your infrastructure.
- **Customization**: Open-source models can be fine-tuned for domain-specific tasks.


## Recommendation

For SMEs prioritizing cost-efficiency, start with `intfloat/e5-large-v2` or `sentence-transformers/all-MiniLM-L6-v2`. Both models provide excellent trade-offs between performance and resource usage. Use Ollama and PostgreSQL-based tools like `pgai Vectorizer` to streamline deployment and embedding management. These solutions minimize operational costs while maintaining robust RAG system capabilities.

<div style="text-align: center">⁂</div>

[^1]: https://www.timescale.com/blog/finding-the-best-open-source-embedding-model-for-rag

[^2]: https://www.timescale.com/blog/open-source-vs-openai-embeddings-for-rag

[^3]: https://www.reddit.com/r/LocalLLaMA/comments/18j39qt/what_embedding_models_are_you_using_for_rag/

[^4]: https://softwaremill.com/embedding-models-comparison/

[^5]: https://www.pragnakalp.com/open-source-embedding-models-which-one-performs-best/

[^6]: https://writingmate.ai/blog/the-best-embedding-models

[^7]: https://entgo.io/blog/2025/02/12/rag-with-ent-atlas-pgvector/

[^8]: https://www.graft.com/blog/open-source-text-embedding-models

[^9]: https://www.datastax.com/blog/best-embedding-models-information-retrieval-2025

[^10]: https://www.pinecone.io/learn/series/rag/embedding-models-rundown/

[^11]: https://www.enterprisebot.ai/blog/choose-the-best-embedding-model-for-your-retrieval-augmented-generation-rag-system

[^12]: https://www.reddit.com/r/Supabase/comments/13x0nwt/what_is_the_most_costefficient_way_to_have_an/

[^13]: https://www.reddit.com/r/ollama/comments/1hhy0tt/finding_the_best_opensource_embedding_model_for/

[^14]: https://www.timescale.com/blog/which-openai-embedding-model-is-best

[^15]: https://www.datastax.com/blog/best-embedding-models-information-retrieval-2025

[^16]: https://www.bentoml.com/blog/a-guide-to-open-source-embedding-models

[^17]: https://www.reddit.com/r/Rag/comments/1hdd3u2/which_embedding_model_should_i_use_need_help/

[^18]: https://www.bentoml.com/blog/building-rag-with-open-source-and-custom-ai-models

[^19]: https://www.puppyagent.com/blog/How-to-Implement-a-Multilingual-RAG-System-Effectively-in-2025

[^20]: https://huggingface.co/docs/transformers/en/model_doc/gpt_neox

[^21]: https://github.com/infiniflow/ragflow

[^22]: https://ai.plainenglish.io/choosing-an-embedding-model-for-retrieval-augmented-generation-rag-705dbb8a9e12

[^23]: https://www.pragnakalp.com/open-source-embedding-models-which-one-performs-best/

[^24]: https://github.com/tensorchord/Awesome-LLMOps

[^25]: https://www.reddit.com/r/LocalLLaMA/comments/1fl6hl3/leading_opensource_embedding_model/

[^26]: https://bdtechtalks.com/2024/01/08/microsoft-llm-embeddings/

[^27]: https://www.timescale.com/blog/general-purpose-vs-domain-specific-embedding-models

[^28]: https://codesphere.com/articles/best-open-source-sentence-embedding-models

[^29]: https://cloud.google.com/vertex-ai/generative-ai/docs/use-embedding-models

[^30]: https://www.timescale.com/blog/open-source-vs-openai-embeddings-for-rag

[^31]: https://writingmate.ai/blog/the-best-embedding-models

[^32]: https://github.com/mikeroyal/Self-Hosting-Guide

[^33]: https://towardsdatascience.com/openai-vs-open-source-multilingual-embedding-models-e5ccb7c90f05/

[^34]: https://cloud.google.com/vertex-ai/generative-ai/docs/embeddings/get-text-embeddings

[^35]: https://telnyx.com/resources/embedding-vs-fine-tuning

[^36]: https://blog.getzep.com/text-embedding-latency-a-semi-scientific-look/

