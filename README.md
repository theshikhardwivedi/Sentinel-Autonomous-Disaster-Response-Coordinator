# 🚨 Sentinel: Autonomous Multi-Agent Disaster Response Coordinator

### **A Hierarchical Multi-Tool System for Real-Time Crisis Management**

Sentinel is a **Commander-Tool system** designed to drastically accelerate decision-making and resource deployment during catastrophic events. It ensures **safety-optimized deployment** through rigorous conditional logic and validation.

---

> ### **The Core Mission: Eliminating the Fog of War**
> **Sentinel** is an **Autonomous Multi-Agent System** that acts as an AI Crisis Commander. By leveraging **Gemini's Multimodal Intelligence** and **Conditional Logic**, it transforms chaotic, unstructured input into an **actionable, safety-optimized Incident Command Report (ICR)**. Its core safety feature is **Conditional Rerouting** based on real-time visual assessment.

### 🌍 The Problem: The Golden Hour Challenge

In a disaster, every minute counts, but centralized human command centers face significant delays due to data chaos, slow visual assessment, and resource mismatches.

### 💡 The Solution: Actionable, Optimized Orders

**Sentinel's Promise:** To drastically reduce response time and save lives by automating the synthesis of chaotic, multimodal data into **actionable, life-saving rescue orders.**

-----

## 🚀 Key Features (Agent Design Kit Principles)

* **Model Stability:** Uses the highly reliable **Gemini 2.5 Flash** model for high-throughput, mission-critical operations.
* **Multimodal Triage:** Processes raw field data (text, images) using specialized tools, integrating **Gemini Vision** for rapid assessment of hazards (e.g., road blockages).
* **Long-Term Memory (RAG):** Integrates **FAISS vector search** with **Sentence Transformers** to retrieve local operational unit data (equipment, personnel) for optimized logistics planning.
* **Conditional Orchestration (Safety Guardrail):** The **CommanderAgent** applies critical safety rules, executing an automatic **REROUTE** from ground to air deployment if visual hazards are confirmed (T-1 scenario).
* **Autonomous Evaluation (Observability):** Includes a dedicated **Audit Tool** to perform a critical self-assessment of the final report for safety and efficiency, closing the **Feedback Loop**.
* **Structured Output (Pydantic):** Generates a formal, verifiable JSON-based report, ensuring **type safety** and reliable data exchange.

-----

## 🧠 Architectural Design

Sentinel employs a **hierarchical, specialized workflow** with a single Commander orchestrating three core tools, ensuring high reliability and clear separation of concerns, adhering to the principles of the **Agent Design Kit (ADK)**.

### **Commander and Tool Constellation**

| Functional Agent (Tool) | Role | Core Function | ADK Principle |
| :--- | :--- | :--- | :--- |
| **🎖 CommanderAgent** | Strategic Orchestration | Synthesizes data and applies **Conditional Logic** to decide the final, safest deployment strategy. | **Hierarchical Orchestration** |
| **👁 Vision Tool** | Multimodal Assessment | Analyzes input images to confirm infrastructure accessibility status (*Passable* or *Blocked*). | **Multimodal Intelligence** |
| **📦 Logistics Tool** | RAG Allocation | Queries a vector store (FAISS) to match complex needs to the optimal unit capability. | **Long-Term Memory (RAG)** |
| **⚖ Audit Tool** | Observability & Evaluation | Critically reviews the final report for safety, efficiency, and resource gaps. | **Autonomous Evaluation** |

### **Architecture Diagram**

A visual representation of the agent workflow and data pipeline.

<img width="1024" height="1024" alt="sentinel_architecture" src="https://github.com/user-attachments/assets/5077820f-2927-4914-b8b4-f77637751611" />

-----

## ✅ Validation & Robustness Proof

The system's integrity is proven through three validation scenarios, ensuring the Commander's **Conditional Routing** logic functions correctly across success and failure modes.

| ID | Scenario Goal | Input Challenge | Logic Validated |
| :--- | :--- | :--- | :--- |
| **T-1** | **Safety Override Test** | Road is visually **blocked**. Logistics recommends Ground Unit. | **Commander overrides** the plan and **reroutes to Air Support**, proving the safety guardrail. |
| **T-2** | **RAG Precision Test** | Road is **clear**. Specialized need: water purification. | **Logistics Tool** finds the precise `Water Logistics Unit`. Full success path. |
| **T-3** | **Resource Gap & Audit** | Need is complex. RAG has no unit for 'heavy equipment'. | **Audit Tool logs** the critical resource gap, proving **Observability** of resource limitations. |

-----

## ⚙️ Getting Started

These instructions will get you a copy of the project up and running on your local machine or in a Kaggle environment for development and testing.

### **Prerequisites**

You will need the following installed:

* Python 3.10+
* A valid **Google Gemini API Key** (from Google AI Studio)
* The key must be set as an environment variable named `GOOGLE_API_KEY`.

### **Installation**

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/theshikhardwivedi/Sentinel-Autonomous-Disaster-Response-Coordinator.git
    cd Sentinel-Autonomous-Disaster-Response-Coordinator
    ```

2.  **Install dependencies:**
    The project relies on `google-generativeai` for the LLM, `sentence-transformers` for embeddings, and `faiss-cpu` for vector search.
    ```bash
    pip install -r requirements.txt
    ```

*(Note: Ensure your `requirements.txt` file includes all necessary libraries: `google-generativeai`, `pandas`, `numpy`, `sentence-transformers`, `faiss-cpu`, etc.)*

### **Usage**

The entire system is executed through the main Jupyter Notebook.

1.  **Setup Environment:** Ensure your `GOOGLE_API_KEY` is set.
2.  **Open Notebook:** Open `/notebook/sentinel-ai-disaster-response-coordinator.ipynb`.
3.  **Run Cells Sequentially:** Execute the cells from top to bottom. The notebook demonstrates the full flow, from data ingestion to the final generated **Incident Command Report**.

-----

## 🤝 Contributing

Contributions are what make the open-source community an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'feat: Add AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

-----

## 👤 Author

**Shikhar Dwivedi**

* Kaggle: [@theshikhardwivedi](https://www.kaggle.com/code/theshikhardwivedi/sentinel-autonomous-disaster-response-coordinator)
* GitHub: [@theshikhardwivedi](https://github.com/theshikhardwivedi/Sentinel-Autonomous-Disaster-Response-Coordinator.git)
