# Building a PDF Q&A System using LLM
This project provides a robust pipeline for processing PDF documents, creating embeddings, and setting up a retrieval-based question-answering (QA) system using a pretrained language model. It is designed for Google Colab and leverages popular libraries such as LangChain, Gradio, Hugging Face, and FAISS.

## Directory Structure
```
├── PDF_LLM.ipynb     # File containing the code for implementing an LLM-based Q&A system
├── utils/
│   └── custom_logger.py         # Custom logger used throughout the process
├── config.json                 # Configuration file for model and settings
└── README.md                   # Project documentation (You are here)
```
## Setup
### Upload the following Files:
- custom_logger.py: Upload to a folder named utils (create the folder if it doesn't exist).
- config.json: Upload it to the current directory of your Google Colab session.


## Project Modules
The primary modules of this project include:
### 1. Document Processing
This module handles the ingestion, segmentation, and embedding of PDF documents to enable efficient querying. It consists of three main classes:
- DataLoadPDF - Loading PDF Data
  Handles loading and reading PDF files.
- DataSplitter - Splitting Document Data
  Manages the splitting of the document data into chunks with overlap if necessary.
- EmbeddingManager - Creating Embeddings
  Manages the creation, loading, and saving of embeddings using the HuggingFaceEmbeddings class and FAISS for efficient vector storage.
 ### 2. Model Loading
  The ModelLoader class is responsible for loading the language model for text generation. You can load the model in either 8-bit precision for memory efficiency or with torch.bfloat16 for faster inference.
  ### 3. Question-Answering System
  The QASystem class sets up a retrieval-based QA system using the previously loaded embeddings and language model. It uses a simple prompt template to generate answers based on context. 
  ### 4. Gradio UI
  This module allows users to upload a PDF, ask questions, and receive answers in real-time.
  - Gradio UI serves as an interface for users to interact with the document processing and QA system.
- Users can first download the PDF with Generative AI interview questions and answers and upload it in the UI, input their queries, and the model will return relevant answers based on the document's content.
- After loading the model and processing the document, run the Gradio app to start interacting with the model via a web interface.

For more detailed instructions on building and training the LLM, refer to this full blog on [How to Build an LLM from Scratch](https://www.projectpro.io/article/how-to-build-an-llm-from-scratch/1064). Alternatively, you may also download the [How to Build an LLM from Scratch PDF](https://www.projectpro.io/free-learning-resources/how-to-build-an-llm-from-scratch-pdf) for a comprehensive guide.

## Special Thanks

Special thanks to [VK Maurya](https://github.com/vk-maurya/PDF-QLM) for his contributions to this project.

