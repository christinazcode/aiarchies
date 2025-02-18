<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" class="logo" width="120"/>

# what is the preferred self hosted embedding model for a self hosted gpt-neox rag system for a small or medium enterprise where cost per use is to be minimized compared to performance

---
For a small or medium enterprise prioritizing minimal cost per use in a self-hosted GPT-NeoX RAG system, open-source embedding models are the preferred choice[^1][^3]. Here's a breakdown of suitable options and considerations:

## Open-Source Embedding Models

* **all-MiniLM-L6-v2**: This model is a cost-efficient option for text embedding and can be used for Supabase edge functions[^8].
* **E5 Models**: The E5 models, such as `intfloat/e5-large-v2`, are designed for efficient embedding and are worth considering[^2].
* **Stella**: Stella is an excellent open-source option that is small enough to fine-tune for even better performance[^4].


## Key Considerations

* **Cost**: Open-source models eliminate the "OpenAI tax" and give you complete control over the embedding creation process[^1]. Using self-hosted models avoids the ongoing costs associated with cloud-based API solutions[^3][^16].
* **Data Privacy**: Open-source models enhance data privacy by allowing you to run them locally, ensuring complete control over how your data is handled[^1].
* **Customization**: Open-source models offer a customizable alternative, allowing you to tailor the models to your specific needs[^1].
* **Tools**: Tools like Ollama and pgai Vectorizer can simplify the process of comparing and managing open-source embedding models[^1]. Ollama helps in accessing and managing the models, while pgai Vectorizer automates embedding generation and storage in PostgreSQL[^1].
* **Hardware**: When testing open-source models, focus on CPU performance for cost-effective scaling[^19].

Given these factors, a practical approach would be to evaluate `all-MiniLM-L6-v2`, E5 models, and Stella using tools like Ollama and pgai Vectorizer to determine which provides the best balance of performance and cost for your specific use case[^1][^2][^4]. Benchmarking these models on your data is crucial to find the optimal solution[^15].

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

