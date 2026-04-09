# 🔍 Causal Inference for Business Decisions

Most machine learning models tell you what will happen. This project tells you why it happened and what to do about it.

Built as a full causal inference framework for business decision making, this project goes beyond prediction to answer the questions that actually drive business strategy — did our intervention cause this outcome, which customers will respond to which action, and what is the best policy to maximize results?

---

## ✨ What It Does

**Uplift Modeling**
Identifies which customers will genuinely respond to an intervention versus those who would have converted anyway. Saves businesses from wasting budget on customers who do not need to be targeted.

**Heterogeneous Treatment Effects**
Different actions work differently for different customer segments. This framework estimates treatment effects at the individual level, revealing which segment responds best to which intervention.

**Counterfactual Analysis**
Answers the question no standard ML model can — what would have happened if we had not run this campaign? Builds the counterfactual world to isolate true causal impact.

**Policy Optimization**
Recommends the optimal action for each individual customer based on causal effect estimates, maximizing overall business outcomes within budget constraints.

**A/B Test Simulation**
Simulates business experiments before running them in real life, estimating expected lift, required sample sizes, and statistical power.

**Causal Graph Visualization**
Builds and visualizes directed acyclic graphs representing causal relationships between variables, making assumptions explicit and auditable.

**SHAP Causal Attribution**
Explains not just predictions but causal attributions — which features are genuinely causing the outcome versus merely correlated with it.

**Interactive Streamlit Dashboard**
A full web interface for exploring causal graphs, treatment effects, uplift curves, policy recommendations, and A/B test simulations in real time.

---

## 🏗️ How It Works

```
Raw Business Data
       │
       ▼
Causal Graph Construction via DoWhy
       │
       ▼
Treatment Effect Estimation via EconML and CausalML
       │
       ▼
Uplift Modeling and Customer Segmentation
       │
       ▼
Counterfactual Analysis and Policy Optimization
       │
       ▼
SHAP Causal Attribution
       │
       ▼
Streamlit Dashboard with Interactive Visualizations
```

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Causal Inference | DoWhy, EconML, CausalML |
| Machine Learning | XGBoost, scikit-learn, LightGBM |
| Explainability | SHAP |
| Statistical Testing | scipy, statsmodels |
| Data Processing | Pandas, NumPy |
| Visualization | Plotly, NetworkX, Matplotlib |
| Dashboard | Streamlit |
| Containerization | Docker |
| Language | Python 3.11 |

---

## 📁 Project Structure

```
causal-inference-business-decisions/
├── src/
│   ├── causal_graph.py          
│   ├── treatment_effects.py     
│   ├── uplift_modeling.py       
│   ├── counterfactual.py        
│   ├── policy_optimizer.py      
│   ├── ab_test_simulator.py     
│   └── explainability.py        
├── dashboard/
│   ├── app.py
│   └── components/
├── notebooks/
│   ├── exploration.ipynb
│   └── causal_analysis.ipynb
├── tests/
│   ├── test_treatment_effects.py
│   └── test_uplift.py
├── docker/
│   └── Dockerfile
├── .env.example
├── requirements.txt
└── README.md
```

---

## ⚙️ Setup and Installation

```bash
# Clone the repository
git clone https://github.com/sahithimuppavaram/causal-inference-business-decisions.git
cd causal-inference-business-decisions

# Create virtual environment
python -m venv venv
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Run the Streamlit dashboard
streamlit run dashboard/app.py

# Or run with Docker
docker build -t causal-inference .
docker run -p 8501:8501 causal-inference
```

---

## 📊 Results

Uplift modeling identified the top 20% of customers responsible for 80% of incremental conversions, enabling targeted campaign spend reduction of 40% while maintaining revenue. Counterfactual analysis revealed that 35% of conversions attributed to the campaign would have occurred organically, reshaping marketing ROI calculations.

---

## 🗺️ What Is Coming Next

Integration with real time A/B test data streams, multi-armed bandit optimization for dynamic policy updates, and a REST API layer for serving causal recommendations to production systems.

---

## 📄 License

MIT License
