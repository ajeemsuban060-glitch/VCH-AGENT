# VCH-Agent — Viral Content Hunter

> **A local-first predictive AI system for identifying fresh Reddit and YouTube content with unusually high future engagement potential, then measuring whether those predictions were correct.**

---

## 1. Project Identity

**Project Name:** VCH-Agent  
**Full Name:** Viral Content Hunter  
**Project Type:** Local-first predictive AI / ML system  
**Primary Language:** Python  
**Initial Interface:** Gradio  
**Database:** SQLite  
**Target Cost:** $0  
**Primary Platforms:** Reddit and YouTube

VCH-Agent is a predictive content intelligence system.

It does not simply identify content that is already trending.

Its purpose is to identify **fresh content that has an unusually high probability of outperforming its expected baseline within a future time window**, then track the content and compare the prediction against the actual outcome.

---

# 2. Core Principle

The most important principle of VCH-Agent is:

> **VCH-Agent does not claim that content will go viral. It makes measurable predictions and then proves whether those predictions were correct.**

The system must therefore be designed around:

- prediction
- measurement
- temporal validation
- reproducibility
- explainability
- controlled experimentation
- model improvement

Never present an unverified prediction as a fact.

---

# 3. Core Workflow

The complete conceptual workflow is:

```text
Fresh Content
      ↓
Data Harvesting
      ↓
Feature Extraction
      ↓
Local LLM Analysis
      +
Real-Time Engagement Signals
      +
Historical Baselines
      ↓
Feature Engineering
      ↓
Predictive ML Model
      ↓
Virality Probability
      ↓
Top-K Ranking
      ↓
Prediction Storage
      ↓
24h / 72h Tracking
      ↓
Actual Outcome
      ↓
Evaluation
      ↓
Training Dataset
      ↓
Controlled Model Improvement