<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" class="logo" width="120"/>

# what is the preferred hosted embedding model for a hosted gpt-neox rag system for a small or medium enterprise

---
For a small or medium enterprise looking to implement a hosted GPT-NeoX RAG system, there are several strong options for embedding models. Based on the latest information and considering factors like performance, cost, and ease of use, here are some preferred choices:

## Cloud-based Solutions

1. **OpenAI's text-embedding-3-small**: This model offers an excellent balance of performance and cost-effectiveness. It's the latest in OpenAI's embedding series and provides strong results for retrieval tasks[^1][^4].
2. **Cohere's Embed v3**: Known for its high performance in retrieval tasks, this model is another top choice for RAG systems[^1].

## Open-source Options

If you prefer an open-source solution that can be easily hosted:

1. **E5-base-v2**: This model offers a good balance between performance and resource requirements. With 768 embedding dimensions and 109M parameters, it's suitable for many small to medium enterprises[^4].
2. **BGE (BAAI/bge-base-en-v1.5)**: While there are concerns about overfitting to benchmarks, it still performs well in many real-world scenarios[^5].

## Considerations for SMEs

- **Cost**: Cloud-based solutions like OpenAI and Cohere offer cutting-edge performance but come with usage-based pricing. For budget-conscious SMEs, self-hosting an open-source model might be more cost-effective in the long run.
- **Ease of Use**: Cloud-based options typically provide simple APIs, making integration straightforward. However, they may have limitations on customization.
- **Performance**: While open-source models can perform well, proprietary cloud-based models often have a slight edge in performance due to more extensive training data and resources.
- **Scalability**: Cloud-based solutions generally offer better scalability, which can be crucial as your enterprise grows.


## Recommendation

For most small to medium enterprises implementing a hosted GPT-NeoX RAG system, **OpenAI's text-embedding-3-small** is likely the best choice. It offers:

1. State-of-the-art performance
2. Easy integration through API
3. Scalability to handle growing demands
4. Continuous updates and improvements

If budget is a primary concern or you require more control over the model, consider hosting the **E5-base-v2** model. It provides a good balance of performance and resource requirements while allowing for customization and potentially lower long-term costs.

Remember to benchmark these options with your specific dataset and use case to determine the best fit for your enterprise's needs.

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

