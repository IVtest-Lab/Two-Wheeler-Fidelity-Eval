# Two-Wheeler-Fidelity-Eval

This repository presents the **Questionnaire** for the **Human-perceived Fidelity** dimension of the fidelity evaluation method proposed in **_Evaluating the Fidelity of Two-Wheeler Simulation Models: A Multi-Dimensional Method_**.

The questionnaire asks human participants to watch interaction videos between two-wheelers and cars, judge whether the observed interaction appears real or simulated, and then rate the fidelity of the two-wheeler / car behaviors.

## Questionnaire Design

### Trials and Videos

- The questionnaire contains **20 trials**.
- Each trial consists of **one interaction video** and **the same three questions**.
- The 20 interaction videos are provided as GIFs in [`Questionnaire_interaction_gif/`](./Questionnaire_interaction_gif), organized as follows:

| Source | Scenario | Count | Path |
|---|---|---|---|
| Real | Straight-ahead | 5 | `Questionnaire_interaction_gif/Real/Straight-ahead/` |
| Real | Left-turn | 5 | `Questionnaire_interaction_gif/Real/Left-turn/` |
| Simulated | Straight-ahead | 5 | `Questionnaire_interaction_gif/Sim/Straight-ahead/` |
| Simulated | Left-turn | 5 | `Questionnaire_interaction_gif/Sim/Left-turn/` |
| **Total** |  | **20** |  |

The set is balanced across **Real vs. Simulated** (10 each) and across **Straight-ahead vs. Left-turn**.

### Questions

For each trial, human participants answer the same three questions:

- **Q1 — Interaction identification** (select one)
  - ☐ Both the car(s) and the two-wheeler in this interaction follow **real** trajectories.
  - ☐ Both the car(s) and the two-wheeler in this interaction follow **simulated** trajectories.
- **Q2 — Car realism** (1–5 scale)
  - How would you rate the realism of the car's (cars') interaction behaviors?
- **Q3 — Two-wheeler realism** (1–5 scale)
  - How would you rate the realism of the two-wheeler's interaction behaviors?

## Example Trial

Please watch the trajectory animation below and answer the following questions.

<div align="center">

<img src="Questionnaire_interaction_gif/Sim/Left-turn/Sim%20left-turn%20case%201.gif" alt="Simulated left-turn interaction, case 1" width="720">

</div>

<div align="left">

### Q1: Please identify

- ☐ Both the car and the two-wheeler in this interaction follow **real** trajectories.
- ☐ Both the car and the two-wheeler in this interaction follow **simulated** trajectories.

### Q2: How would you rate the realism of the car's interaction behaviors? *(1–5 scale)*

### Q3: How would you rate the realism of the two-wheeler's interaction behaviors? *(1–5 scale)*

</div>

## Two-Wheeler Simulation Model

In the simulated interaction videos, the two-wheeler is controlled by a **two-wheeler behavioral model trained based on Offline-to-Online Reinforcement Learning (O2O RL)**.

The model first learns interactive riding behavior from pre-collected driving data, and is then further improved through online interaction.
The complete technical pipeline—covering offline pretraining, online adaptation, simulation deployment, and fidelity evaluation—is documented here:

📄 **[Overall structure of the O2O RL Two-Wheeler Model](./O2O_RL_TW_model_intro/O2O_RL_TW_model_intro.pdf)**

## Repository Structure

```text
Two-Wheeler-Fidelity-Eval/
├── README.md                               # This document
├── O2O_RL_TW_model_intro/
│   └── O2O_RL_TW_model_intro.pdf           # Overall structure of the O2O RL two-wheeler model
└── Questionnaire_interaction_gif/
    ├── Real/
    │   ├── Straight-ahead/                 # 5 real straight-ahead interaction GIFs
    │   └── Left-turn/                      # 5 real left-turn interaction GIFs
    └── Sim/
        ├── Straight-ahead/                 # 5 simulated straight-ahead interaction GIFs
        └── Left-turn/                      # 5 simulated left-turn interaction GIFs
```


