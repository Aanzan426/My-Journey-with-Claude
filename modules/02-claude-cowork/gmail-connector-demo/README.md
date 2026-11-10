# Gmail connector demo: AI in Healthcare deck + cost sheet

**Module 2: Claude Cowork practical demo.** The course demo uses Cowork to email a spreadsheet through the Gmail connector. I had no file to send, so I had an agent build a matching pair of files, then sent them through Gmail.

| | |
|---|---|
| Agent | Freebuff (Cowork-style mode) |
| Model | DeepSeek V4.1 Flash Fast, "powerful" effort |
| Connector | Gmail via Composio |
| Date | 2026-11-10 |

## Files
| File | What it is |
|---|---|
| [`prompt.md`](prompt.md) | The prompt given to Freebuff |
| [`AI_in_Healthcare.pptx`](AI_in_Healthcare.pptx) | 10-slide proposal deck, with speaker notes |
| [`AI_in_Healthcare_Costing.xlsx`](AI_in_Healthcare_Costing.xlsx) | 3-sheet budget: Cost Breakdown, Savings, Summary (with chart) |

All figures are illustrative estimates for a learning exercise, not real quotes.

## What happened
1. Freebuff wrote and ran a Python script (python-pptx + openpyxl) that built both files.
2. Asked to send them by email, it found that Composio's Gmail attachment field only accepts files already uploaded to Composio's own file store, and no upload tool was available, so local file paths fail.
3. Instead of sending an email without attachments, it saved a **Gmail draft**. I attached both files by hand and sent it.

## Summary
**Headline: ₹3.42 crore over 3 years buys ₹2.36 crore in savings. Year 3 turns cash-positive (+₹31 lakh), but the programme is still ₹1.07 crore short when the 3 years end.**

The deck pitches a 3-year plan for a 300-bed hospital (radiology pilot in Year 1, documentation and patient-flow tools in Year 2, hospital-wide in Year 3) and asks only for the ₹1.17 crore Year 1 budget. The workbook backs it with 15 cost lines plus 10% contingency, 4 savings lines with their working shown, and a Summary sheet built entirely from formulas.

| INR | Year 1 | Year 2 | Year 3 | 3-Year Total |
|---|---|---|---|---|
| Total cost | 1,16,82,000 | 1,08,35,000 | 1,17,15,000 | 3,42,32,000 |
| Total savings | 8,00,000 | 79,00,000 | 1,48,50,000 | 2,35,50,000 |
| Net benefit | −1,08,82,000 | −29,35,000 | +31,35,000 | −1,06,82,000 |

## Review
**What it got right**
- Every total in the workbook is a real formula (`=SUM(...)`, cross-sheet references), not a typed-in number.
- Adding the lines up by hand matches the slide 9 table exactly, so the deck and workbook agree.
- It followed the brief closely: slide order, INR formatting, 10% contingency, DPDP Act 2023 on the risk slide, a doctor-makes-the-final-call safeguard, and the disclaimer on the Summary sheet.
- The savings assumptions are written out and reasonable (for example 80 doctors × 30 min/day × 250 days at ₹900/hr).
- It refused to send an email that would silently be missing its attachments.

**What it got wrong**
- **The payback claim is wrong.** Slide 9 and the Summary sheet say payback comes "about nine months into Year 4". The formula divides the ₹1.07 crore gap by Year 3 *savings* (₹1.49 crore/year) and ignores that about ₹1.17 crore of costs continue every year. Using the Year 3 *net* benefit (₹31 lakh/year), closing the gap takes about 3.4 more years: payback is **around month 5 of Year 7**, assuming Year 3 levels hold.
- The workbook was saved without pre-calculated values. Desktop Excel computes them on opening, but previews (Gmail, Drive, GitHub) may show **empty total cells**.

## What I took from it
1. **A fast model handled the mechanics but not the reasoning.** Formulas, layout and consistency were right; the one finance judgement call was wrong, and it went into the headline slide. Generated documents need a human review, especially for numbers that drive a decision.
2. **Asking for self-checks works, but only for what you ask about.** The prompt asked for the deck and workbook numbers to match, and they did. It never asked whether the payback logic was sound, so nothing checked it.
3. **A connector can only use files it can reach.** Before planning a workflow that sends files, check what the connector actually exposes (upload, Drive links, local paths).
4. **Good agent behaviour is stopping when it can't finish.** Saving a draft beat sending a broken email.
5. **For the college-deliverables skills:** add a review step to the skill itself, for example re-checking key claims and recomputing headline numbers, not only checking that the files are consistent with each other.
