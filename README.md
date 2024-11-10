# PromptQuest
 PromptQuest is an AI-powered platform for generating essays and answering questions using large language models. Built with FastAPI and LangChain, it offers fast, accurate responses based on custom prompts and document retrieval. Ideal for academic, business, or research use, PromptQuest delivers real-time, context-aware results.

Features
Essay Generation: Generate essays based on any topic.
Policy Q&A: Answer questions based on provided documents (e.g., company policies).
Custom Prompts: Tailor prompts for different use cases using LangChain.
Document Retrieval: Efficiently search and retrieve information from large text documents using Chroma and Ollama embeddings.
Interactive UI: Streamlit interface for seamless interaction.
Technologies Used
FastAPI: Web framework for building the backend API.
LangChain: Framework for creating advanced language models and prompts.
Ollama: LLM integration for text generation and document-based retrieval.
Chroma: Vector store for efficient document embedding and retrieval.
Streamlit: Frontend interface for user interaction.
Uvicorn: ASGI server for running the FastAPI app.
dotenv: For managing environment variables.

Installation & Setup
1. Clone the Repository
bash
Copy code
git clone https://github.com/bhxvxshh/PromptQuest.git
cd PromptQuest
2. Create a Virtual Environment
bash
Copy code
python -m venv venv
source venv/bin/activate   # On Windows, use `venv\Scripts\activate`
3. Install Dependencies
bash
Copy code
pip install -r requirements.txt
4. Set Up Environment Variables
Create a .env file in the root of the project with the following variables:

env
Copy code
LANGCHAIN_API_KEY=your_langchain_api_key
5. Run the Backend API
bash
Copy code
uvicorn app:app --reload
6. Run the Streamlit Frontend
bash
Copy code
streamlit run client.py
How It Works
FastAPI Backend: The backend exposes two primary routes:

/essay: Takes a topic as input and generates a 100-word essay.
/gemma2:2b: Handles policy-related queries and retrieves relevant answers from documents.
Streamlit Frontend: The user enters a topic for essay generation or asks a policy-related question. The frontend sends the input to the backend API, receives the response, and displays it.

Document-Based Querying: When users ask policy questions, the backend uses Chroma to retrieve relevant information from provided documents (e.g., policies) and returns the answer.
License
This project is licensed under the MIT License - see the LICENSE file for details.

Acknowledgements
LangChain and Ollama for providing powerful tools for building language models and document retrieval.
Streamlit for easy-to-use frontend development.
Uvicorn for serving the FastAPI application.
