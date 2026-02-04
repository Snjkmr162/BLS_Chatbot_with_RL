# BLS Labor Market Chatbot with Reinforcement Learning

An interactive chatbot that answers questions about U.S. inflation and unemployment
using Bureau of Labor Statistics (BLS) data, supervised learning, and reinforcement learning.

---

## 🔍 Project Overview

This project demonstrates how reinforcement learning can be used to improve
decision-making in conversational systems.

Rather than generating free-form text, the chatbot:
- Classifies user intent
- Estimates prediction confidence
- Uses a Q-learning policy to decide how to respond

The system is deployed using Streamlit for interactive demos.

---

## 🧠 System Architecture

**Components:**
- TF-IDF + Logistic Regression for intent classification
- Q-learning for response strategy selection
- Deterministic fact-based responses
- Streamlit UI for deployment

**Design Choice:**
Reinforcement learning is trained offline.  
The deployed chatbot performs inference only.

---

## 🎯 Reinforcement Learning Setup

**State Space**
- Confidence level (Low / Medium / High)

**Actions**
- Answer directly
- Answer cautiously
- Ask for clarification

**Reward**
- Positive reward for appropriate responses
- Penalty for overconfident incorrect answers

---

## 📊 RL Learning Curve

The notebook includes a learning curve showing reward stabilization over time,
demonstrating policy convergence.

This training step is not executed during deployment.

---

## 🚀 Deployment (Streamlit)

The Streamlit app:
- Loads trained models and Q-table
- Accepts user questions
- Displays chatbot response with confidence score

No model retraining occurs at runtime.

---

## 🛠️ Tech Stack

- Python
- Pandas / NumPy
- Scikit-learn
- Reinforcement Learning (Q-learning)
- Streamlit
- Google Colab

---

## 🔮 Future Improvements

While the current system trains reinforcement learning policies offline and
uses them for inference-only deployment, several extensions are planned:

- **Online Reinforcement Learning in Streamlit**
  - Incorporate user feedback (e.g., thumbs up/down or follow-up behavior)
    to update rewards in real time.
  - Allow the chatbot to adapt its confidence thresholds and response strategy
    dynamically during live interactions.

- **Human-in-the-Loop Feedback**
  - Use explicit user feedback to refine the reward function instead of relying
    solely on simulated rewards.
  - Improve robustness for ambiguous or multi-intent economic questions.

- **Expanded State Space**
  - Extend the RL state beyond confidence scores to include:
    - Question length
    - Historical user interactions
    - Topic recurrence

- **Hybrid RL + Generative Models**
  - Combine reinforcement learning for decision-making with large language
    models for richer natural-language responses, while preserving factual accuracy.

- **Additional Economic Indicators**
  - Integrate wage growth, labor force participation, and CPI subcomponents
    for deeper macroeconomic analysis.

These improvements would move the system closer to a production-grade
adaptive conversational agent.


