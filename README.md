# AI-Native Design Patterns

**Side-by-side Do / Don't modules for building observable, human-in-the-loop AI systems in high-stakes enterprise workflows.**

Built by [Magarottos, Inc.](https://www.magarottos.com/) - [Pattern Hub](https://www.magarottos.com/pattern-hub/)

---

## What This Is

Most AI implementations fail because they prioritize conversation over control. This library documents ten essential design patterns across eleven industries, showing the difference between black-box automation and observable, trustworthy AI systems.

Each module presents a **Don't** (how AI typically gets shipped) alongside a **Do** (what a well-designed, human-in-the-loop system actually looks like) — rendered as interactive UI examples you can study, export, and adapt.

---

## The 10 Patterns

Every industry page applies the same ten patterns to its domain-specific workflows:

| # | Pattern | What It Addresses |
|---|---------|------------------|
| 01 | **Progressive Disclosure of AI Confidence** | Hiding vs. surfacing how certain the model actually is |
| 02 | **Human-in-the-Loop Checkpoints** | Automating consequential actions vs. requiring human approval |
| 03 | **Explainable Output Framing** | Black-box verdicts vs. visible reasoning and evidence |
| 04 | **Graceful Degradation Messaging** | Confident outputs on incomplete data vs. honest limitations |
| 05 | **Contextual AI Onboarding** | Mandatory pre-training vs. inline coaching during real work |
| 06 | **Feedback Loop Integration** | No correction mechanism vs. structured model improvement |
| 07 | **Scope Boundary Visualization** | Undeclared AI limits vs. explicit capability transparency |
| 08 | **Multi-Modal Input Adaptation** | Text-only interfaces vs. unified handling of all input types |
| 09 | **Trust Calibration Indicators** | Uniform confidence on all outputs vs. differentiated evidence signals |
| 10 | **Audit Trail Transparency** | No decision record vs. full, exportable action history |

---

## Industries Covered

| Industry | Focus Areas |
|----------|-------------|
| **Finance** | Month-end close, audit trails, policy guardrails, confidence explainability |
| **Legal** | Contract review, human-in-the-loop checkpoints, audit transparency |
| **Insurance** | Claims processing, underwriting, fraud detection, policy management |
| **Healthcare** | Clinical decision support, patient data, diagnostic assistance |
| **E-Commerce & Retail** | Personalization, inventory management, pricing optimization |
| **Cybersecurity** | Threat detection, incident response, vulnerability management |
| **Education** | Adaptive learning, assessment, student support, administration |
| **Logistics & Supply Chain** | Route optimization, demand forecasting, warehouse operations |
| **HR & Compliance** | Hiring, policy review, disciplinary workflows, people ops |
| **Dental Insurance** | Claims follow-up, eligibility verification, denials, appeals, aging AR, patient billing |
| **Marketing** | Campaign optimization, copy generation, audience targeting, budget allocation, brand governance |

---

## Tech Stack

- **React 18** + **TypeScript**
- **Vite** — build tooling
- **Tailwind CSS** — styling
- **Lucide React** — icons
- **html2canvas** — PNG export per module

---

## Running Locally

```bash
npm install
npm run dev
```

Open `http://localhost:5173` to see the Pattern Hub index. Each industry is a separate route (e.g. `/finance`, `/healthcare`, `/dental`, `/martech`).

---

## Project Structure

```
src/
  PatternHub.tsx              # Index page — links to all industries
  components/
    ComparisonCard.tsx        # Don't / Do card wrapper
    ExportContainer.tsx       # Module wrapper with PNG export
    ExportButton.tsx          # Per-module export trigger
    DownloadAllButton.tsx     # Batch export all 10 modules
    DownloadGuideButton.tsx   # Downloads full HTML implementation guide
  utils/
    imageExport.ts            # html2canvas export logic
  finance/
  legal/
  insurance/
  healthcare/
  ecommerce/
  cybersecurity/
  education/
  logistics/
  hr/
  dental/
  martech/
```

Each industry folder follows the same structure:

```
{Industry}App.tsx             # Route root — renders intro + all 10 modules in order
{Industry}IntroSection.tsx    # Hero with industry context and pattern legend
ModuleOne.tsx — ModuleTen.tsx # One file per pattern
```

---

## Exporting Modules

Every module has an **Export PNG** button that captures the Do/Don't panel as a `2x` resolution image with padding. A **Download All** button on each industry page exports all 10 modules in sequence.

A **Download Implementation Guide** button on the hub page generates a self-contained HTML document covering all 110 modules across all 11 industries — with personas, contexts, and direct links.

---

## Design Notes

- **Don't card** — red border, shows the failure mode and its real-world consequence
- **Do card** — emerald border, shows the correct pattern with interactive UI where possible
- Color system uses neutral tones, blues, greens, ambers, and reds appropriate to each domain
- 8px spacing grid throughout
- Each module is fully self-contained with no shared state between modules

---

## License

MIT — use these patterns freely. Attribution appreciated.

© 2026 Magarottos, Inc.
