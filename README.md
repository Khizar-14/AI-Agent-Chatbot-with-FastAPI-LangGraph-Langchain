# LangGraph AI Agent

## **Overview**
This project implements an AI chatbot using LangChain and LangGraph, integrating with Groq and OpenAI models. It also includes web search functionality via Tavily. The system is designed as a FastAPI backend with a Streamlit-based UI for user interaction.

**AI Models**: Supports AI models from Groq and OpenAI.

**Web Search**: Integrates Tavily Web Search for enhanced responses.

**Backend**: Built using FastAPI with Pydantic Schema Validation.

**Frontend**: Interactive Streamlit UI for user interaction.

**API Documentation**: Uses Swagger UI for easy exploration of API endpoints.

---

## **Tech Stack**
- **Python** (FastAPI, Streamlit, Requests, Pydantic)
- **LangChain** (Groq, OpenAI, Tavily Integration)
- **LangGraph** (Agent-based AI interaction)
- **Uvicorn** (FastAPI ASGI server)

---

## **Installation**

### **Step 1: Clone the Repository**
```bash
git clone https://github.com/yourusername/langgraph-ai-agent.git
cd langgraph-ai-agent
```

### **Step 2: Create Virtual Environment**
```bash
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```

### **Step 3: Install Dependencies**
```bash
pip install -r requirements.txt
```

---

## **Setting Up API Keys**
Ensure you have valid API keys and set them in your environment:
```bash
export GROQ_API_KEY="your_groq_api_key"
export TAVILY_API_KEY="your_tavily_api_key"
export OPENAI_API_KEY="your_openai_api_key"
```
(Windows PowerShell)
```powershell
$env:GROQ_API_KEY="your_groq_api_key"
$env:TAVILY_API_KEY="your_tavily_api_key"
$env:OPENAI_API_KEY="your_openai_api_key"
```

---

## **Running the Backend Server**

### **Step 1: Start the FastAPI backend**
```bash
uvicorn main:app --host 127.0.0.1 --port 9999 --reload
```

### **Step 2: Access Swagger UI for API documentation**
```
http://127.0.0.1:9999/docs
```

---

## **Running the Streamlit UI**

### **Step 1: Start the Streamlit frontend**
```bash
streamlit run app.py
```

This will open the AI chatbot UI in your browser.

---

## **API Usage**

### **Endpoint: `/chat` (POST)**
- **Description**: Interacts with the AI chatbot.
- **Request Body**:
  ```json
  {
    "model_name": "gpt-4o-mini",
    "model_provider": "OpenAI",
    "system_prompt": "Act as a smart AI assistant",
    "messages": ["Hello, how are you?"],
    "allow_search": true
  }
  ```
- **Response**:
  ```json
  {
    "response": "Hello! How can I assist you today?"
  }
  ```

---

## **Contributing**
Feel free to submit pull requests or raise issues in the repository.

---

## **License**
This project is licensed under the **MIT License**.

---

## **Author**
Developed by **Khizar Hussain** ([GitHub Profile](https://github.com/Khizar-14))

