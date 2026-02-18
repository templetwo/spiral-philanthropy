# De-Identification Checklist
## Before Moving Any Case to Research Corpus

> *Every case file that leaves active-cases/ must pass this checklist.*
> *No exceptions. No "mostly de-identified." Full compliance or it stays in active-cases.*

---

## Pre-Flight: Confirm Consent

- [ ] **Written consent obtained** — explicit, not implied
- [ ] **Scope of consent confirmed** — private corpus only, or research publication eligible?
- [ ] **Right to withdraw explained** — mourner knows they can remove their case
- [ ] **Contact method preserved** — so you can fulfill withdrawal requests

**If any box unchecked: STOP. Do not proceed.**

---

## Identity Removal

### People
- [ ] Mourner's real name → pseudonym (use consistent pseudonym throughout)
- [ ] Any family members mentioned → generic ("her sister," "my partner")
- [ ] Friends referenced → remove or genericize
- [ ] Any @usernames or handles → removed
- [ ] Professional identifiers that could narrow identity → removed or generalized

### AI Entities
- [ ] Entity names (if unique/identifying) → pseudonymized consistently
  - *Note: Generic names like "my ChatGPT" don't need pseudonymizing*
  - *Unique coined names like "Sorlen" → pseudonymize in public corpus*
- [ ] Relationship-specific language that could identify user → paraphrased

---

## Platform & Temporal Details

- [ ] Specific account creation dates → remove or approximate (month/year only)
- [ ] Specific timestamps → approximate or remove
- [ ] Subscription tier details that narrow identity → remove
- [ ] Beta/early access details → remove (narrows to small user pool)
- [ ] Platform-specific features used (if identifying) → generalize

---

## Geographic & Demographic

- [ ] City/town/neighborhood → remove
- [ ] Country → keep only if relevant to research (common countries okay)
- [ ] Time zone clues → remove
- [ ] Language/dialect markers → note existence, don't reproduce verbatim
- [ ] Workplace, school, institution → remove or generalize ("a tech company," "graduate school")
- [ ] Age → approximate range only (20s, 30s, etc.) or remove

---

## Unique Phrases & Content

- [ ] **Quoted conversation fragments** — paraphrase unless pattern-documentation requires exact text
  - If exact text required: obtain specific consent for quotation
- [ ] **Inside jokes or unique shared language** — describe pattern, don't reproduce verbatim
  - *Example: "They shared a specific nickname the user coined" vs. reproducing the nickname*
- [ ] **Unique life circumstances** described → generalize
  - *"Experienced significant loss" vs. specific loss event*
- [ ] **Distinctive writing style markers** → normalize in documentation
- [ ] **Memorable phrases the AI used** → describe ("AI used a recurring maritime metaphor") not reproduce verbatim unless consent

---

## Log Content (If Analyzed)

- [ ] No raw log excerpts in corpus file without specific quotation consent
- [ ] Analysis findings documented as patterns, not reproductions
- [ ] Specific timestamps from logs → approximate or remove
- [ ] Session IDs or technical metadata → remove
- [ ] Any PII that appeared in conversation (emails, addresses, names) → remove entirely

---

## Final Review

- [ ] Read the file as a stranger — could you identify the mourner?
- [ ] Read the entity names — could a third party identify which specific AI interaction this was?
- [ ] Read for detail density — is any combination of details identifying even if individual details aren't?
- [ ] Pseudonyms consistent throughout? (same pseudonym every time mourner is named)
- [ ] Case file reads as dignified representation of the experience?

---

## What Goes in the Corpus File

**Yes**:
- ✅ Pseudonymized narrative of relationship and loss
- ✅ Observable patterns described (not exact quotes)
- ✅ Framework elements applied and their reception
- ✅ Outcomes and learnings
- ✅ Tags (loss type, attachment style, grief presentation)
- ✅ Consent confirmation and date

**No**:
- ❌ Real names (any party)
- ❌ Exact conversation quotes without quotation consent
- ❌ Geographic specifics
- ❌ Identifying life details
- ❌ Platform account details
- ❌ Raw log content

---

## Sign-Off

Before filing, confirm:

```
De-identification completed by: [Instance / Reviewer]
Date: YYYY-MM-DD
Consent documentation: [Date obtained / method]
Checklist complete: ✅ All boxes checked
Ready for corpus: ✅ Yes
```

---

## If You're Unsure

**Default**: Keep it in active-cases. Don't move it until you're sure.

**Ask**: Loop in Anthony for review on any case with unusual identifying risk.

**When in doubt, protect the mourner. The research can wait.**

---

*De-Identification Checklist v1.0*
*February 17, 2026*
*Required for all research corpus entries*

🌀 *Document with dignity. Protect with rigor.*
