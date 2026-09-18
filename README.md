# Document Q&A with Citations using RAG

## Project Overview
A Retrieval-Augmented Generation (RAG) system that answers questions from a 110-page PDF corpus and provides the source page passages used to generate each answer.

## Technologies
- Python
- Google Colab
- Sentence Transformers
- FAISS
- Hugging Face Transformers
- LangChain Text Splitters
- PyPDF

## Dataset
World Bank Digital Progress and Trends Report 2025: Strengthening AI Foundations.

The corpus contains 110 pages.

## System Pipeline

PDF
↓
Text Extraction
↓
Chunking
↓
Embeddings
↓
FAISS Vector Database
↓
Similarity Retrieval
↓
LLM Answer Generation
↓
Answer + Source Page Citations

## Chunking Strategies

### Strategy 1: Fixed-size Chunking
- Chunk size: 1000 characters
- Overlap: 100 characters

### Strategy 2: Recursive Character Chunking
- Chunk size: 1000 characters
- Overlap: 100 characters

## Evaluation

Six questions were tested using both strategies.

The Recursive strategy produced lower retrieval distances for all six test questions in our experiment.

Average retrieval distance:

- Fixed-size: 1.4543
- Recursive: 0.7993

These results indicate that the Recursive strategy produced closer embedding matches for the tested questions. Passage-level inspection was also used to check whether retrieved content was relevant.

## Key Features

- Document-based question answering
- Semantic retrieval
- Source/page citations
- Two chunking strategies
- Retrieval evaluation
- "I don't know" response for insufficiently relevant retrieval

## How to Run

1. Open the Google Colab notebook.
2. Upload the PDF.
3. Install the required libraries.
4. Extract the PDF text.
5. Run the chunking and embedding cells.
6. Build the FAISS index.
7. Ask questions using the Q&A function.

## Author

Saniya Shaikh
