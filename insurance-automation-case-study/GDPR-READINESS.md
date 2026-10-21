# GDPR readiness roadmap

**Status: Review in progress — this is a project plan, not legal advice or certification.**

GDPR does not require a universal “GDPR certificate” to run every automation. For an actual insurance service, lawful processing and accountability must be evaluated case by case, with qualified privacy/legal review where needed.

## Open review items
- [ ] Inventory each category of personal data collected: policy details, DOB, contact details, quote answers, communication logs, Slack messages, email, and n8n execution data.
- [ ] Map controller/processor roles, purposes, recipients, locations, retention and legal basis **per activity**. Do not assume consent is the right legal basis for everything.
- [ ] Produce a suitable Article 13/14 privacy notice before collecting real data.
- [ ] Review processor agreements, vendors and international transfers for n8n hosting, model provider, Slack, Gmail and any other vendors.
- [ ] Minimize identifiers and restrict sensitive data in logs, prompts, model outputs and staff channels.
- [ ] Evaluate whether any special-category data is handled, and determine any additional requirements.
- [ ] Put tested retention/deletion rules in place for data tables, execution histories, backups and emails.
- [ ] Implement access controls, role permissions, secret management, encryption, incident response and change logging.
- [ ] Design a reliable process for access, rectification, erasure and other relevant data-subject requests.
- [ ] Assess need for a DPIA (Article 35); carry it out before high-risk processing if required.
- [ ] Document risks, mitigations and technical testing (false matching, incorrect output, inappropriate disclosure, duplicate delivery, prompt injection, failed human handoff).
- [ ] Validate insurance-specific authorization, document-issuance policies, records and communication requirements with appropriate professionals.
- [ ] Assess AI Act relevance based on the **actual** processing purpose and system behavior.

## Release gate
**Do not connect the public demo to live insurance systems or customer data.** Any operational use should follow security, privacy, legal and integration review.

## Portfolio claim
Suitable: “Functional insurance workflow prototype; GDPR readiness work underway.”

Not suitable: “GDPR certified”, “compliant by design”, “production-secure”, or “legally approved”.
