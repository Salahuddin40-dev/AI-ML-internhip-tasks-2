#  Context-Aware Chatbot Using LangChain

This project builds an intelligent chatbot that can remember previous conversation context and retrieve information from external documents using **LangChain**, **FAISS**, and **OpenAI** models. The chatbot is deployed using **Streamlit** for easy web-based interaction.

---

## Objective

To develop a chatbot that:
- Understands and remembers user conversations
- Searches and retrieves answers from a custom document base
- Provides context-aware responses using LLMs (e.g. ChatGPT)

---

## Dataset / Knowledge Base

You can use:
- `.txt` or `.md` files (e.g., Wikipedia articles)
- Internal docs or notes
- Any text-based knowledge source

In this project, we use a file named `my_data.txt`.

---

## Technologies Used

- [LangChain](https://github.com/langchain-ai/langchain)
- [OpenAI GPT models](https://platform.openai.com/)
- [FAISS](https://github.com/facebookresearch/faiss) for vector search
- [Streamlit](https://streamlit.io/) for deployment
- `langchain-community` modules for embeddings and document loading

---

## Installation

Install the required Python packages:

```bash
pip install -U langchain langchain-community openai faiss-cpu streamlit
```

---

##  OpenAI API Key

Set your OpenAI API Key:

```python
import os
os.environ["OPENAI_API_KEY"] = "your-api-key-here"
```

You can also use environment variables or `.env` files to load the key securely.

---

##  How It Works

1. Loads your documents from a `.txt` file  
2. Converts text to vector embeddings using OpenAI  
3. Stores vectors in FAISS for fast search  
4. Uses LangChain’s `ConversationalRetrievalChain` with memory  
5. Chatbot answers based on:
   - Chat history
   - Retrieved relevant info from documents

---

##  Project Structure

```
context_chatbot/
├── my_data.txt            # Your custom knowledge base
├── app.py                 # Streamlit chatbot app
├── chatbot_notebook.ipynb # Jupyter notebook version
```

---

##  Running the Streamlit App

After setting up the environment and OpenAI key:

```bash
streamlit run app.py
```

This will launch a local web interface where you can chat with the bot.

---

##  Example

**Input:**
```
Who wrote the Constitution of Pakistan?
```

**Bot Output:**
```
The Constitution of Pakistan was drafted by the National Assembly under the leadership of Zulfikar Ali Bhutto in 1973.
```

*(Assuming this info is in `my_data.txt`)*

---

##  Skills Gained

- LangChain conversational agents  
- Embedding and vector search with FAISS  
- Retrieval-Augmented Generation (RAG)  
- Streamlit app deployment  
- Chatbot with memory and context

---


