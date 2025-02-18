<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" class="logo" width="120"/>

# what is the preferred hosted embedding model for a hosted gpt-neox rag system for a small or medium enterprise

---
For a hosted GPT-NeoX RAG system in a small or medium enterprise, here's a breakdown of embedding model considerations based on the search results:

* **Factors to consider:** When choosing an embedding model, it's important to consider factors such as performance, dimensionality, multilingual support (if needed), hosting requirements (self-hosted vs. cloud-based), and domain specificity[^1][^3][^4].
* **Hugging Face MTEB Leaderboard:** A good starting point is the Hugging Face MTEB (Massive Text Embedding Benchmark) leaderboard[^6].

Given these points, here are some suitable options for a small or medium enterprise:

* **OpenAI's text-embedding-3-large:** This is a strong choice due to its excellent performance in retrieval tasks[^1]. However, it is a cloud-based service, which may have cost considerations.
* **Cohere's Embed v3:** Similar to OpenAI, Cohere's Embed v3 offers a good balance of accuracy and efficiency[^1]. It is also a cloud-based option.
* **Open-source options:**
    * **E5-large-v2 or BAAI/bge-large-en-v1.5:** These are viable open-source alternatives if you prefer self-hosting[^1].
    * **intfloat/multilingual-e5-large-instruct:**  Consider this if multilingual support is needed[^1].
    * **jinaai/jina-embeddings-v2-base-code:** If the RAG system is focused on code-related tasks, this model could be a good fit[^1][^5].

It's recommended to benchmark a few different embedding models with your specific data and use case to determine the optimal choice for your GPT-NeoX RAG system[^1].

<div style="text-align: center">⁂</div>

[^1]: https://www.enterprisebot.ai/blog/choose-the-best-embedding-model-for-your-retrieval-augmented-generation-rag-system

[^2]: https://huggingface.co/docs/transformers/en/model_doc/gpt_neox

[^3]: https://www.timescale.com/blog/finding-the-best-open-source-embedding-model-for-rag

[^4]: https://cloud.google.com/vertex-ai/generative-ai/docs/use-embedding-models

[^5]: https://www.reddit.com/r/LocalLLaMA/comments/18j39qt/what_embedding_models_are_you_using_for_rag/

[^6]: https://unstructured.io/blog/understanding-embedding-models-make-an-informed-choice-for-your-rag

[^7]: https://buttondown.com/ainews/archive/ainews-contextual-document-embeddings-cde-small-v1/

[^8]: https://vectorize.io/picking-the-best-embedding-model-for-rag/

[^9]: https://www.mongodb.com/developer/products/atlas/choose-embedding-model-rag/

[^10]: https://www.galileo.ai/blog/mastering-rag-how-to-select-an-embedding-model

[^11]: https://www.pinecone.io/learn/series/rag/embedding-models-rundown/

[^12]: https://github.com/tensorchord/Awesome-LLMOps

[^13]: https://nlpcloud.com/effectively-using-gpt-j-gpt-neo-gpt-3-alternatives-few-shot-learning.html

[^14]: https://github.com/Hannibal046/Awesome-LLM

[^15]: https://github.com/EleutherAI/gpt-neox

