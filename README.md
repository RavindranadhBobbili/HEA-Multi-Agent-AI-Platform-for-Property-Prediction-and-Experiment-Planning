# HEA-Multi-Agent-AI-Platform-for-Property-Prediction-and-Experiment-Planning
Built a multi-agent AI platform for high-entropy alloy research integrating literature retrieval, experiment planning, physics-informed HEA screening, machine learning property prediction, model comparison, uncertainty estimation, and FastAPI dashboard deployment.
# HEA Multi-Agent AI Platform for Property Prediction and Experiment Planning

This project is a full-stack AI platform for high-entropy alloy research. It combines literature retrieval, experiment planning, physics-informed HEA screening, machine learning property prediction, and a browser-based dashboard.

## Features

- Literature RAG using TF-IDF retrieval
- Evidence-backed literature summary
- Bayesian-style experiment proposal using Gaussian Process regression
- HEA critic using VEC, atomic size mismatch, and entropy features
- Property prediction using Random Forest, Extra Trees, Gradient Boosting, and Ridge regression
- Model comparison with R² and MAE
- Uncertainty estimate from ensemble model spread
- SQLite experiment history
- CSV export
- FastAPI backend
- Interactive web dashboard

## Project Motivation

High-entropy alloy design requires combining literature evidence, physics rules, experimental feedback, and machine learning. This project demonstrates how AI agents can support materials discovery by suggesting experiments, checking alloy feasibility, and predicting property scores from recorded experiments.

## Tech Stack

- Python
- FastAPI
- Scikit-learn
- NumPy
- SQLite
- HTML/CSS/JavaScript
- Uvicorn

## Installation


Main Modules
Agent	Function
Retriever Agent	Searches ingested literature
Summarizer Agent	Produces evidence-backed synthesis
Planner Agent	Suggests next experiment
Critic Agent	Applies HEA physics rules
Predictor Agent	Trains ML models and predicts property score
Report Agent	Exports experiment records
API Endpoints
GET  /
GET  /health
POST /literature/ingest
POST /literature/answer
POST /agent/propose
POST /experiments/record
GET  /experiments/history
POST /models/train
POST /predict/property
GET  /export/csv
Example Workflow
Ingest HEA literature text.
Ask a literature question.
Generate candidate experiments.
Record measured property score.
Train prediction models.
Predict property score for a new alloy condition.
Export experiment history as CSV.
Example Use Case

Input alloy/process condition:

{
  "al_pct": 10,
  "co_pct": 22,
  "cr_pct": 22,
  "fe_pct": 22,
  "ni_pct": 24,
  "anneal_temp_c": 900,
  "anneal_time_h": 5,
  "cooling_rate_c_per_min": 12
}

Output includes:

predicted property score
model-wise predictions
uncertainty estimate
VEC
atomic size mismatch
mixing entropy
HEA critic recommendation
Disclaimer

This is a research and portfolio project. The built-in HEA rules are simplified heuristics and should be validated with experimental data, CALPHAD calculations, microscopy, and domain expertise before real materials decisions.

Future Improvements
Sentence-transformer embeddings
FAISS vector database
PDF ingestion
SHAP explainability
CALPHAD feature integration
Multi-objective optimization
Docker deployment
Cloud deployment on AWS

## requirements.txt

```text
fastapi
uvicorn
scikit-learn
numpy
pydantic
nest_asyncio
Suggested Folder Structure
hea-multi-agent-property-prediction/
│
├── hea_agent_property_dashboard.py
├── README.md
├── requirements.txt
├── .gitignore
└── reports/

```bash
pip install fastapi uvicorn scikit-learn numpy pydantic nest_asyncio

MIT License

Copyright (c) 2026 Ravindra B

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell   
copies of the Software, and to permit persons to whom the Software is        
furnished to do so, subject to the following conditions:                     

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.                              

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR   
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,     
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE  
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER       
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
