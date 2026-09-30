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
