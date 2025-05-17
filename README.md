🤖 Customer Support System using RAG
A customer support chatbot powered by Retrieval-Augmented Generation (RAG) that leverages custom data and LLMs to deliver accurate, context-rich responses for product-related queries.

📋 Project Overview
This project implements an end-to-end RAG-based system for customer support. It includes data scraping, vector-based retrieval, and dynamic response generation using LLMs with customized prompts.

✨ Features
🔍 Natural language question handling

🔗 Retrieval-Augmented response generation

🧠 Custom prompt design for contextual accuracy

🔧 Configurable via YAML settings

🧹 Modular pipeline for scraping, embedding, and serving

🛠️ Tech Stack
Python: Core programming language

FastAPI: API framework (via main.py)

Transformers: LLM and embeddings

Pandas: Data manipulation

YAML: Configuration management

LangChain : Prompt chaining and agent tools

Conda/venv: Environment management

DataBase:AstraDB

📁 Project Structure
CUSTOMER_SUPPORT_SYSTEM/
├── main.py                         # API entry point
├── test.py                         # Test script
├── requirements.txt                # Python dependencies
├── setup.py                        # Package setup (if needed)
├── .env                            # Environment variables (API keys etc.)
├── config/
│   ├── config.yaml                 # Configurations (API keys, paths)
│   └── config_loader.py            # Loader for config
├── prompt_library/
│   └── prompt.py                   # Prompt design and templates
├── data_collection_pipeline/
│   └── flipkart_scrapper.py       # Web scraper for product reviews
├── retriever/
│   └── retrieval.py               # Vector search and document retrieval
├── utils/
│   └── model_loader.py            # Load LLM and embeddings
└── README.md                       # Project documentation

🚀 Setup & Installation
🔧 Prerequisites
Python 3.9+

Conda or virtual environment

API keys for LLM providers (e.g., Google AI Studio, Groq)

🔨 Installation Steps
# Clone the repository
git clone https://github.com/yourusername/customer-support-system.git
cd customer-support-system

# Create and activate virtual environment
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

🔐 Environment Variables
Create a .env file and add:

GOOGLE_API_KEY=your_google_key
GROQ_API_KEY=your_groq_key
ATRA_DB_API_ENDPOINT=your_Astra_db_end_point_key
ASTRA_DB_APPLICATION_TOKEN=Astra_db_application_token_key
ASTRA_DB_KEYSPAC=Astra_db_keyspace_key

🏃‍♂️ Running the App
Start the API server using:
uvicorn main:app --reload

Then open your browser and go to: http://localhost:8000/docs

🔄 Workflow
Scraping: Collect product reviews using the Flipkart dataset

Embedding: Convert documents to vector space

Retrieval: Fetch relevant chunks using vector similarity

Prompting: Use predefined prompt templates to generate answers

Response: Serve the response via API


🤝 Contribution
Want to improve this project?

Fork the repo

Create a new branch (feature-x)

Make changes and commit

Open a Pull Request



└── customer_support_rag/
    ├── README.md
    ├── main.py                    # FastAPI application entry point
    ├── pyproject.toml             # Project metadata and dependencies
    ├── requirements.txt           # Project dependencies
    ├── uv.lock                    # UV lock file
    ├── .python-version            # Python version specification
    ├── config/                    # Configuration files
    │   └── config.yaml
    ├── data/                      # Data files
    │   └── flipkart_product_review.csv
    ├── logs/                      # Log files
    ├── notebook/                  # Jupyter notebooks for experimentation
    │   └── customer_service_bot.ipynb
    ├── rag/                       # Core RAG modules
    │   ├── __init__.py
    │   ├── constant/
    │   ├── data_ingestion/
    │   ├── exception/
    │   ├── logging/
    │   ├── model_loaders/
    │   ├── model_with_memory/
    │   ├── prompts/
    │   └── retriever/
    ├── static/                    # Static assets for web interface
    │   └── style.css
    ├── templates/                 # HTML templates
    │   └── chat.html
    └── utils/                     # Utility functions
        ├── __init__.py
        └── config.py
