# Project Self-Assessment
## AI Bias Assessment vs AI Risk Assessment Template & AI Governance Policy Template

**Assessed by:** Jake Kantor  
**Date:** May 2026

---

## Part 1 — Assessment Against AI System Risk Assessment Template

### Section 1 — System Description

| Field | Status | Evidence |
|-------|--------|----------|
| System Name | ✅ Met | UTKFace Gender Classification CNN |
| System Owner | ✅ Met | Jake Kantor, Greg Arcand, Marcus Lee |
| Business Unit | ⚠️ Partial | Research context — not an organizational deployment |
| Deployment Date | ✅ Met | Spring 2026 |
| System Version | ✅ Met | Baseline CNN and Adversarially Trained CNN documented |
| Primary Use Case | ✅ Met | Binary gender classification from facial images |
| Intended Users | ⚠️ Partial | Research — real-world intended users not defined |
| Geographic Scope | ✅ Met | Global (UTKFace dataset spans demographics) |
| Data Sources | ✅ Met | UTKFace — 23,708 images documented with demographic breakdown |

**Gap:** System description framed as research project rather than organizational deployment. A real client engagement would require organizational context, business unit, and intended user population.

---

### Section 2 — Regulatory Classification

| Requirement | Status | Evidence |
|-------------|--------|----------|
| EU AI Act risk classification | ✅ Met | High-risk identified — biometric classification |
| High-risk category identified | ✅ Met | Biometric identification, employment context noted |
| NYC Local Law 144 applicability | ✅ Met | Bias audit methodology directly maps to LL144 requirements |
| GDPR / CCPA consideration | ⚠️ Partial | Privacy section covers DP and FL but no explicit GDPR mapping |
| Additional sector regulations | ❌ Not Met | No sector-specific regulatory analysis |

**Gap:** GDPR data subject rights and sector-specific regulations not explicitly addressed. Would need expansion for a real client engagement.

---

### Section 3 — NIST AI RMF Assessment

#### GOVERN

| Control Area | Status | Evidence |
|-------------|--------|----------|
| AI governance policy exists | ⚠️ Partial | No organizational policy — research context |
| Roles and responsibilities defined | ✅ Met | Co-authors documented, assessor identified |
| Risk tolerance documented | ⚠️ Partial | Implicit in recommendations but not formally stated |
| Human oversight mechanisms | ✅ Met | Recommended in governance recommendations |
| Incident response plan | ❌ Not Met | Not addressed in research context |
| Vendor AI governance requirements | ❌ Not Met | No vendor assessment conducted |

#### MAP

| Risk Area | Status | Evidence |
|-----------|--------|----------|
| Intended use risks | ✅ Met | Misclassification risks documented across deployment contexts |
| Data risks | ✅ Met | Training data imbalance, demographic representation documented |
| Model risks | ✅ Met | Adversarial vulnerability, bias, privacy tradeoffs all assessed |

#### MEASURE

| Domain | Status | Evidence |
|--------|--------|----------|
| Fairness metrics by group | ✅ Met | TPR, FPR, Accuracy, Precision by race — before and after mitigation |
| Robustness testing | ✅ Met | Gaussian noise, FGSM attack, adversarial training comparison |
| Explainability | ✅ Met | LIME applied to three test images with governance interpretation |
| Privacy assessment | ✅ Met | DP across epsilon values, Federated Learning simulation |
| Acceptable disparity threshold | ❌ Not Met | No formal threshold defined — gap for real deployment |

#### MANAGE

| Area | Status | Evidence |
|------|--------|----------|
| Risk treatment plan | ✅ Met | Six governance recommendations with specificity |
| Monitoring plan | ⚠️ Partial | Continuous monitoring recommended but no cadence defined |
| Incident response | ❌ Not Met | Not addressed |

---

### Section 4 — Regulatory Compliance Checklist

#### EU AI Act

| Article | Status | Evidence |
|---------|--------|----------|
| Article 9 — Risk management | ✅ Met | Full NIST AI RMF application documented |
| Article 10 — Training data | ✅ Met | Dataset demographics documented, imbalance identified |
| Article 11 — Technical documentation | ✅ Met | README, notebook, executive summary |
| Article 12 — Logging | ⚠️ Partial | Recommended but not implemented in research context |
| Article 13 — Transparency | ✅ Met | LIME explainability implemented and documented |
| Article 14 — Human oversight | ✅ Met | Recommended with specificity in governance section |
| Article 15 — Accuracy and robustness | ✅ Met | Adversarial testing, noise perturbation, accuracy metrics |

#### NYC Local Law 144

| Requirement | Status | Evidence |
|-------------|--------|----------|
| Bias audit completed | ✅ Met | TPR/FPR by demographic group measured |
| Independent auditor | ⚠️ Partial | Academic context — not independent third party |
| Results published | ✅ Met | GitHub repository public |
| Candidate/employee notice | ❌ Not Met | Research context — not applicable |

---

### Overall Risk Assessment Template Coverage

| Domain | Coverage | Rating |
|--------|----------|--------|
| System Description | 75% | ⚠️ Good |
| Regulatory Classification | 70% | ⚠️ Good |
| GOVERN | 50% | ❌ Partial |
| MAP | 95% | ✅ Strong |
| MEASURE | 90% | ✅ Strong |
| MANAGE | 60% | ⚠️ Partial |
| EU AI Act Compliance | 85% | ✅ Strong |
| NYC LL144 Compliance | 65% | ⚠️ Good |

**Overall Template Coverage: ~74%**

**Primary Gaps:**
- No formal risk tolerance threshold defined
- No monitoring cadence specified
- No incident response procedures
- No vendor assessment
- Research context limits organizational governance sections

---

## Part 2 — Assessment Against AI Governance Policy Template

This project is a risk assessment, not a governance policy. The comparison is therefore about whether the assessment produces outputs that would support a governance policy rather than whether it satisfies policy requirements directly.

### What The Project Supports

| Policy Section | Support Level | How |
|----------------|--------------|-----|
| Section 4 — Acceptable Use | ✅ Strong | Identifies prohibited deployment contexts explicitly |
| Section 5 — Risk Classification | ✅ Strong | High-risk classification with EU AI Act mapping |
| Section 6 — Human Oversight | ✅ Strong | Recommendation 1 and 2 directly address oversight requirements |
| Section 7 — Bias and Fairness | ✅ Strong | Full bias audit methodology demonstrated |
| Section 8 — Transparency | ✅ Strong | LIME explainability implemented |
| Section 9 — Data Governance | ✅ Strong | Training data documentation and imbalance analysis |
| Section 10 — Vendor AI | ⚠️ Partial | No vendor assessment conducted |
| Section 11 — Security | ✅ Strong | Adversarial testing methodology fully demonstrated |
| Section 12 — Roles | ⚠️ Partial | Research roles documented, organizational roles not defined |
| Section 13 — Training | ❌ Not Met | No training materials produced |
| Section 14 — Incident Reporting | ❌ Not Met | Not addressed |

---

## Summary: What This Assessment Demonstrates

### Strengths
- Full NIST AI RMF application across all four functions
- Strongest bias assessment methodology in the portfolio — TPR/FPR by demographic group before and after two mitigation strategies
- Most comprehensive adversarial security testing — FGSM attack, adversarial training, clean vs adversarial accuracy comparison
- Regulatory mapping to EU AI Act and NYC Local Law 144
- Explainability with governance interpretation

### Gaps For Real Client Engagement
1. **Formal risk tolerance thresholds** — what disparity level is acceptable needs to be defined
2. **Monitoring cadence** — how often metrics are reviewed needs specification
3. **Incident response** — what happens when bias or adversarial incidents are detected
4. **Organizational governance context** — roles, responsibilities, policy linkage
5. **Independent auditor status** — for NYC LL144 compliance the auditor must be independent

### What To Build Next
After AIGP these gaps become the basis for additional portfolio artifacts:
- Monitoring and incident response procedure
- Formal risk tolerance framework
- Independent audit methodology document

---

*Self-assessment conducted against AI System Risk Assessment Template v1.0 and AI Governance Policy Template v1.0*  
*Prepared by Jake Kantor | May 2026*
