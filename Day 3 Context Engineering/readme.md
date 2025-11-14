# **Day 3 – Context Engineering, Sessions & Memory**

Day 3 focused on building truly stateful AI agents by combining short-term context engineering with long-term memory. This module showed how agents maintain continuity, track structured state, and recall information across multiple conversations — essential for creating personalized and production-ready AI systems.

---

## **Key Learnings**

### 🧠 Context Engineering
- Used **Context Compaction** to assemble optimized context windows for LLM reasoning.
- Structured and managed information dynamically to support coherent multi-turn conversations.

### 💬 Sessions & Conversation History
- Maintained conversation history across multiple turns using the ADK Session system.
- Used events and session data to track dialogue flow and ensure continuity.

### 🗂️ Session State
- Tracked structured values (preferences, flags, variables) across each session.
- Enabled agents to update, reference, and reason over evolving session state.

### 💾 Persistent Storage
- Enabled conversations to survive restarts.
- Stored session data in persistent storage to support long-running or returning-user interactions.

---

## **Long-Term Memory (ADK Memory Service)**

### 🧩 Adding Memory
- Introduced **MemoryService** alongside **SessionService**.
- Both services were passed to the ADK Runner for full state and memory management.

### 📝 Storing Information
```python
await memory_service.add_session_to_memory(session)
