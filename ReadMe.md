# Smart Cultural Storyteller 

**An Agentic Geospatial Narrative Engine**

This project is an interactive, map-based AI system that transforms static geographical coordinates into immersive cultural narratives. It uses a **Hybrid Agentic Architecture** combining real-time Wikipedia data, Generative AI, and Web Search to research, narrate, and visualize local folklore.

---

##  Quick Start Guide

### 1. Prerequisites
Ensure you have **Python 3.8+** installed.

### 2. Installation
Open your terminal or command prompt in the project folder and run the following command to install all dependencies:

```bash
pip install fastapi uvicorn requests wikipedia-api duckduckgo-search edge-tts geopy pandas

Note: If you are running this inside a Jupyter environment (like Anaconda or Colab), you can run !pip install ... in the first cell of the notebook.

3. How to Run (Step-by-Step)
This project is contained entirely within the Jupyter Notebook (.ipynb). The notebook acts as a "Builder" that automatically creates the necessary system files and launches the server.

Open the Notebook: Launch your Jupyter Notebook file (e.g., submission.ipynb).

Run All Cells: Execute the cells from top to bottom.

File Creation: The initial cells use %%writefile to automatically generate the core/ folder, agent.py, main.py, and index.html.

Server Launch: The final cell starts the uvicorn server.

Access the Dashboard:

Once the server starts, you will see a URL in the output (usually http://127.0.0.1:8001).

Open your web browser and go to: http://localhost:8001

📂 Project Structure
When you execute the notebook, it automatically generates this architecture on your disk:

Plaintext

📂 Project Root
├── 📄 submission.ipynb       # The Main Source of Truth (Run this)
├── 📄 README.md              # This file
├── 📄 main.py                # FastAPI Server Entrypoint
├── 📄 index.html             # Frontend Dashboard (MapLibre + Charts)
└── 📂 core/                  # AI Logic Module
    ├── 📄 agent.py           # The "Brain" (Wikipedia + LLM + Search)
    ├── 📄 narrative.py       # Narrative Planning Logic
    ├── 📄 data_service.py    # Geocoding & Cultural Data
    └── 📄 cultural_intelligence_builder.py
 Architecture & Features
Frontend: MapLibre GL JS (Interactive Map), Chart.js (Cultural Radar).

Backend: FastAPI (High-performance Python server).

The "Agent" (core/agent.py):

Grounding: Fetches real history via Wikipedia-API.

Storytelling: Uses Cloud LLM (Pollinations.ai) to generate folklore based on facts.

Visualization: Uses DuckDuckGo Search to find real historical images (preventing AI hallucinations).

Voice: Uses Edge-TTS for neural voice narration.

  Troubleshooting
"Address already in use" Error:

If you restart the kernel, the old server might still be holding Port 8001.

Fix: Restart your kernel (Kernel -> Restart) or change the port in the final command (e.g., port=8002).

Map Not Loading:

Ensure you have an active internet connection (Map tiles and Search require internet).

Image Search Failed:

If images don't appear, the system falls back to a placeholder. This can happen if the search engine rate-limits your IP. Wait 1 minute and try again.

Team / Author
Project: Smart Cultural Storyteller


Track: Generative AI / Education & Cultural Heritage
