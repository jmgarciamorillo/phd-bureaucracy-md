# Contributing to PhD Bureaucracy Framework

Thanks for contributing!

This repository is an AI-assisted, Markdown-first framework designed to simplify doctoral monitoring reports and bureaucratic milestones. It structures academic context in a format that any AI agent can understand and translate into official, ready-to-sign documents.

---

## How to Contribute

### 1. Improve the Framework Prompting & Rules (`AGENTS.md`)

If you notice issues with agent drafting behavior, anti-AI heuristics, or tone constraints:

* Open an issue first to describe the proposed enhancement or bug (e.g., unintended AI hallmarks, improved grammatical rules for academic writing, better formatting blocks).
* Update `AGENTS.md` keeping instructions concise, objective, and institution-agnostic where appropriate.
* Open a pull request explaining your rationale and showing before/after examples of agent outputs.

### 2. Adapting & Expanding to Other Universities

Currently, this repository is tailored specifically for a single university—the **Universidad de Granada (UGR)**. However:

* **Individual Adaptation:** The repository can be easily customized for any university simply by updating `fixed_data/`, `templates/`, and `AGENTS.md`.
* **Community Support Worldwide:** If there is interest from the academic community in supporting other universities worldwide, the repository structure can be modified to include pre-defined presets, institutional catalogs, and templates for other universities.
* Feel free to open an issue or pull request proposing a multi-institution folder structure or adding pre-defined configurations for your university.
* Ensure no private personal data (real IDs, confidential drafts, private emails) is ever committed. Always use realistic placeholders.

### 3. Improve Documentation & Examples

* Clarify the setup steps in `README.md`.
* Improve the example files in `fixed_data/` and `current_year/` to make them more helpful for new PhD candidates.
* Fix typos, broken internal links, or formatting inconsistencies.

---

## Pull Request Guidelines

* Keep PRs focused on a single concern or improvement.
* Test your prompt or instruction adjustments with an LLM agent to ensure it produces clean, compliant outputs without regressions.
* Never commit personal or sensitive doctoral evaluations into the repository.

---

## License

By contributing, you agree that your contributions are provided under the repository license terms.
