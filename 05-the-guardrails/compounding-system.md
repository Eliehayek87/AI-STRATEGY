# Compounding System Design

## Feedback Loops

| Loop | Input | Output | Compounds? | Status |
|------|-------|--------|-----------|--------|
|Analyst review decisions | Human validation, overrides, escalation outcomes| Improved confidence calibration and false-positive reduction| Y | active |
|Open-source and internal screening results |Entity matches, watchlists, prior notices, adverse media |Better risk classification and contextual matching | Y | active  |
|Regression and golden dataset evaluations | Prompt/model changes and benchmark runs| Improved reliability and hallucination control| Y | active |

**Broken loop identified by partner:*The system currently captures operational decisions but does not consistently reinject analyst feedback and escalation outcomes into a structured continuous evaluation and improvement pipeline.*
**Fix plan:*Implement a centralized evaluation and feedback layer that automatically captures analyst adjudications, false positives, escalation rationale, and source reliability scoring to continuously update regression benchmarks and improve retrieval and confidence calibration.*

## Context Connectivity
<!-- How does knowledge flow across teams and domains? Where does it silo? -->
Knowledge flows across operational analysts, legal/human-rights reviewers, and governance teams through shared case reviews, escalation workflows, and audit trails. Current silos remain around historical adjudication decisions, source credibility intelligence, and politically sensitive assessments that are not yet fully centralized into reusable institutional knowledge.

## Governance Policy

**Scope:*Operational support for notice screening, watchlist checks, open-source analysis, public figure/activist detection, and human-rights/neutrality risk identification.*
**Autonomy boundaries:*The system may assist with screening, summarization, matching, and risk indication but cannot autonomously approve, reject, or make final operational/legal determinations.*
**Escalation triggers:*Politically exposed persons, activists, journalists, human-rights concerns, weak-confidence matches, conflicting records, neutrality-sensitive indicators, or high-risk geopolitical contexts.*
**Audit cadence:*Continuous logging with weekly regression reviews and periodic governance/compliance audits.*
**Regulatory exposure (EU AI Act / other):*High-risk AI considerations due to operational screening, profiling support, and law-enforcement-related analytical assistance requiring strong governance, transparency, auditability, and human oversight controls.*

## Agent Topology
<!-- If using agents: what can each agent do? What can't it do? Who approves what? -->
The screening agent performs internal dataset retrieval, watchlist matching, and open-source analysis. A risk-assessment agent evaluates public figure, activist, political, and neutrality-sensitive indicators. A governance agent validates explainability, confidence thresholds, and escalation requirements. Final operational decisions remain exclusively under authorized human analysts and governance/legal reviewers.
## Shadow AI Audit

| Tool | Owner | Risk Level | Decision |
|------|-------|-----------|----------|
|Public LLM chatbot usage for case analysis | Individual analysts| H  |  govern  |
| Open-source scraping and monitoring tools| Operational review teams| M  |  govern  |
| Internal unofficial AI summarization scripts| Local operational teams| H | kill |

**Total tools found:**Multiple unofficial and fragmented AI-assisted operational tools identified across teams.
**Tools after triage:**Only governed, auditable, and approved AI-assisted workflows retained under centralized oversight.
**Estimated hidden spend:**Moderate hidden operational and compliance cost due to fragmented tooling, duplicated AI usage, and unmanaged external AI service consumption.
