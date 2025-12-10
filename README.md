---------------------
PROJECT STRUCTURE
---------------------
```text
loan-policy-optimization/
│
├── notebooks/
│   ├── 01_EDA_and_Preprocessing.ipynb
│   ├── 02_Deep_Learning_Model.ipynb
│   ├── 03_RL_Agent.ipynb
│   └── 04_Analysis_and_Comparison.ipynb
│
├── data/                     # Dataset location
│
├── models/                   # Trained DL & RL models
│
├── results/
│   ├── figures/
│   ├── metrics/
│   └── predictions/
│
├── requirements.txt
├── README.md
└── report/
    └── Final_Report.pdf


---------------------------
INSTALLATION
---------------------------
git clone https://github.com/YOUR_USERNAME/loan-policy-optimization.git
cd loan-policy-optimization
python -m venv venv
venv\Scripts\activate   # Windows
pip install -r requirements.txt

---------------------------
USAGE WORKFLOW
---------------------------
| Step | Notebook                           | Purpose                     |
| ---- | ---------------------------------- | --------------------------- |
| 1    | `01_EDA_and_Preprocessing.ipynb`   | Cleaning, encoding, scaling |
| 2    | `02_Deep_Learning_Model.ipynb`     | Train MLP                   |
| 3    | `03_RL_Agent.ipynb`                | Train CQL agent             |
| 4    | `04_Analysis_and_Comparison.ipynb` | Model comparison            |


------------------------------
DEEP LEARNING MODEL DETAILS
-----------------------------

Architecture: 128 → 64 → 32 → 1

Activation: ReLU + Sigmoid

Loss: Weighted BCE

Optimizer: Adam

Regularization: Dropout + BatchNorm

Early Stopping Enabled

---------------------------
FINAL TEST PERFORMANCE
---------------------------

AUC-ROC: 0.68

Accuracy: 82%

Precision: 0.45

Recall: 0.28

F1-Score: 0.35


---------------------------
REINFORCEMENT LEARNING
---------------------------

Algorithm: Discrete Conservative Q-Learning (CQL)

Offline Training Only

Action Space: {Deny, Approve}

State Space: 31 financial features

---------------------------
OPTIMIZATION
---------------------------
Profit per loan

Default-adjusted returns

Capital efficiency


----------------------
KEY INSIGHTS
----------------------

| Aspect             | Deep Learning | Reinforcement Learning |
| ------------------ | ------------- | ---------------------- |
| Objective          | Accuracy      | Profit                 |
| Output             | Probability   | Decision               |
| Optimization       | Risk          | Return                 |
| Interpretability   | High          | Medium                 |
| Business Alignment | Indirect      | Direct                 |

----------------------
LIMITATIONS
----------------------

Offline RL has no counterfactual data

Reward function is simplified

No fairness constraints applied

No real-time online learning

Single-step decision only

----------------------
FUTURE ENHAMCEMENT
----------------------
Fairness-aware policy learning

Online RL / Contextual Bandits

SHAP-based explainability

Recovery-aware rewards

Multi-objective profit + risk optimization
