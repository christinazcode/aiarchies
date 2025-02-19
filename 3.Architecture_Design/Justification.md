# Justification for Building a Self-Hosted RAG System

This document outlines the rationale for building a self-hosted Retrieval-Augmented Generation (RAG) system using the following components: **all-MiniLM-L6-v2** embedding model, **GPT-NeoX** as the LLM, **Milvus** as the vector database, BM25 for initial ranking, and tools like **Langfuse**, **MLflow**, and **DeepEval** for observability and guardrails. It also includes an analysis of cost, performance, and comparisons with alternative solutions.

---

## **System Components and Justifications**

### **1. Embedding Model: all-MiniLM-L6-v2**

- **Why this model?**:
    - The all-MiniLM-L6-v2 model is compact (6 layers, 384 dimensions), offering fast embedding generation with reduced computational costs. It balances simplicity and ranking quality, making it ideal for scalable RAG systems[^1][^8].
    - While larger models like SGPT or GTR may offer better retrieval quality, they require expensive GPUs and higher latency[^8].


### **2. LLM: GPT-NeoX**

- **Why GPT-NeoX?**:
    - Open-source and self-hosted, GPT-NeoX provides flexibility and cost-efficiency compared to proprietary cloud-based models like GPT-4 or Claude.
    - It supports fine-tuning for domain-specific tasks and can be optimized using techniques such as quantization to reduce memory usage while maintaining performance[^7][^9].


### **3. Vector Database: Milvus**

- **Why Milvus?**:
    - Milvus is a high-performance open-source vector database optimized for handling embeddings at scale. It integrates seamlessly with RAG pipelines and offers cost-effective operation when self-hosted compared to cloud options like Pinecone[^4][^7].
    - Its scalability ensures smooth handling of large datasets without compromising latency.


### **4. Initial Ranking Model: BM25**

- BM25 is a robust text-based ranking algorithm that efficiently narrows down candidates before embedding-based retrieval. This hybrid approach improves query latency by reducing the number of vectors processed in subsequent stages.


### **5. Observability \& Guardrails**

- **Langfuse (Observability)**:
    - Langfuse provides observability for LLM pipelines, enabling monitoring of prompt performance, response quality, and error tracking. Its open-source version is free to self-host[^3].
- **MLflow \& DeepEval (Guardrails)**:
    - MLflow tracks experiments and model versions, ensuring reproducibility in fine-tuning workflows.
    - DeepEval adds automated evaluation frameworks to ensure output quality aligns with business needs.

---

## **Annual Cost of Ownership**

| Component | Cost Estimate (Annual) |
| :-- | :-- |
| **Hardware (GPUs)** | \$12,000–\$15,000 for A100 GPUs (or \$3/hour for cloud GPU rentals during heavy loads)[^4]. |
| **Milvus Database** | Free (self-hosted); infrastructure costs depend on server usage (~\$1,000–\$5,000/year)[^4]. |
| **Langfuse** | Free (open-source version)[^3]. |
| **MLflow \& DeepEval** | Free (self-hosted); infrastructure costs negligible if hosted on existing servers. |
| **Embedding Computation** | Negligible if run on local GPUs; API-based alternatives cost ~\$0.0004/1k tokens[^4]. |
| **Electricity \& Maintenance** | ~\$2,000–\$5,000 depending on hardware usage intensity. |

**Total Annual Cost:** \$15,000–\$25,000 (self-hosted). This is significantly lower than recurring API costs for proprietary LLMs like GPT-4 (\$0.03–\$0.12 per token)[^4].

---

## **Performance Comparison: Alternative LLMs**

| Model | Parameters | Strengths | Weaknesses |
| :-- | :-- | :-- | :-- |
| GPT-NeoX | Variable | Open-source; customizable; cost-efficient[^7]. | Requires infrastructure investment. |
| LLaMA 3 | Up to 70B | Superior reasoning; open-source[^5][^6]. | Higher memory/GPU requirements. |
| Falcon 180B | 180B | High accuracy; excels in generative tasks[^5]. | Expensive to self-host. |
| Mistral 7B | 7B | Efficient; fast inference; low latency[^5][^6]. | Limited capacity for complex queries. |

GPT-NeoX strikes a balance between cost-efficiency and performance for most RAG applications.

---

## **Advantages of Self-Hosting**

1. **Cost Efficiency**:
    - Self-hosting reduces reliance on expensive APIs like OpenAI’s GPT models.
    - Operational costs drop to approximately 10% of cloud-based solutions when scaled effectively[^2][^4].
2. **Data Privacy \& Security**:
    - Ensures sensitive data remains within organizational boundaries.
    - No risk of data leakage to third-party providers.
3. **Customizability**:
    - Fine-tune models for specific domains or use cases.
    - Optimize pipelines with tailored workflows.
4. **Scalability**:
    - Easily scale hardware resources based on demand without incurring per-query costs.

---

## Conclusion

Building a self-hosted RAG system using all-MiniLM-L6-v2 embeddings, GPT-NeoX LLM, Milvus vector database, BM25 ranking model, Langfuse observability tools, MLflow, and DeepEval offers significant advantages in terms of cost efficiency, data privacy, and customizability. While initial setup requires hardware investment (~\$15k–\$25k annually), the long-term savings far outweigh the recurring expenses of cloud-based solutions.

This stack is optimal for organizations prioritizing control over their AI systems while ensuring high-quality retrieval and generation capabilities at scale.

<div style="text-align: center">⁂</div>

[^1]: https://www.reddit.com/r/LocalLLaMA/comments/18j39qt/what_embedding_models_are_you_using_for_rag/

[^2]: https://myscale.com/blog/what-to-expect-rag/

[^3]: https://langfuse.com/pricing-self-host

[^4]: https://blog.stackademic.com/rag-systems-made-easy-a-step-by-step-cost-and-implementation-guide-1213f908f590

[^5]: https://botpress.com/blog/best-large-language-models

[^6]: https://www.wordware.ai/blog/compare-llms-a-guide-to-finding-the-best-large-language-models

[^7]: https://towardsdatascience.com/retrieval-augmented-generation-rag-inference-engines-with-langchain-on-cpus-d5d55f398502/

[^8]: https://blog.metarank.ai/from-zero-to-semantic-search-embedding-model-592e16d94b61

[^9]: https://www.bacancytechnology.com/blog/best-llm-models

[^10]: https://friendli.ai/blog/friendli-engine-tensorrt-llm-vllm

[^11]: https://www.chatbees.ai/blog/rag-llm

[^12]: https://labelyourdata.com/articles/types-of-llms

[^13]: https://winder.ai/llmops-tools-comparison-open-source-llm-production-frameworks/

[^14]: https://www.bentoml.com/blog/building-rag-with-open-source-and-custom-ai-models

[^15]: https://www.pinecone.io/learn/sagemaker-rag/

[^16]: https://www.youtube.com/watch?v=SNpmkx9cpck

[^17]: https://huggingface.co/sentence-transformers/all-MiniLM-L6-v2

[^18]: https://www.graft.com/blog/open-source-text-embedding-models

[^19]: https://github.com/taishi-i/awesome-ChatGPT-repositories

[^20]: https://blog.keithmcnulty.org/how-i-created-an-ai-version-of-myself-aec12bc30067

[^21]: https://www.restack.io/p/embeddings-knowledge-embedding-models-for-rag-cat-ai

[^22]: https://www.reddit.com/r/selfhosted/comments/1b75mar/llm_who_know_me/

[^23]: https://www.youtube.com/watch?v=q9MD_hU2Yd8

[^24]: https://www.galileo.ai/blog/mastering-rag-how-to-select-an-embedding-model

[^25]: https://pub.towardsai.net/a-taxonomy-of-retrieval-augmented-generation-a39eb2c4e2ab

[^26]: https://www.reddit.com/r/Rag/comments/1h2iitk/what_is_a_range_of_costs_for_a_rag_project/

[^27]: https://www.linkedin.com/posts/tyler-maran_turns-out-self-hosting-can-be-more-expensive-activity-7209644712071225345-_9xm

[^28]: https://www.edenai.co/post/the-2025-guide-to-retrieval-augmented-generation-rag

[^29]: https://news.ycombinator.com/item?id=37148210

[^30]: https://news.ycombinator.com/item?id=41637550

[^31]: https://www.linkedin.com/pulse/beyond-rag-2025-technical-deep-dive-calum-simpson-2fkdc

[^32]: https://docs.llamaindex.ai/en/stable/examples/llm/nvidia_nim/

[^33]: https://dataforest.ai/blog/rag-in-2025-smarter-retrieval-and-real-time-responses

[^34]: https://huggingface.co/avsolatorio/GIST-all-MiniLM-L6-v2

[^35]: https://www.llamaindex.ai/blog/one-click-open-source-rag-observability-with-langfuse

[^36]: https://www.madrona.com/rag-is-not-enough-ai-data-architecture/

[^37]: https://developers.googleblog.com/en/vertex-ai-rag-engine-a-developers-tool/

[^38]: https://www.techtarget.com/whatis/feature/12-of-the-best-large-language-models

[^39]: https://www.bentoml.com/blog/benchmarking-llm-inference-backends

[^40]: https://www.promptingguide.ai/research/rag

[^41]: https://hatchworks.com/blog/gen-ai/large-language-models-guide/

[^42]: https://botscrew.com/blog/llm-comparison-choosing-the-right-model/

[^43]: https://research.aimultiple.com/retrieval-augmented-generation/

[^44]: https://www.tensorops.ai/post/emerging-architectures-of-llm-applications-2025-update

[^45]: https://www.calibraint.com/blog/detailed-comparison-of-all-llm-models-guide

[^46]: https://www.reddit.com/r/LangChain/comments/1dyxty1/can_you_suggest_me_some_best_llms_for_rag/

[^47]: https://dev.to/ezinsightsai/llm-product-development-in-2025-the-ultimate-guide-37f1

[^48]: https://www.debutinfotech.com/blog/large-language-models-comparison

[^49]: https://dev.to/lakhera2015/100-days-of-generative-ai-building-your-first-rag-application-using-open-source-tools-day-8-3kc6

[^50]: https://www.youtube.com/watch?v=BNeegP_3IKI

[^51]: https://github.com/danny-avila/LibreChat/discussions/2233

[^52]: https://www.restack.io/p/embeddings-knowledge-embeddings-vs-rag-cat-ai

[^53]: https://www.syntio.net/en/labs-musings/self-hosted-rag-powered-llm-solution-for-confluence-and-microsoft-sharepoint/

[^54]: https://edrm.net/2025/02/private-llms-vs-rag-systems-choosing-the-right-ai-strategy-for-your-legal-organization/

[^55]: https://langfuse.com/pricing

[^56]: https://langfuse.com/changelog/2024-01-29-custom-model-prices

[^57]: https://www.tensorops.ai/post/understanding-the-cost-of-large-language-models-llms

[^58]: https://langfuse.com/docs/model-usage-and-cost

