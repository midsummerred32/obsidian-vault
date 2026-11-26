---
tags:
---

---

# Service, Clinical & Shadowing Dashboard

## Undergrad & Pre-Med Totals (AMCAS Ready)
```dataview
TABLE WITHOUT ID
  key AS "Category",
  length(rows) AS "Entries",
  sum(rows.L.hours) AS "Total Hours"
FROM ""
WHERE file.path = this.file.path
FLATTEN file.lists AS L
WHERE L.hours AND L.era = "Undergrad"
GROUP BY L.category
```

## High School Totals (Common App / NHS)
```dataview
TABLE WITHOUT ID
  key AS "Category",
  length(rows) AS "Entries",
  sum(rows.L.hours) AS "Total Hours"
FROM ""
WHERE file.path = this.file.path
FLATTEN file.lists AS L
WHERE L.hours AND L.era = "High School"
GROUP BY L.category
```

## Activity & Organization Rollup (All Eras)
```dataview
TABLE WITHOUT ID
  rows.L.era[0] AS "Era",
  rows.L.category[0] AS "Category",
  rows.L.org[0] AS "Organization",
  min(rows.L.date) + " to " + max(rows.L.date) AS "Date Range",
  sum(rows.L.hours) AS "Total Hours",
  rows.L.contact[0] AS "Verifier / Contact"
FROM ""
WHERE file.path = this.file.path
FLATTEN file.lists AS L
WHERE L.hours
GROUP BY L.era + " - " + L.category + " - " + L.org
SORT rows.L.era[0] DESC, sum(rows.L.hours) DESC
```

## Physician Shadowing Breakdown
```dataview
TABLE WITHOUT ID
  rows.L.specialty[0] AS "Specialty",
  rows.L.provider[0] AS "Physician (MD/DO)",
  rows.L.org[0] AS "Hospital / Clinic",
  sum(rows.L.hours) AS "Hours",
  rows.L.contact[0] AS "Contact Info"
FROM ""
WHERE file.path = this.file.path
FLATTEN file.lists AS L
WHERE L.category = "Shadowing"
GROUP BY L.specialty + " - " + L.provider
SORT sum(rows.L.hours) DESC
```

---

## Master Log
*Templates for new entries (change `[era:: ]` to `Undergrad` after high school graduation):*
* **Non-Clinical Volunteering:** `- [era:: Undergrad] [category:: Community Service] [org:: ] [activity:: ] [date:: YYYY-MM-DD] [hours:: 0.00] [contact:: Name, Title - Email/Phone]`
* **Clinical Volunteering / Paid:** `- [era:: Undergrad] [category:: Clinical Experience] [org:: ] [activity:: ] [date:: YYYY-MM-DD] [hours:: 0.00] [contact:: Name, Title - Email/Phone]`
* **Physician Shadowing:** `- [era:: Undergrad] [category:: Shadowing] [org:: ] [provider:: Dr. Name, MD/DO] [specialty:: ] [activity:: ] [date:: YYYY-MM-DD] [hours:: 0.00] [contact:: Email/Phone]`

- [era:: High School] [category:: Community Service] [org:: Macedonia Rec] [activity:: Soccer Practice] [date:: 2023-08-14] [hours:: 1.25] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Macedonia Rec] [activity:: Soccer Practice] [date:: 2023-08-21] [hours:: 1.25] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Macedonia Rec] [activity:: Soccer Scrimage] [date:: 2023-08-26] [hours:: 3.00] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Macedonia Rec] [activity:: Soccer Practice] [date:: 2023-08-28] [hours:: 1.25] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Macedonia Rec] [activity:: Soccer Game] [date:: 2023-09-09] [hours:: 2.50] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Macedonia Rec] [activity:: Soccer Game] [date:: 2023-09-16] [hours:: 2.00] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Macedonia Rec] [activity:: Soccer Practice] [date:: 2023-09-18] [hours:: 1.25] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Macedonia Rec] [activity:: Soccer Practice] [date:: 2023-09-25] [hours:: 1.25] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Macedonia Rec] [activity:: Soccer Game] [date:: 2023-09-30] [hours:: 2.00] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Macedonia Rec] [activity:: Soccer Game] [date:: 2023-10-07] [hours:: 2.00] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Macedonia Rec] [activity:: Soccer Game] [date:: 2023-10-17] [hours:: 2.00] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Scouts BSA] [activity:: Cub Haunted] [date:: 2023-10-21] [hours:: 9.00] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Scouts BSA] [activity:: Yard Charge] [date:: 2023-11-11] [hours:: 3.00] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Nordonia Boys Volleyball] [activity:: Mulch Madness] [date:: 2024-05-05] [hours:: 3.00] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Student Council] [activity:: Special Olympics] [date:: 2024-05-10] [hours:: 5.00] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Nordonia Boys Volleyball] [activity:: Mulch Madness] [date:: 2024-05-19] [hours:: 3.00] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Macedonia Rec] [activity:: Soccer Practice] [date:: 2024-08-12] [hours:: 1.00] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Macedonia Rec] [activity:: Soccer Practice] [date:: 2024-08-19] [hours:: 1.00] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Macedonia Rec] [activity:: Soccer Practice] [date:: 2024-08-26] [hours:: 1.00] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Macedonia Rec] [activity:: Soccer Game] [date:: 2024-08-31] [hours:: 2.00] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Macedonia Rec] [activity:: Soccer Game] [date:: 2024-09-07] [hours:: 2.00] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Macedonia Rec] [activity:: Soccer Practice] [date:: 2024-09-09] [hours:: 1.00] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Macedonia Rec] [activity:: Soccer Game] [date:: 2024-09-14] [hours:: 2.00] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Macedonia Rec] [activity:: Soccer Practice] [date:: 2024-09-16] [hours:: 1.00] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Macedonia Rec] [activity:: Soccer Game] [date:: 2024-09-21] [hours:: 2.00] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Macedonia Rec] [activity:: Soccer Practice] [date:: 2024-09-23] [hours:: 1.00] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Macedonia Rec] [activity:: Soccer Game] [date:: 2024-09-28] [hours:: 2.00] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Macedonia Rec] [activity:: Soccer Practice] [date:: 2024-09-30] [hours:: 1.00] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Macedonia Rec] [activity:: Soccer Game] [date:: 2024-10-05] [hours:: 2.00] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Macedonia Rec] [activity:: Soccer Practice] [date:: 2024-10-07] [hours:: 1.00] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Macedonia Rec] [activity:: Soccer Game] [date:: 2024-10-12] [hours:: 2.00] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Macedonia Rec] [activity:: Soccer Practice] [date:: 2024-10-14] [hours:: 1.00] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Macedonia Rec] [activity:: Soccer Game] [date:: 2024-10-19] [hours:: 2.00] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Student Council] [activity:: Special Olympics] [date:: 2025-05-02] [hours:: 5.00] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Nordonia Boys Volleyball] [activity:: Mulch Madness] [date:: 2025-05-17] [hours:: 4.00] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Scouts BSA] [activity:: Yard Charge] [date:: 2025-11-15] [hours:: 5.50] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Scouts BSA] [activity:: Eagle Scout Project] [date:: 2025-11-22] [hours:: 24.00] [contact:: ]
- [era:: High School] [category:: Community Service] [org:: Student Council] [activity:: Miles for Smiles] [date:: 2026-05-08] [hours:: 4.00] [contact:: ]