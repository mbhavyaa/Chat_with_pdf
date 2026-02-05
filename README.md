# Conversational PDF RAG 

A conversational Retrieval-Augmented Generation (RAG) application that allows users to upload PDF documents and chat with their content. The system supports multi-turn conversations with chat history awareness, enabling accurate follow-up questions and context-aware answers.

---

##  Features

-  Upload and process multiple PDF files  
-  Semantic search using embeddings and vector database  
-  Conversational Q&A with chat history  
-  History-aware question reformulation  
-  Fast LLM inference using Groq  
-  Answers grounded strictly in PDF content  

---

##  How It Works (High Level)

1. PDFs are loaded and split into overlapping text chunks  
2. Each chunk is converted into embeddings using a HuggingFace model  
3. Embeddings are stored in a Chroma vector database  
4. User queries are embedded and matched via semantic similarity  
5. Relevant chunks are retrieved and passed to the LLM  
6. Chat history is used to rewrite follow-up questions for better retrieval  
7. The LLM generates concise, context-grounded answers  

---

##  Tech Stack

- **Frontend:** Streamlit  
- **LLM:** Groq (ChatGroq)  
- **Embeddings:** HuggingFace (`all-MiniLM-L6-v2`)  
- **Vector Store:** ChromaDB  
- **Framework:** LangChain  
- **Document Loader:** PyPDFLoader  

---

##  Installation & Setup

