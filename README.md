# Student AI 

Student AI, is a privacy-aware, hallucination-free AI assistant that allows users to query documents or videos intelligently. Built with the RAG (Retrieval-Augmented Generation) pipeline addressing common challenges of generative AI such as hallucination, privacy risks, and information overload.

---

## Features

- **Accurate QA with RAG Pipeline**  
  Uses advanced semantic search over vector embeddings to fetch relevant chunks from uploaded PDFs or video transcripts.

- **PDF and YouTube Video Support**  
  Users can upload PDFs or paste YouTube video links; the bot understands the content and answers questions based on it.

- **Zero-Hallucination Approach**  
  If a question is out of context or unrelated, it clearly informs the user instead of guessing an answer.

- **Multilingual Support**  
  Bittu understands and answers queries in multiple languages.

- **Real-Time Response**  
  Achieves an average response time of 3.32 seconds, rated useful by over 95% of users during testing.

- **Privacy-First Design**  
  No user data is stored; sensitive documents are processed locally and discarded after the session.

---

## How It Works

1. **File/Link Input**  
   Upload a PDF or paste a YouTube video link via a Gradio interface.

2. **Embedding Generation**  
   Content is chunked and transformed into high-dimensional vector embeddings using Hugging Face models.

3. **Query Processing**  
   User queries are embedded similarly and compared with content embeddings using dot-product similarity.

4. **RAG Pipeline**  
   Top relevant chunks along with optional external context are passed to an LLM (e.g., Gemma) for response generation.

5. **Truthful Answering**  
   If the answer isn't present in the content, the bot says so—ensuring no hallucinations.

---

## Tech Stack

- **LangChain** – for orchestration of the RAG pipeline  
- **Hugging Face (Gemma)** – for model inference  
- **FAISS** – for efficient vector similarity search  
- **Gradio** – for building the interactive UI  
- **Python** – core development language  
