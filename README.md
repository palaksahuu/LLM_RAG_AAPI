 AI-Powered Automation API

 Project Overview
This project is an AI-Powered Automation API
 that dynamically executes system commands based on natural language queries. 
 It utilizes ChromaDB for function retrieval and FastAPI for a scalable API interface.

 Features
- Natural Language Function Execution – Users can trigger system commands using plain English.
- FastAPI Backend – High-performance API for function execution.
- ChromaDB Vector Store – Stores function metadata for retrieval.
- Dynamic Function Execution – Automatically imports and executes functions.
- Extensive Logging – Tracks API requests, errors, and execution time.
- Unit & Integration Testing – Ensures robust functionality.
- Docker Support – Easy deployment in a containerized environment.



 Tech Stack
- Backend: FastAPI
- Vector Store: ChromaDB
- ML Model: SentenceTransformer (`all-MiniLM-L6-v2`)
- logging: Python Logging Module
- Containerization: Docker


 Project Structure

AI-Automation-API
├── automation_functions/       # Core function implementations
│   ├── functions.py            # Function definitions
│   ├── __init__.py             # Module exports
│
├── embeddings/                 # Vector store for function retrieval
│   ├── vector_store.py         # ChromaDB vector database
│
├── api/                        # API layer
│   ├── main.py                 # FastAPI implementation
│   ├── models.py               # API request/response schemas
│   ├── utils.py                # Logging & execution utilities
│
├── tests/                      # Unit & integration tests
│   ├── test_api.py             # API tests
│   ├── test_functions.py       # Function tests
│
├── logs/                       # API logs (generated at runtime)
│
├── db/                         # ChromaDB storage (persistent)
│
├── requirements.txt            # Python dependencies
├── Dockerfile                  # Docker container configuration
├── .gitignore                  # Ignored files/folders
├── README.md                   # Project documentation
```

 Installation & Setup
 Clone the repository**
bash
git clone https://github.com/yourusername/AI-Automation-API.git
cd AI-Automation-API


 Create & Activate Virtual Environment**

python -m venv venv
source venv/bin/activate  
venv\Scripts\activate     


 Install Dependencies**

pip install -r requirements.txt


 Run the API Server

uvicorn api.main:app --host 0.0.0.0 --port 8000 --reload

API will be live at: [http://localhost:8000](http://localhost:8000)

 Usage
Execute Automation Commands**
 Example Request:

{
  "prompt": "Open Chrome"
}


{
  "status": "success",
  "function": "open_chrome",
  "result": null,
  "execution_time_ms": 125.7
}



