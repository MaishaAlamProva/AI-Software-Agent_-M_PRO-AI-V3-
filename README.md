# M_PRO AI V3 — Professional Coding Architect

**M_PRO AI V3** is an elite AI Software Architect designed to enforce project standards through long-term memory. Using a Retrieval-Augmented Generation (RAG) approach, it reviews code against specific, persistent project rules stored in a vector database.

---

## 🚀 Features

*   **Persistent Project Memory**: Uses **FAISS** vector storage to remember your unique coding standards (e.g., "Always use FastAPI," "Strict snake_case").
*   **Intelligent Code Review**: Leverages **Llama 3.3 70B** for lightning-fast, production-grade architectural feedback.
*   **Rich Terminal UI**: Powered by the `rich` library for beautiful, structured, and professional console output.
*   **Contextual Awareness**: Automatically retrieves relevant project rules based on your current input.

---

## 🛠️ Tech Stack

*   **LLM**: Groq (Llama-3.3-70b-versatile)
*   **Orchestration**: LangChain
*   **Vector Database**: FAISS (Facebook AI Similarity Search)
*   **Embeddings**: HuggingFace (`all-MiniLM-L6-v2`)
*   **UI**: Rich

---

## 📋 Usage

Run the `AI Software Agent.ipynb` notebook or the Python script.

### **Chat Commands**
*   **General Queries**: Simply paste code for an architectural review.
*   **`remember: <text>`**: Store a new rule into the long-term vector memory.
*   **`exit`**: End the session.

### **Example Interaction**
```text
You: remember: Database layer must use repository pattern.
M_PRO AI: [MEMORY SAVED]

You: Review this code: 
    @app.route("/data")
    def get_data():
        return db.query("SELECT * FROM table")

M_PRO AI: [AI REVIEW]
- Issue: Direct database query found.
- Suggestion: Refactor to use the Repository Pattern as per project standards.
