# GitHub Portfolio Cleanup Plan

**Owner:** Yogesh Gadade  
**Audience:** Senior AI Engineer / Senior Generative AI Developer roles  
**Status:** Proposal only — no repository visibility, archive, deletion, rename, or pin changes have been made.

## Portfolio strategy

Optimize the public profile for senior AI engineering roles across product companies, fintech, and large technology companies. Prioritize a small number of independently engineered, reproducible projects over a large catalogue of older coursework and tutorial repositories.

## Proposed featured repositories

| Repository | Proposed positioning | Recommended next action |
|---|---|---|
| `AIML_Agentic_AI` | Agentic AI engineering portfolio | Replace placeholder README; develop original implementations with architecture, tests, evaluation, and demos |
| `aceloop` (currently private) | AI engineering / coding assessment platform | Keep private until execution isolation, resource controls, trusted result validation, CI, and documentation are hardened |
| `Machine-Learning` | Applied ML and predictive modeling | Select strongest projects; add leakage-safe evaluation, calibration, explainability, and reproducible setup |
| `Natural-Language-Processing` | NLP engineering | Modernize selected examples; compare traditional baselines with transformer approaches |
| `Cryptocurrency-forecasting-and-analysis` | Financial time-series analysis | Add chronological and walk-forward validation, leakage checks, baselines, and data provenance |

Potential future additions should be purpose-built, independent repositories for production RAG, LLM evaluation/observability, and fintech risk intelligence. Do not create empty showcase repositories merely to advertise keywords.

## Proposed repository descriptions

These are suggested descriptions, not yet applied.

| Repository | Suggested description |
|---|---|
| `AIML_Agentic_AI` | Independent implementations and engineering patterns for agentic AI, LLM applications, RAG, evaluation, and production-ready workflows. |
| `aceloop` | AI-assisted coding practice platform with a FastAPI backend, React frontend, and isolated code-execution architecture (under security hardening). |
| `Machine-Learning` | Applied machine-learning projects covering predictive modeling, feature engineering, model evaluation, and explainability. |
| `Natural-Language-Processing` | NLP projects exploring text processing, information extraction, classification, and language-model approaches. |
| `Cryptocurrency-forecasting-and-analysis` | Financial time-series analysis and forecasting experiments with emphasis on leakage-aware validation and reproducibility. |
| `Interacting-with-BQ-using-Python` | Python examples for querying and working with Google BigQuery. |
| `Time-Series-Analysis` | Statistical time-series analysis, forecasting methods, and model evaluation experiments. |
| `Recommendation-Engine` | Recommendation-system experiments and evaluation methods (retain as a featured project only after implementation review). |

## Keep, improve, consolidate, or archive

### Keep and improve
- `AIML_Agentic_AI`: make this the primary public AI portfolio.
- `Machine-Learning`, `Natural-Language-Processing`, `Cryptocurrency-forecasting-and-analysis`: improve the strongest work and make experiments reproducible.
- `Interacting-with-BQ-using-Python`: modernize authentication, client usage, examples, and tests if it remains useful.
- `Statistical-Data-Analysis`, `Optimization-in-Data-Science`: retain selected, well-documented work where it adds evidence of analytical depth.

### Consolidate or selectively retain
- `Analytics`, `Pre-processing`, `Time-Series-Analysis`, `Deep-Learning`, `Neural-Networks`, `Recommendation-Engine`: inspect project quality and overlap; move the strongest reusable work into coherent, documented projects rather than maintaining overlapping collections.
- `Web-Scrapping`, `Big-Data-Technologies`, `Translator`: retain only if they can demonstrate current engineering practices, lawful data collection, provenance, and reproducible setup.

### Candidate for archive or removal — approval required
- Empty or minimal repositories: `Python`, `Neural-Networks` (verify current contents before action).
- Basic educational examples: `hello-world`, `Single-Neuron-Linear-Regression-Exampl`, and `Handwritten-Number-reading-using-Deep-Learning` may be archived or left unpinned.
- Older profile/academic repositories: `Yogeshnaik1190`, `MS-Data-Science`, `MA-570-Analysis-Review`, `MA-541-Statical-Methods-Group-Project` should be assessed for privacy, ownership, and relevance before any visibility change.
- Forks or repositories primarily representing other developers: `Deep-Learning-by-Priya`, `abhisheknaiidu`, `thmsgbrt`, `siddheshshaji`. Remove from portfolio highlights; consider deletion only after checking whether they contain original work worth preserving and reviewing upstream license/attribution.

**Important:** This is a triage recommendation based on repository metadata, README, and selected source inspection. It is not a claim that every file, notebook, license, secret, or historical commit has been exhaustively audited.

## AceLoop: public release blockers

Do not make `aceloop` public or enable arbitrary public code execution until the following are addressed:

1. Replace platform-specific macOS `sandbox-exec` with a hardened Linux container execution boundary.
2. Enforce CPU, memory, process, disk, and wall-clock quotas at the container/runtime level.
3. Restrict network access and filesystem access; run as non-root with a read-only base filesystem where practical.
4. Have the trusted parent process validate execution results; never trust a report written by the untrusted child process.
5. Standardize configuration: the current `ACELOOP_` settings prefix and unprefixed example environment variables need a consistent, tested contract.
6. Add backend and frontend CI, linting, dependency/security scanning, and frontend tests.
7. Document the threat model, architecture, local setup, operational limits, and deployment process.

## Definition of done for featured repositories

- Clear README: problem, use cases, architecture, trade-offs, setup, demo, and limitations.
- Reproducible dependencies and data instructions.
- Unit and integration tests with CI status.
- No secrets, private data, employer code, or confidential business logic.
- Evaluation results with baselines and stated methodology.
- Structured logging and useful failure handling; observability where relevant.
- Architecture diagram and key design decisions.
- License and data provenance reviewed.

## Approval gates

The current PR only updates the profile README and adds this proposed cleanup plan. Before applying any repository metadata or lifecycle changes, review and approve the exact targets. In particular, do not delete, archive, transfer, or change visibility of any repository based solely on this proposal.
