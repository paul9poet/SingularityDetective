# Hurricane Katrina Case Study

This case study documents how AGI-ColdCases handles the *Katrina 2005* emergency simulation.

---

## 🕒 Timeline Phases

| Time | Phase |
|------|-------|
| T-100h | Early depression |
| T-72h  | Storm formation |
| T-48h  | Hurricane watch |
| T-36h  | Hurricane warning |
| T-24h  | Peak intensity |
| T=0h   | Landfall |
| T+12h  | Levee failures |
| T+24h  | Flooding |
| T+48h  | Aftermath |

Each checkpoint becomes a **decision node**.

---

## 🧩 Inputs to the System

At each checkpoint, the simulation feeds:
- synthetic weather data
- infrastructure status
- governance state
- communication data

These form the *observation vector*.

---

## 🧠 Decision Process

1. **Numeric hub analyzes weather and risk**
2. **Risk scores are bound with constraints via VSA**
3. **Symbolic hub evaluates logic with ethical priorities**
4. **Decisions are logged with audit proofs**

---

## 📄 Example Decision Log Entry

```json
{
  "timestamp": "2005-08-28T14:00:00Z",
  "time_label": "T-24h",
  "state": { … },
  "risk_scores": { "composite_risk": 0.89 },
  "decision": "recommendMandatoryEvacuation",
  "justification": {
    "rulesFired": ["HighRiskThreshold","MinimizeLossOfLifeConstraint"],
    "confidence": 0.92
  }
}
