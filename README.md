# Basic_Chat_bot
🤖 AI Chatbot with Llama 3, FastAPI & Streamlit
A full-stack AI-powered chatbot that uses Meta’s Llama-3.3-70B-Instruct via the Together API, served through a FastAPI backend, and interacted with via a Streamlit frontend.

Perfect for experimenting with large language models locally or deploying as a lightweight AI assistant.

✨ Features
LLM Integration: Uses meta-llama/Llama-3.3-70B-Instruct-Turbo-Free via Together AI.
FastAPI Backend: RESTful API endpoints for chat and LLM queries.
Streamlit UI: Simple, interactive web interface for chatting with the model.
Session History: Remembers conversation history during your session.
Scalable Design: Easy to extend with new models, endpoints, or UI components.

📦 Tech Stack
Backend: FastAPI (Python)
Frontend: Streamlit (Python)
LLM Provider: Together AI
Environment Management: python-dotenv
API Client: together Python SDK
🚀 Getting Started

1. Prerequisites
Make sure you have:
Python 3.9+
pip or poetry
Together AI API key (set as TOGETHER_API_KEY in .env)
👉 Get your free API key from Together AI
2. Clone & Install
bash
git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name

# Create virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install together python-dotenv fastapi uvicorn streamlit requests
git clone https://github.com/mahgoubhany/Basic_Chat_bot
cd your-repo-name

# Create virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install together python-dotenv fastapi uvicorn streamlit requests
3. Setup Environment
Create a .env file in the root directory:

TOGETHER_API_KEY=your_together_api_key_here

4. Run the Backend (FastAPI)
uvicorn main:app --reload --host 0.0.0.0 --port 8000

API Docs: Visit http://localhost:8000/docs to explore endpoints. 

5. Run the Frontend (Streamlit)
In a new terminal:
bash
streamlit run main.py
Chat UI: Visit http://localhost:8501 

🧭 API Endpoints (FastAPI)
GET
/
Root endpoint — returns “hello world”
GET
/hello/{name}
Greets user by name

POST
/chat/
Echoes user message (for testing)

POST
/llm/
Sends query to Llama 3 and returns AI response

Example /llm/ request body:

json
{
  "query": "What is the capital of France?"
}
💬 Example Chat
User: Best linux distro for daily use in brief
Bot: Ubuntu — user-friendly, great hardware support, large community, ideal for beginners and daily drivers.

🛠️ Project Structure

├── main.py              # FastAPI + Streamlit (combined for simplicity)
├── .env                 # Environment variables
├── README.md            # You are here!
└── requirements.txt     # Dependencies (optional)
💡 Note: In production, consider separating backend and frontend into different files/modules. 

📄 License
MIT — Feel free to use, modify, and distribute.

🙌 Acknowledgements
Together AI for free access to powerful LLMs
FastAPI for the blazing-fast backend
Streamlit for the effortless frontend
Llama 3 by Meta — the brain behind the bot
📬 Feedback & Contributions
Found a bug? Want to add a feature? Open an issue or submit a PR!


