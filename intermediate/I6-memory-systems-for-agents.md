# Course I6: Memory Systems for Agents

> **Give agents the ability to remember** — Implement short-term, long-term, episodic, and entity memory systems using vector databases and advanced recall strategies.

### Goal: Build agents with robust memory systems that persist across sessions

---

## I6.1 Types of Memory — Short-Term, Long-Term, Episodic, Semantic
- Why agents need memory — Without memory, every conversation starts from zero
- Short-term memory — The current conversation, working context
- Long-term memory — Persistent knowledge that survives across sessions
- Episodic memory — Remembering specific past events and interactions
- Semantic memory — General facts and knowledge accumulated over time
- Procedural memory — Learned skills and workflows (how to do things)
- The memory architecture — How different memory types work together
- Human memory as inspiration — Drawing parallels to cognitive science

## I6.2 Conversation Memory — Buffer, Summary, Sliding Window (Lab)
- Buffer memory — Storing the full conversation history verbatim
- Token limits — When full history exceeds the context window
- Summary memory — LLM summarizes older messages to save tokens
- Sliding window — Keeping only the last N message pairs
- Buffer + summary hybrid — Recent messages verbatim, older ones summarized
- Token-aware truncation — Cutting history based on token count, not message count
- Memory serialization — Saving and loading conversation state
- Choosing the right strategy — Based on conversation length and context window size

## I6.3 Persistent Memory with Vector Databases (Lab)
- Why persistent memory — Remembering across sessions, days, weeks
- Memory as embeddings — Converting memories into searchable vectors
- Storing memories — Adding conversation summaries, facts, and events to a vector store
- Retrieving memories — Similarity search to find relevant past context
- Memory injection — Adding retrieved memories into the system prompt
- ChromaDB for memory — Collections, metadata filtering, persistence
- Memory lifecycle — Creating, updating, and archiving memories
- Scalability — Managing large memory stores efficiently

## I6.4 Entity Memory — Tracking Facts About People, Places, Things (Lab)
- What is entity memory — Structured knowledge about specific entities
- Entity extraction — Using LLMs to identify entities in conversation
- Entity stores — Key-value stores for entity attributes
- Entity updates — Updating facts as new information arrives
- Conflict resolution — Handling contradictory information about entities
- Entity relationships — Tracking connections between entities
- Use cases — CRM-like agents, personal assistants, research agents

## I6.5 Memory Injection Strategies — When and How to Recall
- The recall problem — When should the agent look up memories
- Always-on recall — Search memory for every user message
- Trigger-based recall — Only recall when certain keywords or patterns appear
- LLM-driven recall — Let the agent decide when to search memory
- Relevance scoring — Filtering out low-relevance memories
- Memory context placement — Where in the prompt to inject memories (system, before user message)
- Memory quantity — How many memories to inject (too few vs too many)
- Recency weighting — Prioritizing recent memories over old ones

## I6.6 Memory Management — Forgetting, Updating, Compressing (Lab)
- The memory bloat problem — Unlimited memory becomes noisy and expensive
- Forgetting strategies — TTL (time-to-live), access-based decay, explicit deletion
- Memory consolidation — Merging related memories into summaries
- Memory compression — Distilling verbose memories into concise facts
- Importance scoring — Ranking memories by significance
- Memory pruning — Periodically removing low-value memories
- Privacy and compliance — Deleting memories on user request (GDPR right to be forgotten)
- Memory versioning — Tracking how memories change over time
