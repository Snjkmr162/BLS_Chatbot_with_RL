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

## 📁 Repository Structure

