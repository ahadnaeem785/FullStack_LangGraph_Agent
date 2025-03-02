# **LangGraph AI Chatbot (FastAPI + Streamlit)**

## **📌 Overview**
This project is a **full-stack AI chatbot system** built using **FastAPI (backend) and Streamlit (frontend)**. It allows users to **define AI agents**, select a model provider (**Groq or OpenAI**), interact with a chatbot, and optionally allow web searches to enhance responses.

---

## **🚀 Features**
- **FastAPI Backend:** Handles AI chatbot requests and model interactions.
- **Streamlit Frontend:** Provides an interactive UI for user queries.
- **Multiple Model Providers:** Supports **Groq** and **OpenAI** models.
- **Customizable System Prompt:** Users can define agent behavior.
- **Web Search Integration:** Optionally enables external web searches.
- **Conversational Flow:** AI agent processes user queries dynamically.

---

## **🛠️ Technologies Used**
- **FastAPI** - Backend API framework
- **Streamlit** - Frontend UI framework
- **Pydantic** - API request validation
- **Uvicorn** - ASGI server to run FastAPI
- **Requests** - Connects Streamlit frontend to FastAPI backend
- **Groq API & OpenAI API** - AI model providers
- **LangChain & LangGraph** - AI agent framework
- **Tavily API** - Web search integration

---

## **📁 Project Structure**
```
App/
│── .venv/                      # Virtual environment (if used)
│── src/
│   └── my_package/
│       ├── __init__.py          # Package initialization
│       ├── ai_agent.py          # AI agent logic
│       ├── backend.py           # FastAPI backend (API)
│       ├── frontend.py          # Streamlit frontend (UI)
│── .env                         # API keys and environment variables
│── pyproject.toml               # Dependency & script configurations (uv, project settings)
│── README.md                    # Project documentation
│── uv.lock                      # Dependency lock file for uv package manager
```

---

## **📌 Installation & Setup**

### **1️⃣ Clone the Repository**
```bash
git clone https://github.com/your-repo/AI-Chatbot.git
cd AI-Chatbot
```

### **2️⃣ Install Dependencies**
Use `uv` (or `pip`) to install dependencies.
```bash
uv venv .venv  # Create virtual environment
uv install  # Install dependencies
```

### **3️⃣ Set Up Environment Variables**
Create a `.env` file and add your API keys:
```
GROQ_API_KEY=your_groq_api_key
OPENAI_API_KEY=your_openai_api_key
TAVILY_API_KEY=your_tavily_api_key
```

---

## **🚀 Running the Project**

### **Start the FastAPI Backend**
```bash
uv run back_end
```
This starts the backend at **`http://127.0.0.1:9999`**.

### **Start the Streamlit Frontend**
```bash
uv run front_end
```
This launches the UI at **`http://localhost:8501`**.

---

## **📌 Usage**
1. **Define AI Agent** - Enter a system prompt to instruct the agent.
2. **Select Provider** - Choose between **Groq** or **OpenAI** models.
3. **Choose AI Model** - Select an AI model for generating responses.
4. **Enable Web Search** (optional) - Allow AI to search the web.
5. **Ask a Question** - Enter a query and receive an AI-generated response.

---

## **📌 API Endpoints (FastAPI)**
### **1️⃣ `POST /chat`**
Handles chatbot interactions.
#### **Request Body:**
```json
{
    "model_name": "gpt-4o-mini",
    "model_provider": "OpenAI",
    "system_prompt": "Act as an AI chatbot who is smart and friendly",
    "messages": ["Hello, how are you?"],
    "allow_search": false
}
```
#### **Response:**
```json
{
    "response": "I am doing great! How can I help you today?"
}
```

---

## **🔹 Customization & Enhancements**
- Add **memory functionality** to retain previous conversations.
- Implement **long-term memory** for enhanced personalization.
- Integrate **additional AI models** beyond Groq and OpenAI.
- Add **user authentication** for personalized experiences.

---

## **📌 Contributors**
- **Muhammad Ahad** (Project Lead)
- Open for contributions!

---

## **📌 License**
This project is licensed under the **MIT License**.

---

## **📌 Support & Contact**
For issues or feature requests, please open an issue on GitHub or contact **[your email]**.

🚀 **Happy Coding!**

