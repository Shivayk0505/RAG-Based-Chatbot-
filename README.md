# RAG-Based-Chatbot.
This project involves developing a Retrieval-Augmented Generation (RAG) system designed to extract relevant information from YouTube transcripts and PDF documents. The system aims to generate accurate, context-aware responses to user queries by combining retrieval techniques with advanced natural language generation.

METHODOLOGY 
1. Data Ingestion - Extract transcripts from YouTube videos using `youtube_transcript_api`. - Extract text from PDF files using `pdfplumber`. 
2. Summarization - Use HuggingFace’s `pipeline('summarization')` to condense long transcripts into short 
abstracts. 
3. Text Processing: - Sentence tokenization (nltk, spacy) - Embedding generation (all-MiniLM-L6-v2) 
4.CClustering: - Similarity thresholding (cosine similarity ≥ 0.7) - Union-Find algorithm for dynamic grouping 
4. Embedding & Vector Storage - Generate embeddings using `sentence-transformers` (MiniLM). - Store vectors in a FAISS index for fast similarity search. 
5. Retrieval & Generation - Retrieve top relevant clusters based on query similarity. - Combine context with user query and generate answers using `Mistral-7B-Instruct`. 
TECHNOLOGIES USED - Python (Core language) - HuggingFace Transformers (Summarization & LLMs) - SentenceTransformers (Embeddings) - Mistral-7B-Instruct (LLM) 
