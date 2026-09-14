# Site UX Audit & Alignment Plan (Debate Document)

Based on the newly established `PRODUCT_VISION.md`, this document outlines a comprehensive audit of all major pages in the `orange-dev-tracker`. The goal is to identify what works, what breaks the vision, and how to fix it.

Please use this document to debate and align on the proposed changes before we execute them.

---

## 1. Discussions (`pulse.html`)
**Vision:** *The Intellectual Heartbeat (R&D, Strategy, Consensus)*

*   **🟢 What Works:** 
    *   The "Hot Threads" split between Delving Bitcoin and the Mailing List is excellent. 
    *   The "Themes" grid successfully highlights the topics dominating mindshare.
*   **🔴 What Breaks the Vision:** 
    *   The "Top Voices" section and the macro stats (Total Messages/Voices). These are *human* metrics, not *idea* metrics. They belong on the Health or Engineering pages. 
    *   The page currently lacks a sharp narrative on "What are the biggest unresolved debates?"
*   **💡 Proposed Fix:** 
    *   Migrate "Top Voices" and macro human stats away from Pulse.
    *   Introduce an "Emerging Consensus vs. Contested Debates" section (if data supports it), or heavily double down on the R&D themes to fill the gap.

## 2. Roadmap (`roadmap.html`)
**Vision:** *The Operational Engine (Execution)*

*   **🟢 What Works:** 
    *   The recent addition of Dev Meetings grounds the page perfectly in weekly execution.
    *   Tracking the progress bars of GitHub umbrella issues creates a great execution dashboard.
*   **🔴 What Breaks the Vision:** 
    *   The Active Projects are currently just raw titles (e.g., "SENDTEMPLATE", "Erlay") with raw GitHub task links. To a non-core developer (or VC), this is meaningless. It fails the "Tech Exec" test of instant comprehension.
*   **💡 Proposed Fix:** 
    *   Inject AI-generated descriptions into the `tracking_issues.json` pipeline (or hardcode them for the top 5-10 major projects for now). We must explain *what* Erlay is and *why* it matters.
    *   Redesign the project cards to feature this description prominently.

## 3. Engineering (`engineering.html`)
**Vision:** *The Factory Floor (Code Velocity & Architecture)*

*   **🟢 What Works:** 
    *   The "Refactoring vs. Bloat" (Churn vs. Net Change) chart is an executive-level masterpiece. 
    *   The codebase architecture breakdowns (Polyglot makeup, footprint by category) are very strong.
*   **🔴 What Breaks the Vision:** 
    *   The top "Vital Signs" scorecard mixes code metrics (PRs Merged) with human metrics (Contributors, Maintainers). 
*   **💡 Proposed Fix:** 
    *   Purify the page to focus *only* on code and velocity. 
    *   Move "Contributors" and "Maintainers" entirely to the Health page. 
    *   Replace them with pure velocity metrics (e.g., Code Review Latency, or just double down on Commits/PRs).

## 4. Health (`health.html`)
**Vision:** *The Sustainability Report (Humans, Funding, Retention)*

*   **🟢 What Works:** 
    *   The narrative arcs ("The Human Engine", "Institutionalization") are the best on the site. 
    *   The Bus Factor and Funding Matrix are killer features.
*   **🔴 What Breaks the Vision:** 
    *   It does not currently absorb the "Top Voices" (from Pulse) and "Contributors" (from Engineering). To truly be the single source of truth for the human element of Bitcoin Core, it needs all human-centric metrics.
*   **💡 Proposed Fix:** 
    *   Consolidate all missing human metrics (Top Voices, Contributor Onboarding rates) onto this page.

## 5. Releases (`releases.html`)
**Vision:** *The Historical Ledger*

*   **🟢 What Works:** 
    *   Everything. It acts as the perfect, self-contained changelog. No changes needed.

---

## 🗣️ Open Debate Topics

1. **Project Descriptions for Roadmap:** Should we build a Python script in `orange-dev-data` to automatically hit the LLM API for 2-sentence summaries of *all* tracking issues, or just manually hardcode descriptions for the top 10 projects in the frontend?
2. **Top Voices:** Should "Top Voices" be completely moved to `health.html`, or is there a case for keeping "Top *Researchers*" on `pulse.html`?
3. **Engineering Vital Signs:** If we remove Contributors/Maintainers from the Engineering scorecard, what metrics should replace them? (e.g., Lines of Code added, PRs merged, Active PRs).
