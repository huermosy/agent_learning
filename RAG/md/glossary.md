# RAG 术语表

## 核心术语
- **RAG**：Retrieval-Augmented Generation，检索增强生成。
- **Chunk**：文档切分后的最小检索单元。
- **Embedding**：将文本映射为向量表示的方法。
- **Retriever**：负责召回相关内容的检索模块。
- **Reranker**：对召回结果二次排序的模块。
- **Context Window**：模型一次能处理的上下文范围。
- **Hallucination**：模型生成与事实不一致内容的现象。

## 常见易混淆概念
- **RAG vs 微调**：RAG 偏向外部知识注入，微调偏向模型参数层适配。
- **召回 vs 重排**：召回追求找全，重排追求找准。
- **记忆 vs 检索**：记忆偏长期状态，检索偏按需取用外部知识。
