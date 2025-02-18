<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" class="logo" width="120"/>

# what is the preferred self hosted embedding model for a self hosted gpt-neox rag system for a small or medium enterprise where cost per use is to be minimized compared to performance

---
For a small or medium enterprise looking to minimize cost per use while maintaining performance in a self-hosted GPT-NeoX RAG system, several open-source embedding models are suitable options. Here are some considerations and recommendations:

## Key Considerations

1. **Cost**: Self-hosting eliminates per-use costs associated with cloud APIs, reducing expenses over time.
2. **Performance**: Choose models that balance performance with resource requirements.
3. **Ease of Integration**: Models with straightforward deployment and management are preferable.

## Recommended Models

1. **Stella**: This model is highly regarded for its performance in retrieval tasks and is available under the MIT license, making it suitable for commercial use. The Stella 400M and 1.5B variants offer different balances of size and performance[^4].
2. **intfloat/e5-large-v2**: Known for efficient embedding generation, this model is well-suited for various NLP tasks and can be a cost-effective choice for RAG applications[^2].
3. **ModernBERT Embed**: This model offers a balance of speed and accuracy, making it a viable option for applications where both are important[^4].

## Tools for Simplification

- **Ollama**: This platform simplifies the process of running and managing open-source models locally, reducing dependency and compatibility issues[^1].
- **pgai Vectorizer**: Automates embedding generation and management directly in PostgreSQL, making it easier to integrate with your RAG system[^1].


## Recommendation

For a self-hosted GPT-NeoX RAG system, **Stella 400M v5** is a strong choice due to its high performance, open-source nature, and commercial usability. It offers a good balance between size and performance, making it suitable for small to medium enterprises looking to minimize costs while maintaining performance.

If you need a more lightweight option with efficient embedding generation, **intfloat/e5-large-v2** could be an alternative. Both models can be easily managed and deployed using tools like Ollama and pgai Vectorizer.

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

[^14]: https://www.reddit.com/r/Supabase/comments/13x0nwt/what_is_the_most_costefficient_way_to_have_an/

[^15]: https://www.bentoml.com/blog/a-guide-to-open-source-embedding-models

[^16]: https://www.graft.com/blog/open-source-text-embedding-models

[^17]: https://www.mongodb.com/developer/products/atlas/choose-embedding-model-rag/

[^18]: https://towardsdatascience.com/openai-vs-open-source-multilingual-embedding-models-e5ccb7c90f05/

[^19]: https://vectorize.io/picking-the-best-embedding-model-for-rag/

[^20]: https://www.pragnakalp.com/open-source-embedding-models-which-one-performs-best/

[^21]: https://www.enterprisebot.ai/blog/choose-the-best-embedding-model-for-your-retrieval-augmented-generation-rag-system

[^22]: https://blog.getzep.com/text-embedding-latency-a-semi-scientific-look/

[^23]: https://ai.plainenglish.io/choosing-an-embedding-model-for-retrieval-augmented-generation-rag-705dbb8a9e12

[^24]: https://www.timescale.com/blog/which-openai-embedding-model-is-best

[^25]: https://www.reddit.com/r/LocalLLaMA/comments/1fl6hl3/leading_opensource_embedding_model/

[^26]: https://codesphere.com/articles/best-open-source-sentence-embedding-models

[^27]: https://cloud.google.com/vertex-ai/generative-ai/docs/use-embedding-models

[^28]: https://mono.software/2024/11/07/testing-embedding-models-rag/

[^29]: https://www.timescale.com/blog/open-source-vs-openai-embeddings-for-rag

[^30]: https://github.com/mikeroyal/Self-Hosting-Guide

[^31]: https://writingmate.ai/blog/the-best-embedding-models

[^32]: https://cloud.google.com/vertex-ai/generative-ai/docs/embeddings/get-text-embeddings

[^33]: https://bdtechtalks.com/2024/01/08/microsoft-llm-embeddings/

