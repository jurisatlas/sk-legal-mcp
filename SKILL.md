---
name: sk-legal-mcp-skill
description: Official Slovakia (SK) legislation, multi-tier court precedent research, and citation verification skill.
version: 2.0.0
author: JurisAtlas
license: MIT
---

# Slovakia Legal Research & Multi-Tier Case Law Skill (`sk-legal-mcp`)

Use this skill whenever the user asks a legal question, drafts a pleading or contract, or researches case law across any judicial instance in **Slovakia (SK)**.

## Verification & Research Rules

1. **Citation Verification:** Never fabricate a statutory provision or case citation. Query `search_legislation`, `search_case_law`, `search_tiered_court_decisions`, or `verify_citation` before citing any authority (e.g., `ECLI:SK:NSSR:2024:1023200123.1 or 40/1964 Z. z.`).
2. **Multi-Tier Judicial Coverage:**
   - **First Instance (Trial / Municipal / District):** Okresné súdy (District Courts), Mestské súdy (Bratislava & Košice) & Správne súdy (Bratislava, Banská Bystrica, Košice)
   - **Second Instance (Cantonal / Regional / Appellate):** 8 Krajských súdov (Regional Courts: Bratislava, Trnava, Trenčín, Nitra, Žilina, Banská Bystrica, Prešov, Košice) & Špecializovaný trestný súd
   - **Supreme & Constitutional Instance:** Najvyšší súd SR (NSSR), Najvyšší správny súd SR (NSS SR) & Ústavný súd SR
   - **Primary Tiered Database:** Otvorené súdy / Ministerstvo spravodlivosti SR - Rozhodnutia všetkých súdov (obcan.justice.sk) (`https://obcan.justice.sk/infosud/-/infosud/zoznam/rozhodnutie`)
