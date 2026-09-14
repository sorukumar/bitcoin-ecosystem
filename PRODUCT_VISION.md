# Orange Dev Tracker: Product Vision & Architecture

## The Core Thesis
Bitcoin Core development is often perceived as an opaque, impenetrable black box. **Orange Dev Tracker** exists to make the invisible visible. We provide institutional-grade analytics, making the velocity, health, and narrative of Bitcoin's development accessible to researchers, investors, and the developers themselves.

We are not building a chaotic data dump; we are building a curated intelligence dashboard. Every page serves a specific, distinct user journey. 

## The Core Five Pillars (Site Architecture)

To maintain a clean user experience and avoid feature creep, the site is strictly partitioned into five core pillars. 

### 1. Discussions (`pulse.html`)
**The Vibe:** The Intellectual Heartbeat.
**The Focus:** Strategy, R&D, and future consensus.
*   **The PM Definition:** The pulse of asynchronous debates across Delving Bitcoin and the mailing list. It aggregates the noise to surface the signal of what researchers are thinking about *before* it becomes code.
*   **The VC / Social Media Pitch:** "Where the future of Bitcoin is debated. Track the R&D pipeline and see consensus forming in real-time."
*   **Key Metrics:** Hot threads, dominant themes, active researchers, BIP mentions.

### 2. Active Initiatives (`roadmap.html`)
**The Vibe:** The Operational Engine.
**The Focus:** Major project execution and milestone tracking.
*   **The PM Definition:** What is actively being built in Bitcoin Core right now. This page tracks major umbrella initiatives and their sub-task completion progress. (Tactical weekly IRC meetings are syndicated to *This Week in Bitcoin*).
*   **The VC / Social Media Pitch:** "The execution dashboard. Track the live delivery and progress of major Bitcoin engineering initiatives."
*   **Key Metrics:** Active GitHub umbrella projects, sub-task completion rates, lead developers.

### 3. Engineering (`engineering.html`)
**The Vibe:** The Factory Floor.
**The Focus:** Macro-level code velocity and architectural composition.
*   **The PM Definition:** Quantitative metrics on how fast the project is shipping and how the codebase is structured (languages, functional areas, refactoring vs. bloat).
*   **The VC / Social Media Pitch:** "Institutional-grade metrics on Bitcoin's code velocity. See exactly how the engineering workforce is scaling and managing complexity."
*   **Key Metrics:** Total commits, PRs merged, contributor onboarding, churn vs. net change.

### 4. Releases (`releases.html`)
**The Vibe:** The Historical Ledger.
**The Focus:** The definitive, backward-looking changelog of what shipped.
*   **The PM Definition:** A highly specific, granular archive. When a user needs to know exactly which PRs went into v26.0 and who contributed to them, this is the single source of truth.
*   **The VC / Social Media Pitch:** "The permanent ledger of Bitcoin's software milestones. Audit the exact composition and human capital behind every major release."
*   **Key Metrics:** Version timelines, highlight summaries, complete PR lists, top contributors per release.

### 5. Health (`health.html`)
**The Vibe:** The Sustainability Report.
**The Focus:** Macro-level sustainability, funding, and workforce retention.
*   **The PM Definition:** An analysis of the *human* engine. Tracking the "Bus Factor", developer retention rates, geographic distribution, and corporate vs. independent funding sources.
*   **The VC / Social Media Pitch:** "Assess the long-term sustainability of Bitcoin. Analyze developer retention, global decentralization, and the funding models securing the network."
*   **Key Metrics:** Bus factor, 1-year survival rate of regulars, institutional sponsorship footprint, global timezone activity.

---

## Guiding Principles for Future Development

1. **Protect the Narrative:** Before adding a new chart or dataset, ask which of the Five Pillars it belongs to. If it's about *what* we are building, it goes in Roadmap. If it's about *how fast* we are building it, it goes in Engineering. Do not mix operational status with R&D debates.
2. **Progressive Disclosure:** Not every piece of data needs to be on the top level. Use UI patterns like "View Archive" or expandable accordions (e.g., historical dev meetings or deep-dive PR lists) to keep the primary dashboards scannable.
3. **No-Nonsense Positioning:** Avoid jargon. Labels should pass the "Tech Exec" test—clear, pragmatic, and instantly understandable within 10 seconds.
