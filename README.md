# LLM-as-a-Judge Engine for Clinical Reasoning Assessment

Automated evaluation architecture designed to grade medical student performance during simulated clinical encounters without hallucination risks.

## Architecture Overview
1. **Input:** Student interaction transcript (audio-to-text / chatbot log).
2. **Grounding:** Official Clinical Practice Guidelines (GPC) + Structured OSCE Scoring Rubrics.
3. **Prompting Strategy:** Few-Shot Prompting with explicit negative constraints and chain-of-thought clinical reasoning.
4. **Output:** Structured JSON file for LMS integration and EPA tracking.

## Sample JSON Output Schema
```json
{
  "student_id": "STU-2026-889",
  "encounter_type": "OSCE_Cardiology_ChestPain",
  "competency_scores": {
    "diagnostic_reasoning": 85,
    "empathy_and_communication": 90,
    "guideline_adherence": 100
  },
  "epas_evaluated": ["EPA-1: History Taking", "EPA-3: Diagnostic Workup"],
  "formative_feedback": "Excellent exploration of pain characteristics. Consider inquiring earlier about family cardiac history."
}

5. Haz clic en **"Commit changes..."**.

---

### Paso 3: Crear el Repositorio 2 (`Clinical-AI-Simulation-Prompts`)

1. Crea tu tercer **"New repository"**.
2. Nombre del repositorio: `Clinical-AI-Simulation-Prompts`
3. Marca **Public** y activa **"Add a README file"**.
4. Edita el `README.md` y pega esto:

```markdown
# Clinical AI Simulation Prompts & Debriefing Frameworks

A collection of prompt engineering templates and debriefing structures for conversational AI avatars in medical education.

## Frameworks Included
- **Embodied Conversational Agents (ECAs):** Patient avatars simulating realistic clinical symptoms, history, and emotional responses.
- **Debriefing with Good Judgment:** Prompt structures designed to analyze student reasoning and foster double-loop learning.
- **AIR Rubric (Advocacy-Inquiry-Reflection):** Automated formative feedback generation for OSCE station debriefs.
