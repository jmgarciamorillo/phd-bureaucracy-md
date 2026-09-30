# PhD Bureaucracy Framework (`phd-bureaucracy-md`)

An AI-assisted, Markdown-first framework designed to streamline the drafting, tracking, and management of recurring doctoral monitoring reports and bureaucratic milestones throughout your PhD studies.

Originally created for the doctoral procedures at the **Universidad de Granada (UGR)**, this repository is architected as an adaptable, reusable framework for any university or doctoral programme.

Please, note that the documents needed for other institutions may differ. Adapt the repository accordinlgy.

---

## 💡 How It Works

Doctoral reporting can be repetitive and fragmented across years. This framework centralizes your academic information into clean Markdown documents and uses an LLM assistant (guided by [`AGENTS.md`](AGENTS.md)) to turn brief, informal notes into publication-grade, official administrative reports ready for submission.

```
                      ┌────────────────────────────┐
                      │   fixed_data/              │
                      │   (Static PhD metadata,    │
                      │    research plan, codes)   │
                      └─────────────┬──────────────┘
                                    │
                                    ▼
┌───────────────────────────┐               ┌───────────────────────────┐
│ current_year/             │   AI Agent    │ history/                  │
│ (Your rough, informal     │ ────────────> │ (Clean, official drafted  │
│  notes for the eval year) │  (AGENTS.md)  │  Markdown reports ready   │
└───────────────────────────┘               │  to copy-paste/archive)   │
                                            └───────────────────────────┘
```

---

## 📁 Repository Structure

```text
.
├── AGENTS.md                  # System prompt & rules governing agent drafting behavior
├── fixed_data/                # Permanent PhD information (single source of truth)
│   ├── PHD_DATA.md            # Student, advisors, and thesis metadata
│   ├── BASE_RESEARCH_PLAN.md  # Multi-year baseline research plan & objectives
│   └── ACTIVITY_CODES.md      # Official catalog of doctoral activity codes (e.g. UGR DAD)
├── current_year/              # Notes and activities for the year under evaluation
│   └── ACTIVITIES_LOG_XXXX.md # Rough log of courses, progress, and publication status
├── templates/                 # Reference layouts and official institutional templates
│   ├── annual_monitoring_report.doc
│   ├── researach_plan.doc
│   └── training_plan.pdf
└── history/                   # Generated final reports across academic years
```

---

## 🚀 Getting Started: How to Use This Repo

### 1. Initial Setup (One-time)

1. **Configure your metadata in [`fixed_data/PHD_DATA.md`](/fixed_data/PHD_DATA.md):**  
   Replace the example data with your name, institution, student ID, thesis title, advisors, tutor, and any other relevant information.
2. **Define your initial plan in [`fixed_data/BASE_RESEARCH_PLAN.md`](/fixed_data/BASE_RESEARCH_PLAN.md):**  
   Outline your main research objectives, methodologies, and target publication milestones with no need of formal and thorough explainations.
3. **Verify activity codes in [`fixed_data/ACTIVITY_CODES.md`](/fixed_data/ACTIVITY_CODES.md):**  
   Pre-filled with official UGR codes (`ED1CTI`, `PD3`, `EIP8`, etc.). Update or extend them if your doctoral programme uses a different catalog.
4. **Generate initial documents:**
   Generate the first research and traning plans, so that the agent can use them in the next years to create subsequent information. They will serve as a baseline for future updates. Use the `history/` directory to store them.

### 2. Routine Yearly Workflow (Generating Reports)

1. **Jot down your notes:**  
   During the academic year, append informal notes, conferences attended, courses taken, and publication progress into `current_year/ACTIVITIES_LOG_YYYY.md`.
2. **Ask your AI assistant:**  
   Prompt your coding assistant or LLM in your IDE (e.g., Antigravity, Claude, ChatGPT, Cursor):
   > *"Draft my annual progress report for academic year 2025–2026 based on my activities log and history."*
3. **Review & Copy-Paste:**  
   The agent will read [`AGENTS.md`](AGENTS.md), cross-reference your history, and generate strictly compliant, anti-AI academic text formatted into independent code blocks. Copy the text directly into your template (e.g. doc, pdf) and they will be ready to be signed.
4. **Archive:**  
   Save the generated report in `history/annual_report_YYYY_YYYY.md` to maintain narrative continuity for future years.

---

## 🛠️ Customization & Adapting to Other Universities

This repository is designed to be easily tailored to your needs:

* **Documents to fulfill:** Modify the `## Documents to fulfill` section in [`AGENTS.md`](AGENTS.md) to add, remove, or customize the specific document requirements (e.g., Initial Training Plan, Research Plan, Annual Monitoring Report).
* **Templates:** Place your university's official template forms (`.doc`, `.pdf`, `.odt`) inside `templates/`. *Note: The agent uses them as structural reference and will never alter binary template files directly.*
* **Drafting Rules:** Style standards, passive/impersonal voice requirements, and strict anti-AI hallmarks (no em-dashes, no clichés, no filler introductions) are configured in [`AGENTS.md`](AGENTS.md).