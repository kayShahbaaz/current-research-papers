# Study Summary: AI-GRC Integrated Management Framework

**Artificial Intelligence in Governance, Risk, and Compliance: An Integrated Framework Grounded in ISO/IEC 27001:2022 and ISO/IEC 42001:2023**

*Dr. M. Abdul Qadeer and Shahbaaz Ahmad*

Department of Computer Engineering, Zakir Husain College of Engineering & Technology, AMU

---

## The Problem

AI is already inside GRC functions at most large regulated organisations. The governance frameworks those organisations use were not built for it. The result is a pattern that keeps repeating: an AI tool in an oversight role, performing well by the wrong measure, causing harm the deploying organisation had no mechanism to detect.

Obermeyer et al. [1] documented this precisely. A clinical risk algorithm assigned lower risk scores to Black patients than to White patients with identical objective health status. No deliberate design choice caused this. The training data was historical healthcare spending, which reflected decades of unequal access rather than unequal need. The model ran at scale before any external analysis caught the problem.

GRC deployments carry the same risks. A fraud detection model with a demographic error rate disparity is a legal liability. A compliance monitoring tool that acts on flagged outputs without human review in between is an accountability gap. A model trained on data collected for a different purpose is a GDPR violation waiting to be found.

This study examines how organisations can govern AI in GRC contexts before those failures occur.

---

## What Was Already Known

Jooda and Onukak [2] confirmed that ML-based approaches improve real-time risk detection and cut manual compliance workloads in meaningful ways. The workload case for AI in regulatory monitoring is especially clear: the volume of regulatory output that compliance teams must track across jurisdictions has grown to the point where human-only monitoring is genuinely impractical [3].

Prior work also established the problems. Algorithmic bias in consequential decisions is a legal risk before it is an ethical one. Privacy infringement gets built into AI training pipelines when organisations do not formally resolve GDPR purpose limitation requirements before training begins. Adversarial data poisoning is a documented threat to ML tools used in security and compliance contexts. Accountability frameworks built for named individuals do not map cleanly onto AI-generated outputs acted upon without human review.

What did not exist was a governance framework that tied specific risks to specific controls across both ISO/IEC 27001 and ISO/IEC 42001, accounted for GDPR and EU AI Act requirements in the same structure, and was designed to run inside an existing ISMS rather than alongside one. That is what this paper addresses.

---

## Methodology

The study uses a PRISMA-guided systematic literature review combined with normative document analysis. Forty-seven sources met inclusion criteria after two screening rounds. Databases covered included IEEE Xplore and Scopus, as well as ScienceDirect and ACM Digital Library. Official repositories from ISO, NIST, and the EU Commission were also searched. Coverage ran from January 2018 to March 2026. Standards were analysed at clause level. No primary empirical data were collected.

---

## The Framework

The AI-GRC Integrated Management Framework (AI-GRC IMF) is a five-phase implementation pathway. It specifies how to apply ISO/IEC 27001:2022 and ISO/IEC 42001:2023 together inside an AI-enabled GRC context. Thw Five phases are: Identify, Assess, Control, Deploy, Monitor.

### Phase 1: Identify

The organisation produces a full inventory of AI tools with any GRC function. This covers tools in production and tools still in development, but also third-party SaaS products with embedded AI features, the category most consistently overlooked in practice and the one most likely to introduce unexamined risk. Each tool is classified against the EU AI Act risk tier structure and the existing ISMS asset classification scheme. The AI management system scope is defined as an extension of the existing ISMS scope under ISO/IEC 27001 Clause 4.3.

### Phase 2: Assess

Every inventoried tool goes through a dual risk assessment, and the sequencing matters. The ISO/IEC 27001 Clause 8.2 process is extended first, picking up AI-specific information security risks including adversarial attack surfaces in training pipelines and model parameter exposure. The ISO/IEC 42001 Clause 6.1 process then evaluates AI-specific risks, covering bias and data quality failures before moving to transparency gaps and regulatory exposure. Where a tool processes personal data, the GDPR Article 35 DPIA runs here rather than as a separate exercise. The output is one consolidated risk register.

### Phase 3: Control

Treatment plans draw from both ISO/IEC 27001 Annex A and ISO/IEC 42001 Annex A, documented in an extended Statement of Applicability. This phase also establishes the runtime governance architecture: human-in-the-loop thresholds for consequential AI decisions, model validation protocols covering bias testing and adversarial robustness, and logging requirements built as a single design satisfying ISO/IEC 42001 and EU AI Act Article 12 while also meeting GDPR Article 22. Privacy-preserving design choices are specified as architectural requirements at this stage. Specifying them here is what makes them genuine design decisions rather than compliance additions bolted on after the fact.

### Phase 4: Deploy

Pre-market conformity assessment for EU AI Act high-risk tools is completed and documented before release. Staged rollout with parallel human review validates behaviour against the benchmarks set in Phase 3. Change management covers both the software infrastructure and the governance documentation. Both must be updated when model architecture or training data changes in a material way.

### Phase 5: Monitor

A unified monitoring programme merges ISO/IEC 27001 Clause 9 and ISO/IEC 42001 Clause 9 requirements into one rather than running two separate review cycles. Coverage includes automated performance monitoring for accuracy degradation and distributional shift. Bias metric tracking runs against defined thresholds. Regulatory horizon scanning covers EU AI Act implementing acts and sector-specific guidance. Findings feed back into Phase 2, closing the plan-do-check-act loop.

---

## What the Study Found

**On integration:** An organisation already certified to ISO/IEC 27001 can bring ISO/IEC 42001 in by extending what it already has. No second management system is needed. Building on what already exists is not a compromise. It is the condition under which governance gets done.

**On bias:** ISO/IEC 42001 Annex A treats bias evaluation as a control objective. EU AI Act Article 10 makes data quality and representativeness requirements mandatory for high-risk tools. These are enforceable legal obligations. Not aspirational principles.

**On privacy:** Federated learning can satisfy GDPR data minimisation requirements without material loss of model utility [4]. The barrier to adoption is almost always the governance decision to use these tools, not their technical availability.

**On accountability:** The human oversight controls in ISO/IEC 42001 Annex A give organisations the formal governance basis for deciding which AI decisions must pass through human review before they result in action. Technical measures alone cannot solve the accountability problem.

**On the EU AI Act:** Credit scoring models, fraud detection tools, and compliance monitoring systems in regulated sectors frequently fall into the high-risk category, which triggers conformity requirements covering data quality, technical documentation, logging, and post-market monitoring. ISO/IEC 42001 conformity covers most of those requirements, which means organisations that have already invested in the standard are substantially better positioned than those that have not. The Act will be fully applicable from August 2027.

---

## Three Reference Tables

The paper includes three tables built for direct practitioner use.

**Table I** maps eight AI use-cases to GRC function domains and applicable standards: regulatory horizon scanning, predictive risk modelling, fraud and anomaly detection, compliance document monitoring, SIEM/UEBA security analytics, executive risk dashboards, internal audit automation, and LLM policy assistants.

**Table II** compares six governance instruments side by side: ISO/IEC 27001:2022, ISO/IEC 42001:2023, NIST AI RMF 1.0, GDPR, EU AI Act 2024/1689, and ISO/IEC 27701:2019.

**Table III** maps seven AI risk categories to specific Annex A controls from both standards, with regulatory requirements and mitigation techniques for each. Those seven are: algorithmic bias, privacy infringement, adversarial attacks, model drift, explainability deficit, accountability deficit, and third-party supply-chain risk.

---

## Limitations

This is secondary research. The AI-GRC IMF has not been tested in the field, and no longitudinal studies of integrated ISO/IEC 27001 and ISO/IEC 42001 implementations in GRC contexts exist in the published literature at time of writing. Field-based case study validation is the most pressing direction for follow-on work.

Generative AI creates governance problems the current versions of both standards do not fully address. Hallucination risk in compliance outputs is one. Prompt injection vulnerabilities are another. Training data contamination is a third. ISO/IEC JTC 1/SC 42 is expected to issue supplementary guidance. Practitioners should put controls in place without waiting for it.

---

## References (Selected)

[1] Z. Obermeyer et al., "Dissecting racial bias in an algorithm used to manage the health of populations," *Science*, vol. 366, no. 6464, pp. 447–453, Oct. 2019.

[2] J. O. Jooda and P. I. Onukak, "AI-driven governance, risk and compliance (GRC) systems," *Open Access Res. J. Sci. Technol.*, vol. 9, no. 1, pp. 87–101, 2023.

[3] KPMG International, "AI in governance, risk and compliance (GRC)," KPMG Risk Insights Report, Jul. 2025.

[4] W. O. Hundeyin et al., "Integrating privacy-preserving AI models into AI governance frameworks," *Int. J. Innovative Sci. Res. Technol.*, vol. 10, no. 10, pp. 376–384, Oct. 2025.

---

## Request the Full Paper

The complete paper is available on request. It includes all three tables and the full 16-source reference list, together with the detailed framework specifications.

Email **maqadeer@amu.ac.in** or **kayshahbaaz@zhcet.ac.in** with your name and affiliation. A brief note on your intended use is helpful.

---

*© 2026 M. Abdul Qadeer and Shahbaaz Ahmad. All rights reserved. This summary is provided for academic communication purposes.*
