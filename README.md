# Slovakia Legal Research MCP Server (`sk-legal-mcp`)

**[Slovenčina](#lang-sk) | [English Documentation](#english-documentation)**

---

<a id="lang-sk"></a>
## Právny MCP server pre legislatívu a judikatúru SR (`sk-legal-mcp`) — Slovenčina

### O tomto repozitári

Tento repozitár obsahuje Model Context Protocol (MCP) server, ktorý prepája vašu AI aplikáciu (Claude Desktop, Cursor, Windsurf, VS Code / Copilot, Cline alebo Antigravity) s portálom Slov-Lex (`slov-lex.sk`) a databázou rozhodnutí okresných, mestských, správnych, krajských a najvyšších súdov SR (`obcan.justice.sk`).

### Rýchla inštalácia (Výber AI aplikácie)

1. **Stiahnutie:** Kliknite vpravo hore na **`<> Code` -> `Download ZIP`** a rozbaľte priečinok v počítači.
2. **Spustenie:** Dvakrát kliknite na **`Click_Here_To_Install_Windows.bat`** (Windows) alebo **`Click_Here_To_Install_Mac.command`** (macOS).
3. **Výber AI klienta:** Označte AI programy, ktoré používate (Claude, Cursor, Windsurf, VS Code, Antigravity), kliknite na inštaláciu a reštartujte vybranú AI aplikáciu.

**Bezpečnostná poznámka:** Inštalátor pracuje výlučne v režime čítania (read-only) a nepristupuje k vašim osobným súborom.

### Sústava súdov a oficiálne zdroje

| Súdna inštancia | Zahrnuté súdy |
|:---|:---|
| **1. stupeň (Okresné, mestské a správne súdy)** | Okresné súdy (District Courts), Mestské súdy (Bratislava & Košice) & Správne súdy (Bratislava, Banská Bystrica, Košice) |
| **2. stupeň (8 Krajských súdov a Špecializovaný trestný súd)** | 8 Krajských súdov (Regional Courts: Bratislava, Trnava, Trenčín, Nitra, Žilina, Banská Bystrica, Prešov, Košice) & Špecializovaný trestný súd |
| **Najvyšší súd SR, NSS SR a Ústavný súd SR** | Najvyšší súd SR (NSSR), Najvyšší správny súd SR (NSS SR) & Ústavný súd SR |

- **Slov-Lex Legal and Information Portal (slov-lex.sk):** [https://www.slov-lex.sk](https://www.slov-lex.sk) (`slov-lex.sk`, `zakonypreludi.sk`, `nrsr.sk`)
- **Otvorené súdy / Ministerstvo spravodlivosti SR - Rozhodnutia všetkých súdov (obcan.justice.sk):** [https://obcan.justice.sk/infosud/-/infosud/zoznam/rozhodnutie](https://obcan.justice.sk/infosud/-/infosud/zoznam/rozhodnutie) (`justice.gov.sk`, `obcan.justice.sk`, `nsud.sk`, `ustavnysud.sk`, `nssud.sk`)

---

<a id="english-documentation"></a>
## English Documentation

Model Context Protocol (MCP) server providing live, read-only access to **Slovakia (SK)** legislation, official gazettes, multi-tier judicial decisions (First Instance, Regional/Cantonal/Appellate, and Supreme/Constitutional courts, including HTML and PDF full-text extraction), and statutory citation verification across all major AI clients (**ChatGPT Desktop, OpenAI Codex CLI, Claude Desktop, Claude Code CLI, Cursor, Windsurf, VS Code / GitHub Copilot / Cline / Roo Code, Google Antigravity / Gemini CLI, Perplexity, and Continue.dev**).

---

### Interactive Desktop Setup (Select Your AI Assistant)

This package includes a graphical installer for legal practitioners and non-technical users that lets you select which AI application(s) you use:

1. **Download:** Click **`<> Code`** at the top right of this repository, select **`Download ZIP`**, and extract the folder to your computer.
2. **Run the Setup Utility:**
   - **Windows:** Double-click `Click_Here_To_Install_Windows.bat`
   - **macOS:** Double-click `Click_Here_To_Install_Mac.command`
3. **Select Your AI Client(s) & Connect:** Check the box(es) for the AI assistant(s) installed on your computer (**ChatGPT Desktop & OpenAI Codex CLI**, **Claude Desktop & Claude Code CLI**, **Cursor**, **Windsurf**, **VS Code / GitHub Copilot / Cline / Roo Code**, **Google Antigravity / Gemini CLI**, or **Perplexity / Continue.dev**), click **Install to Selected AI Clients**, and restart your selected AI application.

**System Integrity Note:** The setup utility operates strictly in read-only mode with respect to your personal files and documents. It installs an isolated Python runtime inside the extracted folder and registers the server entry only in the AI client configuration files you select.

---

### Multi-Tier Judicial Hierarchy & Live Indexed National Archives

This server performs live queries across the full judicial hierarchy and official legal archives of **Slovakia**, extracting full text from both HTML pages and official court/gazette PDF judgments:

| Judicial Tier | Covered Courts & Tribunals |
|:---|:---|
| **Tier 1 — First Instance** | Okresné súdy (District Courts), Mestské súdy (Bratislava & Košice) & Správne súdy (Bratislava, Banská Bystrica, Košice) |
| **Tier 2 — Regional / Cantonal / Appellate** | 8 Krajských súdov (Regional Courts: Bratislava, Trnava, Trenčín, Nitra, Žilina, Banská Bystrica, Prešov, Košice) & Špecializovaný trestný súd |
| **Tier 3 — Supreme & Constitutional** | Najvyšší súd SR (NSSR), Najvyšší správny súd SR (NSS SR) & Ústavný súd SR |

#### Official Portals & Live Indexed Domains

- **National Legislation & Official Gazette:** Slov-Lex Legal and Information Portal (slov-lex.sk) — [https://www.slov-lex.sk](https://www.slov-lex.sk)
  - *Indexed Legislation Domains:* `slov-lex.sk`, `zakonypreludi.sk`, `nrsr.sk`
- **Court Decisions & Jurisprudence Archives:** Otvorené súdy / Ministerstvo spravodlivosti SR - Rozhodnutia všetkých súdov (obcan.justice.sk) — [https://obcan.justice.sk/infosud/-/infosud/zoznam/rozhodnutie](https://obcan.justice.sk/infosud/-/infosud/zoznam/rozhodnutie)
  - *Indexed Judicial & Open Case Law Domains:* `justice.gov.sk`, `obcan.justice.sk`, `nsud.sk`, `ustavnysud.sk`, `nssud.sk`

---

### Available MCP Tools

| Tool | Description |
|:---|:---|
| `search_legislation` | Searches enacted statutes, codes, decrees, and official gazette publications in Slovakia. |
| `search_case_law` | Searches national jurisprudence and open judicial archives for Slovakia. |
| `search_tiered_court_decisions` | Filters case law specifically by judicial instance (`first_instance`, `appellate_regional`, `supreme_constitutional`) or specific regional/cantonal/district court. |
| `list_court_hierarchy` | Returns the complete 3-tier court structure and supported regional court filters for Slovakia. |
| `get_legal_document_markdown` | Retrieves full statutory or judicial texts (both HTML and official `.pdf` court judgments) and converts them into clean Markdown. |
| `verify_citation` | Validates statutory and case law citations against official registries. |

---

<details>
<summary><b>Manual Configuration for Developers (Optional)</b></summary>

```json
{
  "mcpServers": {
    "sk-legal-mcp": {
      "command": "uvx",
      "args": [
        "--from",
        "https://github.com/jurisatlas/sk-legal-mcp/archive/refs/heads/main.zip",
        "sk-legal-mcp"
      ]
    }
  }
}
```
</details>
