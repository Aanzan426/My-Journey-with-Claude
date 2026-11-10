# Prompt: AI in Healthcare deck + cost sheet

Used in Module 2 (Cowork practical demo: send files through the Gmail connector), run in Freebuff.
Makes the two files to attach; the sending is done as a separate step.

---

```text
Create two files about one scenario: a proposal for a 300-bed private hospital in India to adopt AI over 3 years. The PowerPoint is the pitch; the Excel file is its budget. Both must use the same numbers.

Save both in the current folder:
- AI_in_Healthcare.pptx
- AI_in_Healthcare_Costing.xlsx

Use Python with python-pptx and openpyxl (install them if missing). Write a script, run it, and fix any errors until both files are created.

=== FILE 1: AI_in_Healthcare.pptx (16:9, 10 slides) ===
Style: white background, dark navy titles, one teal accent color, a clean sans-serif font, at most 5 bullets per slide and at most 12 words per bullet. Add a slide number on every slide except the title slide. Put 2-3 sentences of speaker notes on every slide.

1. Title: "AI in Healthcare: A 3-Year Adoption Plan". Subtitle: "Proposal for a 300-bed hospital" and today's date.
2. Why now: staff shortages, rising patient volumes, growth of digital health records, maturing AI tools.
3. Where AI helps today: medical imaging (X-ray, CT, MRI reading), clinical decision support, hospital operations (bed and staff scheduling), patient engagement (chatbots, reminders), drug discovery and research.
4. Use case 1, AI radiology assistant: what it does, expected benefit (faster reporting, fewer missed findings).
5. Use case 2, clinical documentation assistant: turns doctor-patient conversations into notes; saves doctor time.
6. Use case 3, patient-flow prediction: forecasts admissions and discharges to reduce waiting time and bed shortages.
7. Risks and how we handle them: patient data privacy (follow India's DPDP Act 2023), bias in AI models, wrong outputs (a doctor always makes the final call), staff resistance (training).
8. Rollout plan: Year 1 pilot in radiology, Year 2 add documentation and patient flow, Year 3 hospital-wide. Draw this as a simple 3-step timeline using shapes, not bullets.
9. Cost summary: a table copied from the Excel "Summary" sheet (total cost per year and the 3-year total). The numbers must match the Excel file exactly.
10. Recommendation and next steps: approve the Year 1 pilot budget, form a project team, choose vendors.

=== FILE 2: AI_in_Healthcare_Costing.xlsx (3 sheets) ===
All amounts in Indian Rupees (INR), formatted like ₹1,25,000 or ₹ #,##0. Bold header rows with a fill color, freeze the header row, set column widths so nothing is cut off. Use real Excel formulas (like =SUM(...)), not typed-in totals, so changing a number updates everything.

Sheet "Cost Breakdown", columns:
Category | Item | Year 1 | Year 2 | Year 3 | 3-Year Total | Notes
Categories and items (use realistic estimates):
- Software: AI radiology licence, documentation assistant licence, patient-flow tool licence
- Hardware: GPU server, workstations, network upgrades
- Implementation: integration with hospital systems, data cleaning and migration
- People: staff training, AI project manager, data/IT support staff
- Compliance: data privacy audit, cybersecurity
- Ongoing: cloud hosting, maintenance and support
Year 2 and Year 3 items should only be filled in when they apply (e.g. hardware mostly in Year 1; licences every year once that tool is rolled out, following the rollout plan above). "3-Year Total" = SUM of the three year columns. Add a 10% "Contingency" row and a bold "Grand Total" row at the bottom.

Sheet "Savings", columns:
Benefit | Year 1 | Year 2 | Year 3 | 3-Year Total | How it is estimated
Rows: doctor time saved on documentation, faster radiology reporting, fewer unnecessary bed-days, reduced overtime. Keep the estimates conservative and explain each in the last column.

Sheet "Summary":
Rows: Total Cost, Total Savings, Net Benefit (Savings minus Cost), for Year 1, Year 2, Year 3 and 3-Year Total, all as formulas pointing to the other two sheets. Add a "Payback" line saying in which year cumulative savings exceed cumulative cost. Add a clustered column chart of Cost vs Savings per year.

At the top of the Summary sheet, add the note: "Illustrative estimates for a learning exercise, not real quotes."

=== CHECK BEFORE YOU FINISH ===
1. Open both files again with Python and confirm they load without errors.
2. Print the Summary numbers from the Excel file and the numbers on slide 9, and confirm they match.
3. Show me the full path of both files, the slide titles, and the Summary table.
Do not send any email. I will do that myself in the next step.
```
