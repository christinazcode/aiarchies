<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" class="logo" width="120"/>

# what is the preferred self hosted embedding model for a self hosted gpt-neox rag system for a small or medium enterprise where cost per use is to be minimized compared to performance

---
For a small or medium enterprise looking to minimize cost per use while maintaining performance in a self-hosted GPT-NeoX RAG system, several open-source embedding models can be considered. Here are some options:

## Open-Source Embedding Models

1. **Stella**: This model is noted for its excellent performance and compact size, making it easy to fine-tune for better results. It's a good choice for self-hosting due to its efficiency and cost-effectiveness[^4].
2. **E5 Models**: The E5 models, such as `intfloat/e5-large-v2`, are designed for efficient embedding and are popular choices for RAG applications. They offer a balance of performance and resource usage[^2][^13].
3. **all-MiniLM-L6-v2**: This model is another efficient option that can be self-hosted. It is widely used for text embedding tasks and can be easily deployed on various platforms[^8].

## Considerations for Self-Hosting

- **Cost**: Self-hosting eliminates per-use costs associated with cloud APIs, reducing overall expenses.
- **Performance**: While open-source models might not match the performance of proprietary models like OpenAI's, they can still provide excellent results, especially when fine-tuned for specific tasks.
- **Data Privacy**: Self-hosting ensures complete control over data, enhancing privacy and security.


## Tools for Simplifying Self-Hosting

- **Ollama**: This platform simplifies the process of running and managing open-source models locally, reducing dependency and compatibility issues[^1].
- **pgai Vectorizer**: This tool automates embedding generation and management directly in PostgreSQL, making it easier to integrate with your RAG system[^1].


## Recommendation

For a self-hosted GPT-NeoX RAG system aiming to minimize cost while maintaining performance, **Stella** or **E5 models** could be excellent choices. Both offer strong performance and are cost-effective. Using tools like Ollama and pgai Vectorizer can streamline the deployment and management of these models. Always evaluate models on your specific dataset to ensure the best fit for your application.

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

