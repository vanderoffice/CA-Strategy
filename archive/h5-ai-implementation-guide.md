# H.5 AI/Agentic Systems - Implementation Guide

*Archived from appendices/08-technical-appendices.md*

For strategic principles and guardrails, see [Appendix H.5](../appendices/08-technical-appendices.md#h5-ai-governance-principles).

---

## Shared Infrastructure Details

California provides shared infrastructure enabling staff to build agentic workflows without individual departments procuring and managing AI systems:

**CDT-Operated Enterprise AI Platform:**
- Centralized access to approved large language models (LLMs)
- Compute resources for training and inference
- Managed services for common AI tasks (OCR, translation, sentiment analysis)
- Unified billing and cost allocation
- Enterprise security and compliance controls

**Departmental Sandboxes:**
- Isolated environments for experimentation and development
- Access to production data copies (anonymized where appropriate)
- Testing framework for validating accuracy and performance
- Promotion pathway from sandbox to pilot to production

**Template Library:**
- Pre-built templates for common use cases
- Customization guidance for department-specific needs
- Community contributions from across state government
- Documentation and training materials

---

## Deployment Process

California establishes a streamlined pathway from idea to production:

1. **Sandbox Development:** Staff build and test agentic workflow in departmental sandbox (days/weeks)
2. **Testing and Validation:** Automated testing validates accuracy, bias, security (1-2 weeks)
3. **Security Scan:** Automated security scanning checks for vulnerabilities and policy compliance (days)
4. **Peer Review:** Review by E3 data governance team ensuring standards compliance (1 week)
5. **Pilot Deployment:** Limited rollout to small user group with monitoring (4-8 weeks)
6. **Production Deployment:** Full rollout with ongoing monitoring and improvement (ongoing)

**Timeline:** Sandbox to production in 8-12 weeks for typical workflow (versus 12-18 months traditional system development)

---

## Expected Impact

- Staff able to automate 20-30% of routine data analysis tasks
- Faster insights enabling more responsive policy and operations
- Reduced backlog of data requests and analysis needs
- Upskilling of workforce in AI literacy and capabilities
- Democratization of data analysis beyond specialized analysts

---

## Standards and Guardrails (Detailed)

Every agentic design pattern must meet California's requirements for:

**Content Classification:**
- Clear labeling of AI-generated content
- Distinction between AI analysis and human judgment
- Appropriate disclaimers for citizen-facing content

**Accuracy Requirements:**
- Validation thresholds for AI outputs (typically 95%+ accuracy for production use)
- Human review requirements for high-stakes decisions
- Fallback to human judgment when confidence below threshold

**Bias Testing:**
- Documented testing for demographic bias
- Disparate impact analysis where applicable
- Mitigation strategies for identified biases

**Transparency:**
- Explainability of AI decisions (how conclusion reached)
- Data provenance (what data informed the analysis)
- Model cards documenting capabilities and limitations

**Logging and Audit:**
- All AI interactions logged for audit and improvement
- Feedback mechanisms capturing accuracy and usefulness
- Regular review of AI performance and drift

**Version Control:**
- Documented versions of prompts, models, and training data
- Rollback capability when new versions underperform
- A/B testing of model improvements
