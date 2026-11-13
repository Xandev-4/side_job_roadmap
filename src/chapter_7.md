# 06. AI / LLM Engineering

Priority: **Core** = learn first, **Next** = after Core / when a project needs it, **Later** = just know it exists.

**Do this after** you have a working, deployed FastAPI backend. It's a layer on top of backend skills, not a replacement for them.

## A. LLM foundations

| Done | Concept                                                | Priority | What you should be able to do                     |
| ---- | ------------------------------------------------------ | -------- | ------------------------------------------------- |
| ☐    | What an LLM is (next-token prediction, in plain words) | Core     | Explain it to a friend                            |
| ☐    | Tokens and tokenization                                | Core     | Know why "words ≠ tokens" and why it affects cost |
| ☐    | Context window                                         | Core     | Explain what happens when you exceed it           |
| ☐    | How a response is generated (sampling)                 | Core     | Describe it at a high level                       |
| ☐    | Temperature                                            | Core     | Know what changes when you raise or lower it      |
| ☐    | top-p and top-k                                        | Core     | Explain what each does                            |
| ☐    | Max tokens, stop sequences                             | Core     | Control output length                             |
| ☐    | Hallucinations and why they happen                     | Core     | Know why models make things up                    |
| ☐    | Pre-training vs fine-tuning vs RLHF (overview)         | Next     | Know the stages                                   |
| ☐    | Transformer and attention (conceptual)                 | Later    | Know the idea, no math needed yet                 |
| ☐    | Model types (chat, reasoning, embedding, multimodal)   | Next     | Choose the right model                            |
| ☐    | Open vs closed models, local models (Ollama)           | Next     | Run a small model locally                         |

## B. Using LLM APIs

| Done | Concept                                         | Priority | What you should be able to do |
| ---- | ----------------------------------------------- | -------- | ----------------------------- |
| ☐    | API keys and keeping them safe                  | Core     | Load from env vars            |
| ☐    | Messages format (system, user, assistant roles) | Core     | Build a multi-turn chat       |
| ☐    | Making a basic API call from Python             | Core     | Get a response in code        |
| ☐    | Streaming responses                             | Next     | Stream tokens to a client     |
| ☐    | Managing conversation history                   | Core     | Keep context across turns     |
| ☐    | Token counting and cost estimation              | Next     | Estimate cost per request     |
| ☐    | Rate limits, retries, timeouts, error handling  | Next     | Make calls reliable           |
| ☐    | Caching responses and prompt caching            | Later    | Cut cost and latency          |
| ☐    | Async calls, batching                           | Later    | Handle many requests          |
| ☐    | Multimodal inputs (images, PDFs)                | Next     | Send an image to a model      |

## C. Prompting

| Done | Concept                                        | Priority | What you should be able to do |
| ---- | ---------------------------------------------- | -------- | ----------------------------- |
| ☐    | Clear instructions, role, context, constraints | Core     | Write a good prompt           |
| ☐    | Few-shot examples                              | Core     | Steer output with examples    |
| ☐    | Output format control                          | Core     | Get consistent formats        |
| ☐    | Chain-of-thought / step-by-step reasoning      | Next     | Improve reasoning tasks       |
| ☐    | System prompts and prompt templates            | Core     | Reuse prompts in code         |
| ☐    | Prompt iteration and versioning                | Next     | Test changes methodically     |
| ☐    | Prompt injection and basic defences            | Next     | Know the risk                 |
| ☐    | Prompt chaining (breaking a task into steps)   | Next     | Split complex tasks           |

## D. Structured output and tools

| Done | Concept                                         | Priority | What you should be able to do            |
| ---- | ----------------------------------------------- | -------- | ---------------------------------------- |
| ☐    | Getting JSON output reliably                    | Core     | Parse model output in code               |
| ☐    | Validating output with Pydantic                 | Core     | Reject malformed responses               |
| ☐    | Tool / function calling                         | Next     | Let the model call your Python functions |
| ☐    | Handling tool results and multi-step tool loops | Next     | Run a tool-use loop                      |
| ☐    | Error handling and fallbacks for bad outputs    | Next     | Retry on invalid output                  |
| ☐    | MCP (Model Context Protocol) basics             | Later    | Know what it is                          |

## E. Embeddings and vector search

| Done | Concept                                            | Priority | What you should be able to do       |
| ---- | -------------------------------------------------- | -------- | ----------------------------------- |
| ☐    | What embeddings are                                | Next     | Explain "text as a list of numbers" |
| ☐    | Generating embeddings via an API or local model    | Next     | Embed a sentence in code            |
| ☐    | Cosine similarity (and dot product)                | Next     | Compute similarity by hand          |
| ☐    | Semantic search vs keyword search                  | Next     | Explain when each wins              |
| ☐    | Vector databases (pgvector, Chroma, Qdrant, FAISS) | Next     | Store and query vectors             |
| ☐    | Approximate nearest neighbour (HNSW, IVF)          | Later    | Know the idea                       |
| ☐    | Hybrid search (keyword + vector)                   | Later    | Know the idea                       |
| ☐    | Reranking                                          | Later    | Know the idea                       |

## F. RAG (Retrieval-Augmented Generation)

| Done | Concept                                                   | Priority | What you should be able to do       |
| ---- | --------------------------------------------------------- | -------- | ----------------------------------- |
| ☐    | Why RAG (knowledge beyond training, fewer hallucinations) | Next     | Explain when you need it            |
| ☐    | Document loading and parsing (PDF, text, web)             | Next     | Extract clean text                  |
| ☐    | Chunking strategies (size, overlap, by section)           | Next     | Choose chunk sizes and justify them |
| ☐    | Indexing pipeline (chunk → embed → store)                 | Next     | Build it end to end                 |
| ☐    | Retrieval (top-k, filters, metadata)                      | Next     | Get relevant chunks                 |
| ☐    | Building the prompt with retrieved context                | Next     | Ground the answer in sources        |
| ☐    | Citations / showing sources                               | Next     | Point to where answers came from    |
| ☐    | Handling "I don't know"                                   | Next     | Avoid answering without evidence    |
| ☐    | Query rewriting, multi-query                              | Later    | Improve retrieval                   |
| ☐    | Evaluating RAG (retrieval quality vs answer quality)      | Next     | Measure, not guess                  |
| ☐    | Advanced RAG (graph RAG, agentic RAG)                     | Later    | Know it exists                      |

## G. Agents

| Done | Concept                                       | Priority | What you should be able to do              |
| ---- | --------------------------------------------- | -------- | ------------------------------------------ |
| ☐    | What an agent is (LLM + tools + loop)         | Next     | Explain it simply                          |
| ☐    | Planning, tool selection, observation loop    | Next     | Build a small agent from scratch           |
| ☐    | Memory (short-term vs long-term)              | Next     | Persist context                            |
| ☐    | Guardrails and limiting agent actions         | Next     | Keep agents safe                           |
| ☐    | Frameworks (LangChain, LlamaIndex, LangGraph) | Later    | Try one only _after_ building from scratch |
| ☐    | Multi-agent systems                           | Later    | Know the idea                              |
| ☐    | Human-in-the-loop                             | Later    | Know when to add it                        |

## H. Evaluation and production

| Done | Concept                                        | Priority | What you should be able to do |
| ---- | ---------------------------------------------- | -------- | ----------------------------- |
| ☐    | Manual evaluation with a test set of questions | Next     | Check quality before shipping |
| ☐    | Automatic evaluation (LLM-as-judge, metrics)   | Later    | Know the idea                 |
| ☐    | Logging prompts and responses                  | Next     | Debug in production           |
| ☐    | Cost and latency monitoring                    | Next     | Track spend                   |
| ☐    | Guardrails, content filtering, PII handling    | Later    | Know the risks                |
| ☐    | Serving an LLM feature behind FastAPI          | Next     | Expose it as an API           |
| ☐    | Observability tools (Langfuse, etc.)           | Later    | Know they exist               |

## I. Model customisation (later stage)

| Done | Concept                                        | Priority | What you should be able to do           |
| ---- | ---------------------------------------------- | -------- | --------------------------------------- |
| ☐    | When to prompt vs RAG vs fine-tune             | Next     | Choose the cheapest approach that works |
| ☐    | Fine-tuning, LoRA / QLoRA                      | Later    | Know what it is                         |
| ☐    | Training from scratch                          | Later    | Skip                                    |
| ☐    | Classic ML basics (regression, classification) | Later    | Optional background                     |
| ☐    | Deep learning, PyTorch                         | Later    | Optional background                     |

## Projects

- [ ] CLI chatbot with memory (no framework, just API calls)
- [ ] Structured extractor (messy text → validated JSON)
- [ ] **RAG app:** chat over your own PDFs/notes, built as a FastAPI service with pgvector, with sources shown, deployed
- [ ] A small tool-using agent (e.g. calendar or notes assistant)
