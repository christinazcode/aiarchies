<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" class="logo" width="120"/>

# what is the preferred self hosted embedding model for a self hosted gpt-neox rag system for a small or medium enterprise where cost per use is to be minimized compared to performance

---
For a self-hosted GPT-NeoX RAG system focused on minimizing cost per use while maintaining reasonable performance, several open-source embedding models stand out as strong candidates.

## Recommended Models

The most cost-effective self-hosted embedding model options include:

- all-MiniLM-L6-v2: Offers a good balance of performance with minimal resource requirements (137M parameters, 768 dimensions)[^1]
- Stella: Provides excellent out-of-box performance and is small enough to fine-tune easily[^4]
- E5-large-v2: Strong performance while being more resource-efficient than larger models[^2]


## Key Advantages

Self-hosting these models provides several benefits:

- Eliminates ongoing API costs and "OpenAI tax"[^1]
- Provides complete control over data privacy[^1]
- Allows for local deployment and customization[^1]


## Deployment Recommendation

For optimal cost-efficiency while maintaining performance:

1. Use Ollama as your deployment platform, which simplifies model management and eliminates dependency issues[^1]
2. Start with all-MiniLM-L6-v2 as your base model due to its smaller size (274MB) and efficient resource usage[^1]
3. Deploy on CPU rather than GPU for better cost efficiency, as CPU deployment is cheaper and easier to scale[^19]

This combination provides a practical balance between performance and resource consumption while keeping operational costs minimal for small to medium enterprises.

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

