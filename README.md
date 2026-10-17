# Physical Science & Domain Expert AI Evaluation Portfolio

## 📌 Project Overview
This repository serves as a professional, no-code portfolio demonstrating my methodology as a **Scientific Domain Expert and Data Reviewer**. It simulates real-world RLHF (Reinforcement Learning from Human Feedback) workflows used to evaluate, fact-check, and fine-tune Large Language Models (LLMs) on complex physics, chemistry, and physical science problems.

This case study highlights my capability to apply advanced grading rubrics to scientific reasoning, identify subtle conceptual hallucinations, and ensure mathematical accuracy in AI outputs.

---

## 🗺️ Framework 1: Scientific Reasoning Grading Rubric
This rubric outlines the strict quality metrics applied when evaluating an AI model's response to physical science prompts.

### 1. Accuracy & Factuality Dimensions
*   **Dimensional Consistency:** All derived physical formulas must maintain proper SI unit continuity across calculations. 
*   **First-Principles Alignment:** Explanations must strictly adhere to verified laws of nature (e.g., Thermodynamics, Conservation of Energy, Newtonian Mechanics) without logical leaps or fabrications.

### 2. Hallucination Typologies in Science
*   **Formula Hallucination:** Fabricating constants or combining unrelated physical equations (e.g., blending quantum mechanics equations arbitrarily into classical physics tasks).
*   **Mathematical Logic Error:** Correctly stating a physical concept but failing during algebraic or calculus derivations.

---

## 📝 Framework 2: Structured Expert Model Evaluation (JSON Simulation)
Below is a structured representation of an expert evaluation log. It shows how a complex physics response from an AI model is analyzed, graded, and critiqued for safety and factual correctness:

```json
{
  "evaluation_id": "SCI-PHYSICS-LOG-773",
  "domain": "Classical Mechanics / Thermodynamics",
  "expert_reviewer": "Songokkevin18",
  "model_response_rating": "FAILED_ACCURACY_CHECK",
  "evaluation_details": {
    "user_prompt": "Explain the conservation of momentum during a perfectly inelastic collision between two masses on a frictionless surface and calculate final velocity.",
    "model_output": "In an inelastic collision, kinetic energy and momentum are both conserved. The final velocity formula is given by Vf = (m1*v1 + m2*v2) / (m1 + m2). Therefore, energy remains constant throughout the system...",
    "expert_critique": {
      "error_identified": "Conceptual Hallucination",
      "severity": "CRITICAL",
      "justification": "The model stated that kinetic energy is conserved in a 'perfectly inelastic collision'. By definition, kinetic energy is NOT conserved in an inelastic collision; it is converted into thermal/internal energy, though total momentum remains conserved. The mathematical formula provided was correct, but the conceptual premise violates core thermodynamic principles."
    }
  }
}
```

---

## ⚠️ Framework 3: Physical Science Edge Case Resolution Log
A primary focus of domain-expert data review involves managing highly technical text anomalies and formatting nuances:

| Complex Scientific Scenario | Immediate Expert Review Protocol | Impact on Model Performance |
| :--- | :--- | :--- |
| **Ambiguous Variables** (e.g., AI uses symbol 'k' without defining if it means Boltzmann constant, spring constant, or Coulomb's constant). | Flag the output as `Ambiguous / Poor Clarity`. Require the model to explicitly state the contextual definitions of all thermodynamic or electrostatic variables. | Prevents the model from generating confusing or conflicting math explanations in future turns. |
| **Ideal vs. Real Conditions** (AI solves a fluid dynamics problem assuming an ideal fluid when the prompt implies a viscous, real-world substance). | Grade the prompt alignment as `Partially Incorrect`. Document the deviation from realistic physical boundary constraints. | Trains the model to carefully recognize environmental assumptions (friction, drag, resistance) in user prompts. |
| **LaTeX Formatting Errors** (The physics equations are correct, but the code syntax breaks the visual rendering of fractions or integrations). | Flag as a `Formatting / Render Failure`. Manually annotate the corrected LaTeX math blocks for target data formatting. | Ensures user-facing systems render mathematical notations beautifully and readably without code leakage. |
