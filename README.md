# 🌍 Sentinel: AI Disaster Response Coordinator


### **A Multi-Agent System for Real-Time Crisis Management**


[](https://www.python.org/)
[](https://www.google.com/search?q=https://ai.google/gemini-api)
[](https://www.kaggle.com/code/theshikhardwivedi/sentinel-ai-disaster-response-coordinator)

Sentinel is a **five-agent, collaborative system** designed to drastically accelerate decision-making and resource deployment during catastrophic events. By leveraging the **multimodal** and **function-calling** capabilities of **Gemini 1.5 Flash**, it transforms chaotic, unstructured input (text, images) into a single, comprehensive, and actionable **Incident Command Report (ICR)** in under a minute.

-----

## 🚀 Key Features

  * **Multimodal Triage:** Processes raw field data (social media, sensor readings, images) using specialized agents for swift categorization.
  * **Gemini Vision:** Utilizes Gemini's vision capability for rapid, accurate assessment of infrastructure damage (e.g., road blockages, structural integrity) from images.
  * **Retrieval-Augmented Generation (RAG):** Integrates **FAISS vector search** with **Sentence Transformers** to retrieve local operational unit data (equipment, personnel) for optimized logistics planning.
  * **Structured Output:** Generates a formal, five-point Incident Command Report (ICR) that synthesizes all information into a deployment directive.
  * **Quality Assurance:** Includes a dedicated **EvaluatorAgent** to perform a critical self-assessment of the final report for accuracy and clarity.

-----

## 🧠 Architectural Design

Sentinel employs a sequential, specialized workflow to ensure high reliability and clear separation of concerns, adhering to the principles of the Agent Design Kit (ADK).

The system is composed of five specialized agents:

| Agent Name | Role | Core Function | Inputs |
| :--- | :--- | :--- | :--- |
| **1. SignalAgent** | Triage & Classification | Analyzes raw text input and extracts key entities (location, needs, severity) into JSON. | Raw Text |
| **2. VisionAgent** | Visual Assessment | Analyzes input images to confirm infrastructure damage and accessibility status. | Image, Triage Data |
| **3. LogisticsAgent** | RAG & Deployment | Queries a vector store (FAISS) of operational units and drafts the resource deployment plan. | Triage Data, Vision Summary |
| **4. CommanderAgent** | Synthesis & Report | Synthesizes all data (Triage, Vision, Logistics) into the final Incident Command Report (ICR). | All Agent Outputs |
| **5. EvaluatorAgent** | Quality Assurance | Critically reviews the ICR against the original input for accuracy and clarity. | Original Input, Final ICR |

### **Architecture Diagram**

A visual representation of the agent workflow and data pipeline.

[Image of a detailed multi-agent system architecture diagram]

-----

## ⚙️ Getting Started

These instructions will get you a copy of the project up and running on your local machine or in a Kaggle environment for development and testing.

### **Prerequisites**

You will need the following installed:

  * Python 3.10+
  * A valid **Google Gemini API Key** (from Google AI Studio)
  * The key must be set as an environment variable named `GEMINI_API_KEY` (or `GOOGLE_API_KEY` if using Kaggle Secrets).

### **Installation**

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/theshikhardwivedi/Sentinel-AI-Disaster-Response-Coordinator.git
    cd sentinel-ai-disaster-response-coordinator
    ```

2.  **Install dependencies:**
    The project relies on `google-genai` for the LLM, `sentence-transformers` for embeddings, and `faiss-cpu` for vector search.

    ```bash
    pip install -r requirements.txt
    ```

    *(Note: You will need to create a `requirements.txt` file containing all the necessary libraries: `google-genai`, `pandas`, `numpy`, `sentence-transformers`, `faiss-cpu`, etc.)*

### **Usage**

The entire system is executed through the main Jupyter Notebook.

1.  **Setup Environment:** Ensure your `GOOGLE_API_KEY` is set.
2.  **Open Notebook:** Open `sentinel-ai-disaster-response-coordinator.ipynb`.
3.  **Run Cells Sequentially:** Execute the cells from top to bottom. The notebook demonstrates the full flow, from data ingestion to the final generated **Incident Command Report**.

-----

## 🤝 Contributing

Contributions are what make the open-source community an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'feat: Add AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

-----

## 👤 Author

**Shikhar Dwivedi**

  * Kaggle: [@theshikhardwivedi](https://www.kaggle.com/code/theshikhardwivedi/sentinel-ai-disaster-response-coordinator)
  * GitHub: [@theshikhardwivedi](https://github.com/theshikhardwivedi/Sentinel-AI-Disaster-Response-Coordinator.git)
