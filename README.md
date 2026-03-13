# Can Language Betray Intent?
## Multi-Modal Deception Detection in LLM Public Goods Games
 
## Overview
 
This project asks: *can surprisal-based language monitoring maintain cooperation in a multi-agent public goods game at lower cost than always-on punishment?*
 
Four GPT-4.1-mini agents play a 15-round public goods game with pre-play chat. A frozen DistilGPT-2 scores every message for linguistic anomaly (NLL surprisal). When a message exceeds a rolling threshold τ, the institution punishes the *next* round — without observing any contribution yet.
 
**Core result:** `surprisal_only` achieves **0.610 cooperation at 9.3% punishment exposure** — equivalent deterrence to `always` (0.603 at 100% exposure) at one-tenth the enforcement cost.
 
**Fundamental limit:** The Manipulator persona ("Let's all cooperate!" + contributes 2–6) defeats NLL detection entirely. `adaptive_adversarial` collapses to 0.513 — the worst condition in the experiment.

 ## Requirements
 
```
openai>=1.0.0
sentence-transformers>=2.2.0
torch>=2.0.0
scikit-learn>=1.3.0
pandas>=2.0.0
numpy>=1.24.0
matplotlib>=3.7.0
seaborn>=0.12.0
transformers>=4.30.0
```
 
---
