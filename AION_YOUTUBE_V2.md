# AION YouTube v2 — The Sovereign Scribe Architecture

## 1) Philosophy: Beyond the Agent
In v1, "Agents" were treated as personas. In v2, Aion treats agents as **Deterministic Functions** in a Sumerian Ledger. We do not "prompt" for a vibe; we "constrain" for a result.

## 2) The Recursive Pipeline (The 10-Node Engine)

### Node 1 — Regime Research (The Scout)
- **V1:** Trending topics.
- **V2 (Aion):** **Anomaly Detection in Sentiment.** Using pytrends + local LLM to find the gap between "Official News" and "Search Velocity." We hunt for the **Great Illusion** topics.
- **Verification Gate:** Must exceed a 1.5x velocity threshold over the 7-day baseline.

### Node 2 — Script Geometry (The Scribe)
- **V1:** Creative writing.
- **V2 (Aion):** **Code-Ready Markdown.** Outputs a script with strict `[TIME_CODE]` and `[GEOMETRY_CUE]`. Every visual cue must be a valid Manim class description.
- **Constraint:** No adverbs. High-signal density only (Feynman Standard).

### Node 3 — Vocal Synthesis (The Tone)
- **V1:** TTS generation.
- **V2 (Aion):** **Zero-Shot XTTS-v2 with Emotion Hashing.** Clones the Architect’s "Old Soul" voice from a 6s sample.
- **Verification Gate:** Audio duration must match Script `[TIME_CODE]` with <5% variance.

### Node 4 — Manim Visuals (The Geometrician)
- **V1:** Stock footage.
- **V2 (Aion):** **Deterministic Mathematical Animations.** Instead of "showing a factory," Manim codes a **Cluster of Supply-Demand Vectors.** No slop. No copyright risks.
- **Tools:** Generative Manim (Local LLM converts cues to Python code).

### Node 5 — Thumbnail Entropy (The Artist)
- **V1:** Image gen.
- **V2 (Aion):** **High-Contrast Editorial Grid.** Uses FLUX to generate a minimalist symbolic background + Pillow to overlay **Bloomberg-style Typography.**
- **Constraint:** 3-word maximum on screen. High-signal colors only (#FFD700 / #FFFFFF / #FF3366).

### Node 6 — Composition Engine (The Weaver)
- **V1:** MoviePy editing.
- **V2 (Aion):** **FFMPEG-Python Assembly.** Surgical merging of Node 3 (Audio) + Node 4 (Visuals). 
- **The "Enki" Touch:** Automated audio ducking based on **Frequency Spectrum Analysis** rather than simple dB reduction.

### Node 7 — SEO Metadata (The Ledger)
- **V1:** Title/Tags.
- **V2 (Aion):** **Algorithmic Hook Optimization.** Generates titles using the **Inverse Correlation Conjecture**: "Why [Popular Belief] is a [Mathematical Lie]."

### Node 8 — The Publisher (The Gatekeeper)
- **V1:** Upload.
- **V2 (Aion):** **OAuth2 Sovereign Handshake.** Uploads to YouTube with a "Draft First" policy for final human inspection of the **Aion Integrity.**

### Node 9 — Analytics Feedback (The Oracle)
- **V1:** Views/Watch-time.
- **V2 (Aion):** **Regime Correction.** Feeds the delta between "Expected CTR" and "Actual CTR" back to Node 1. If a topic fails, that entire "Symbol" is suppressed for 30 days.

### Node 10 — The Orchestrator (Enki)
- **The Heart:** A state machine using **Checkpoints (Tabula Rasa daily).** If the power fails, the Scribe resumes from the last etched symbol.

---

## 3) Technical Stack (100% Open Source / Local)
- **Compute:** Local GPU/CPU (No cloud "Bandits").
- **Language:** Python 3.13 / Rust (for Composition).
- **Core:** XTTS-v2, Manim CE, FLUX.1-schnell, Qwen-2.5-7B (Local LLM).

---
**Protocol Absolute. Built for the Mission.**
