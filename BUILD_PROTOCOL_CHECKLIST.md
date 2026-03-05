# Zipo Project Build Protocol
## Dr Marcus Coelho — Kiama Downs Medical Practice

> **Working control document.** Audit-style checklist of the entire Zipo build.
> Status key: ✅ Completed · ⬜ Pending · ⚠️ Needs review · 🔁 Ongoing

---

## PHASE 1 — STRATEGIC FOUNDATION

### 1.1 Define Purpose & Scope
- ✅ Defined routing-only function
- ✅ Explicitly prohibited medical advice
- ✅ Zero personal data collection inside bot
- ✅ Redirect-to-secure-contact model
- ✅ Clear emergency disclaimer

### 1.2 Define Target Population
- ✅ Identified elderly & vulnerable users
- ✅ Integrated empathy protocol
- ✅ Emotional language detection layer added

### 1.3 Legal Risk Review
- ✅ Multiple model reviews on legality
- ✅ Data minimisation architecture
- ✅ Privacy Act (Australia) alignment
- ✅ No Medicare/DOB collection
- ✅ No uploads allowed
- ✅ AI training disabled in policy
- ⚠️ Platform-level confirmation of training opt-out (verify ElevenLabs settings)

---

## PHASE 2 — COMPLIANCE & PRIVACY

### 2.1 Privacy Policy Update
- ✅ New privacy policy drafted
- ✅ Virtual assistant included
- ✅ Analytics disclosure added
- ✅ 30-day retention clause
- ⚠️ Lawyer review recommended (not yet confirmed)

### 2.2 Consent & Forms
- ✅ Secure contact form built
- ✅ Australian-compliant consent language
- ✅ No free-text medical dumping encouraged
- ✅ Redirect model enforced

### 2.3 Analytics & Data Retention
- ✅ Anonymous analytics defined
- ✅ 30-day transcript retention limit
- ✅ Admin-only transcript access
- ✅ Transcript auto-deletion — N/A (no critical data collected; not required at this stage)
- ✅ Analytics storage — Provisional: Airtable (temporary arrangement; migration to dedicated analytics platform required before scaling)

---

## PHASE 3 — FUNCTIONAL ARCHITECTURE

### 3.1 Core Flow Logic
- ✅ Patient status split (new vs existing)
- ✅ Booking guidance logic
- ✅ Consultation length optimisation
- ✅ Referral & script routing
- ✅ Resource-only condition links

### 3.2 Knowledge Base
- ✅ Public website content identified
- ✅ Airtable structured knowledge base created (58 resources + service catalogue)
- ✅ GitHub repository used as chatbot-readable database
- ⚠️ Ongoing: ensure Airtable mirrors only public info
- ⬜ Create quarterly knowledge review process

### 3.3 Booking System Integration
- ✅ HotDoc links integrated
- ⬜ Test failure pathway under real conditions
- ⬜ Confirm phone hours logic triggers correctly (Sydney time)

---

## PHASE 4 — PATIENT EXPERIENCE DESIGN

### 4.1 Tone & Communication
- ✅ Vulnerable-user protocol added
- ✅ Emotional detection implemented
- ✅ Patient-centred communication standard defined (V10)
- ✅ Language detection added (V10)
- ✅ Calm escalation for urgency
- ⬜ Stress test emotional detection with real examples

### 4.2 Satisfaction Rating System
- ✅ 1–10 rating added
- ✅ Anonymous feedback to info@ansteia.com
- ✅ Rules defined (skip if distress/emergency detected)
- ⬜ Build webhook automation
- ⬜ Create rating aggregation dashboard

---

## PHASE 5 — PERFORMANCE & MEASUREMENT

### 5.1 KPI Framework Defined
- ✅ Booking optimisation metrics
- ✅ Revenue allocation improvement model
- ✅ Admin call reduction indicators
- ✅ Resource deflection tracking
- ✅ Emotional detection tracking

### 5.2 Reporting System
- ⬜ Design monthly performance dashboard
- ⬜ Create template report for Marcus
- ⬜ Define baseline (pre-Zipo metrics)
- ⬜ Define 90-day performance review

---

## PHASE 6 — TECHNICAL INFRASTRUCTURE

### 6.1 Hosting & Security
- ✅ HTTPS confirmed on all endpoints
- ⬜ Confirm webhook encryption
- ✅ Email automation security confirmed
- ⬜ Confirm ElevenLabs data handling configuration

### 6.2 Version Control
- ✅ GitHub repo created: https://github.com/ansteia/zipo-clinic-assistant
- ✅ V8 tagged and documented
- ✅ V10 released
- ⬜ Document full change log
- ⬜ Define version naming standard

---

## PHASE 7 — SCALABILITY & COMMERCIALISATION

### 7.1 White-Label Model
- ✅ Generic white-label structure created
- ⬜ Create white-label onboarding checklist
- ⬜ Create clinic onboarding template
- ⬜ Build pricing model

### 7.2 Sales Positioning
- ⬜ Build clinic pitch deck
- ⬜ Define ROI case study (Dr Marcus as pilot)
- ⬜ Create compliance positioning document

---

## PHASE 8 — RISK & EDGE CASE REVIEW

### 8.1 Emergency Escalation Review
- ⬜ Stress test urgent phrases
- ⬜ Confirm escalation consistency across scenarios

### 8.2 Abuse / Hostile User Handling
- ⬜ Define de-escalation protocol
- ⬜ Define termination conditions

---

## PHASE 9 — GOVERNANCE

### 9.1 Ownership
- ⬜ Define system owner (Adriana Mendivil)
- ⬜ Define medical content owner (Marcus)
- ⬜ Define update cadence

### 9.2 Quarterly Review Process
- ⬜ Review knowledge base
- ⬜ Review privacy policy
- ⬜ Review analytics metrics
- ⬜ Review system performance

---

## SUMMARY STATUS

| Area | Status |
|------|--------|
| Architecture | ✅ Complete |
| Compliance model | ✅ Complete |
| Zero data collection | ✅ Complete |
| Emotional safety | ✅ Complete |
| Analytics defined | ✅ Complete |
| Language detection | ✅ Complete (V10) |
| Reporting system | ⬜ Pending |
| Commercial packaging | ⬜ Pending |
| Technical verification | ⚠️ Partial — HTTPS ✅, Email ✅, Webhooks ⬜, ElevenLabs ⬜ |

---

## PROJECT CONTINUITY & DEPLOYMENT RECORD

**Status:** Active Development — Pre-Launch Hardening Phase
**Owner:** Adriana Mendivil
**Repository:** https://github.com/ansteia/zipo-clinic-assistant

### Project Intent

Zipo is a non-diagnostic, zero-data routing assistant embedded in Dr Marcus's website.

Primary objectives:
- Improve patient navigation
- Improve correct consultation allocation
- Reduce administrative load
- Increase system usage (HotDoc, referrals, scripts)
- Prevent unsafe medical information exposure
- Avoid personal data collection within chatbot
- Maintain privacy compliance (Australia)

### Core Architecture Decisions (FINAL)

> These decisions are **CLOSED** unless legally required to change.

**2.1 No Personal Data Collection**
- Zero personal identifiers collected
- No names, emails, phone numbers, Medicare numbers, DOB, medical history, or attachments
- All clinical or personal interaction redirected to secure contact form
- *Reason: Eliminate privacy liability at chatbot level*

**2.2 Resource-Only Medical Content**
- Zipo provides approved links only
- Does not generate independent medical explanations
- *Reason: Avoid misinformation and reduce medico-legal exposure*

**2.3 Emotional Safety Layer**
- Emotional language detection enabled
- Responds calmly, reassures without diagnosing
- Escalates emergency language to 000 instruction
- *Reason: Most users are vulnerable (elderly, anxious, in pain)*

**2.4 Anonymous Analytics Only**

Tracked:
- Menu selections, link clicks, topic category, routing outcomes, emotional detection events, satisfaction rating

Not tracked:
- Names, contact details, identifiers

Transcript handling:
- Temporarily retained, admin-only access, auto-delete after 30 days, not used for AI training

> **Storage note (provisional):** Analytics currently stored in Airtable. This is a temporary arrangement. Migration to a dedicated analytics platform is required before commercial scaling.

**2.5 Booking Logic**
- Simple issue → 30 min
- Complex/multiple → 45–60 min
- Redirect to HotDoc
- Booking failure → Contact form + clinic phone during business hours

### Risk Log

| Risk | Status |
|------|--------|
| Transcript retention | ✅ Resolved — no critical data collected; auto-deletion not required |
| Analytics storage | ⚠️ Provisional — Airtable (temporary); must migrate before scaling |
| No baseline metrics captured yet | ⚠️ Open |
| No external legal review | ⚠️ Open |
| Booking logic stress testing not completed | ⚠️ Open |

### Handover Instructions

If a new AI or human continues this project:
- **Do not** reintroduce data collection
- **Do not** allow medical advice generation
- **Do not** remove emergency notice
- **Do not** expand knowledge base beyond approved sources
- Verify transcript retention compliance before scaling
- Implement performance dashboard before commercial rollout
