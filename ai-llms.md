# 🤖 AI & LLMs

> Building with and on large language models.

---

## 🧠 Foundation Model Concepts

| Concept | What it is |
|---------|-----------|
| **Transformer architecture** | Self-attention + positional encoding + feed-forward layers |
| **Attention mechanism** | Each token attends to every other token with learned weights |
| **Tokenization** | BPE, WordPiece — split text into sub-word tokens |
| **Context window** | Max tokens model can process at once — affects cost and capability |
| **Embeddings** | Dense vector representations capturing semantic meaning |
| **Autoregressive generation** | Generate one token at a time, each conditioned on previous |
| **Decoder-only vs encoder-decoder** | GPT-style vs T5/BART — different training objectives |
| **Multimodal models** | Vision + language in same model (GPT-4V, Claude, Gemini) |

---

## 💬 Prompt Engineering

| Technique | What it is |
|-----------|-----------|
| **System prompts** | Set model persona, instructions, constraints, output format |
| **Few-shot learning** | Provide examples in prompt to guide output format and style |
| **Zero-shot** | No examples — rely entirely on model's training |
| **Chain-of-thought (CoT)** | Ask model to reason step-by-step before answering |
| **ReAct** | Reasoning + Acting: interleave thinking with tool use |
| **Tree of Thought** | Explore multiple reasoning paths, evaluate and select best |
| **Structured output** | JSON mode, function calling to get parseable responses |
| **Temperature** | 0 = deterministic · 1 = creative · >1 = chaotic |
| **Top-p / nucleus sampling** | Sample from top probability mass — controls output diversity |
| **Prompt injection** | Malicious user input overriding system instructions — must sanitize |

---

## 📚 RAG & Knowledge Augmentation

| Concept | What it is |
|---------|-----------|
| **RAG** | Retrieval-Augmented Generation: inject relevant docs into context window |
| **Chunking strategies** | Fixed-size, semantic, recursive, sentence-based — affects retrieval quality |
| **Embedding models** | text-embedding-3-small, BGE, E5 — map text to dense vectors |
| **Vector similarity** | Cosine, dot product, Euclidean distance for nearest-neighbor search |
| **Reranking** | Cross-encoder rerankers (Cohere, BGE) to improve retrieved chunk order |
| **Hybrid search** | Combine dense (vector) + sparse (BM25/keyword) retrieval |
| **Knowledge graphs** | Structured entity-relation stores for multi-hop reasoning |
| **Context stuffing** | Directly inject all relevant docs when context window is large enough |

---

## 🔧 LLM Frameworks & Tools

| Tech | What it's for |
|------|--------------|
| **LangChain** | Orchestrate LLMs, tools, memory, retrieval chains, agents |
| **LlamaIndex** | Data framework for RAG — ingestion, indexing, structured retrieval |
| **DSPy** | Programmatic prompt optimization — optimize prompts as parameters |
| **Haystack** | Production NLP pipelines, RAG, document search |
| **Instructor** | Structured output extraction from LLMs using Pydantic |
| **Outlines** | Guaranteed structured output generation |
| **Marvin** | Python AI toolkit for building natural language interfaces |

---

## 🗄️ Vector Databases

| DB | What it's for |
|----|--------------|
| **pgvector** | PostgreSQL extension — reuse existing DB, no new infrastructure |
| **Pinecone** | Managed vector DB — serverless, easy to start |
| **Weaviate** | Self-hostable, multimodal, hybrid search built-in |
| **Qdrant** | High-performance Rust-based vector DB |
| **Chroma** | Lightweight open-source for local RAG and prototyping |
| **Milvus** | High-performance distributed vector search |
| **Redis + VSS** | Vector similarity search on Redis |

---

## 🎓 Fine-tuning & Adaptation

| Technique | What it is |
|-----------|-----------|
| **Supervised fine-tuning (SFT)** | Train on labeled input-output pairs for task adaptation |
| **LoRA** | Low-rank adapters — train small matrices, not full model weights |
| **QLoRA** | Quantized LoRA — fine-tune large models on consumer GPUs |
| **RLHF** | Reinforcement learning from human feedback — alignment technique |
| **DPO** | Direct Preference Optimization — simpler RLHF alternative |
| **PEFT** | HuggingFace library: LoRA, prefix tuning, p-tuning |
| **Instruction tuning** | Fine-tune to follow instructions better |
| **GGUF / llama.cpp** | Quantized model formats for efficient local inference |

---

## 📊 AI Ops & Evaluation

| Tool/Concept | What it's for |
|-------------|--------------|
| **LangSmith** | Tracing, evaluation datasets, prompt management for LLM apps |
| **Arize / Phoenix** | LLM observability, drift detection, retrieval evaluation |
| **RAGAS** | RAG evaluation — faithfulness, answer relevance, context recall |
| **Evals** | Systematic evaluation: MMLU, HumanEval, custom domain benchmarks |
| **Guardrails.ai** | Output validation, content filtering, structured generation |
| **NeMo Guardrails** | Programmable guardrails for conversational AI safety |
| **Token cost tracking** | Monitor and budget API spending per user/tenant/feature |
| **Latency optimization** | Streaming responses, caching, model selection by task complexity |

---

## 🗺️ Suggested Roadmap

```
Prompt engineering (zero-shot, few-shot, CoT)
    → API integration (OpenAI / Anthropic)
    → Embeddings + vector search
    → RAG pipeline (chunking + retrieval + generation)
    → LangChain / LlamaIndex
    → Evaluation + observability (LangSmith, RAGAS)
    → Fine-tuning (LoRA / QLoRA)
    → Production (streaming, caching, cost management)
    → Agents + multi-step tool use
```
