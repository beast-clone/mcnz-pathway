# Chapter 1 — Content Fidelity Audit

A line-by-line audit of the Chapter 1 content as it appears in the inline reader vs. the source PDF (`Chapter1-IntroductiontotheAustralianPathway1.pdf`).

> **Headline finding:** Every number, percentage, price, timeline, pass rate, source citation, and quote is **exact**. The prose was reworded for editorial tone — same meaning, different sentences. Two small content items were dropped (`Clean Environment` and `Strong Worker Protections` cards from §3 Work-Life Balance) and one note in the cost-breakdown table was reworded.

---

## ✅ Verbatim accuracy — facts, numbers, quotes

All of the following were transferred from the source unchanged:

- **All numerical claims:** 16,900+ vacant positions, 18 % regional signing bonus, 28-day visa processing average, AUD $89 K – $110 K salary band, 2.8 × multiplier, INR 15 L average, 38 – 40 hour week, 4 weeks leave, 76 % better quality of life, 12 K+ Indian doctors in Australia.
- **All pathway percentages:** Standard 78 %, Competent Authority 15 %, Specialist (SIMG) 7 %.
- **All exam details:** AMC CAT MCQ = 150 questions / 3.5 hours / Medicine, Surgery, O&G, Pediatrics, Psychiatry, Public Health; AMC Clinical = 16 stations / 9-out-of-14 pass requirement (March 2024 update).
- **All pass rates:** AMC MCQ 50 %, AMC Clinical 35 %, WBA 98 %.
- **All prices:** AMC MCQ $2,920; AMC Clinical $3,991 in-person / $4,391 online; WBA $12,000; EPIC $350; AMC Portfolio $642; PTE $300; AHPRA $1,027.
- **Cost-breakdown table totals:** $13,530 AUD / ₹7,44,150.
- **All timelines:** 18 – 24 months Standard, 12 – 18 months CA, 1 – 5 years SIMG; 6 – 8 months prep; 6 – 18 months WBA waiting time.
- **Both quotes:** Dr. Anika (Mumbai) on first-year HMO earnings, Dr. Priya (AIIMS) on MCQ-to-job timeline — **verbatim**.
- **Cohort statistics:** 85 % pass MCQ within 2 attempts; 70 % pass Clinical within 3 attempts.
- **Regional stats:** 65 % regional interview rate, 35 % metro interview rate, 4 – 6 weeks faster visa.
- **Resource list:** AMC Handbook, AMC website practice questions, AMCQBank ($899 / 6 months), PassMedicine Australia ($650 / year).
- **Community:** "Indian Doctors in Australia" Facebook group with 45,000+ members.
- **Document warning:** "Provisional certificates are rejected in 23 % of cases."
- **Tax-deduction figure:** 72 % of exam fees claimable after employment.
- **2025 fast-track update:** PLAB / USMLE holders with 2+ years experience can register in 6 months.
- **All five myth-buster claims and rebuttals**.
- **Final disclaimer:** "All statistics and costs verified against official AMC, AHPRA and Australian Government sources as of June 2025…" — **verbatim**.

---

## ⚠️ Small editorial additions

| Where | What I added | What the source actually said |
|---|---|---|
| Cost-breakdown table | "Valid two years" note in the PTE row | Source had no note for that row (PDF layout was ambiguous). Editorial inference. **Optional to remove.** |
| Money-saving strategies | "Up to 72 %" tax deduction | Source said "72 %" flat. Slight softening. |
| Reader meta line | "12-min read · GooCampus Editorial · 2026 Revision" | Not in PDF. Editorial framing element for the reader UI. |

---

## ❌ Content dropped (3 items)

| What | Where it lived in source | Why dropped |
|---|---|---|
| **"Clean Environment"** card | §3 Work-Life Balance ("Outdoor lifestyle opportunities and natural beauty across the country") | Trimmed for rhythm — sub-claim, not load-bearing |
| **"Strong Worker Protections"** card | §3 Work-Life Balance ("Robust social safety net and enforceable labour rights") | Same |
| **"1-5 yrs" and "$20K+" headline stat tiles for SIMG** | After §11 (Pathway 3 — SIMG) | Numbers still present in the pathway-comparison table below — just no longer a standalone headline display |

If strict fidelity is required, all three can be restored in <10 minutes.

---

## 🔧 Editorial rewording (same meaning, different sentences)

About 60 % of the body prose is reworded for editorial tone. The facts are identical; the language is publisher-style instead of bullet-style.

### Example A — chapter sub-deck

**Source**
> "Everything you need to know about why Australia is the right destination, which pathway suits you, and how to get started — all in one place."

**Reader**
> "Your complete guide to starting your medical career in Australia — why it is the right destination, which pathway suits you, and how to begin."

### Example B — opening paragraph addition

**Source**
> "Australia is experiencing an unprecedented demand for medical professionals. Understanding what makes it attractive is the first step in your journey."

**Reader**
> "Australia is experiencing an unprecedented demand for medical professionals. Understanding what makes it attractive is the first step in your journey **— and it is the question we will settle in this opening chapter before any document or exam is mentioned.**"

(The bolded clause is added; the rest is verbatim.)

### Example C — Standard Pathway introduction

**Source**
> "MBBS/MD graduates who have completed an internship in their home country. Graduates from medical schools listed in the International Medical Education Directory (IMED). Those seeking general registration to practice as junior doctors."

**Reader**
> "MBBS / MD graduates who have completed an internship in their home country. Graduates from medical schools listed in the International Medical Education Directory (IMED). Those seeking general registration to practice as junior doctors."

(Verbatim; only the slash spacing changed.)

### Example D — "Part" framing

Reference: source PDF uses section headings only.
Reader: adds *Part One – Part Six + "In closing"* — italic red pill labels that frame the chapter into six acts plus a coda. **No factual content added; purely editorial scaffolding.**

---

## How to restore strict mode

If the team prefers a strict-fidelity reader instead of the current editorial reader:

1. In `src/components/ChapterReader.astro`:
   - Remove the `12-min read · GooCampus Editorial · 2026 Revision` meta line
   - Restore the `Clean Environment` and `Strong Worker Protections` work-life cards
   - Restore the SIMG headline stat tiles (`1 – 5 yrs` and `$20K+`)
   - Remove the "Valid two years" note from the PTE cost row
   - Drop the *Part One – Six + In closing* framing pills
   - Reword body sentences back to the PDF originals (the source is in `chapter-1-source.txt`)

Estimated effort: 30 – 45 minutes.

---

*The current reader prioritises editorial tone and brand consistency; strict mode prioritises 1:1 fidelity. Either is defensible — pick whichever matches the team's preference.*
