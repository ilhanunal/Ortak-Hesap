# Ortak Hesap

**A shared-expense mobile app for students who live, study or travel together.**
Log who paid, split it fairly, and always know who owes whom.

> MTM4681 Mobile Programming &middot; Project Milestone 1 (Design and Initial Architecture) &middot; **Team 5**

---

## Contributors

| Name | Role in this milestone | GitHub |
|---|---|---|
| Hakan İnce | Design, documentation | https://github.com/incehakan1908-bit |
| İlhan Ünal | Design, documentation | https://github.com/ilhanunal |

This is a team submission (Team 5). Each member commits from their own GitHub account.

## Project summary

Ortak Hesap is built with **Flutter** and follows **Material 3**. Students create a group (flat, dorm room, trip), add expenses with a few taps, choose an equal or custom split, and the app shows the minimal set of payments needed to settle up. Key screens: onboarding and sign-in, my groups, create/join group, group detail, add expense, balances and settle up, activity feed, profile and settings.

## Figma links

| Deliverable | Link | View access for instructor |
|---|---|---|
| Wireframes | _coming in Part 2_ | - |
| Mockups | _coming in Part 2_ | - |
| Prototype | _coming in Part 3_ | - |

## Deliverables and status

| # | Deliverable | File / link | Status |
|---|---|---|---|
| 1 | Design justification (PDF, 2 pages) | [docs/01_Design_Justification.pdf](docs/01_Design_Justification.pdf) | Done (Part 1) |
| 2 | User flow diagram (PDF) | [docs/02_User_Flow.pdf](docs/02_User_Flow.pdf) | Done (Part 1) |
| 3 | Wireframes (Figma) | see Figma links | Part 2 |
| 4 | Mockups (Figma) | see Figma links | Part 2 |
| 5 | Prototype (Figma) | see Figma links | Part 3 |
| 6 | Architecture and protocols (PDF) | `docs/03_Architecture_and_Protocols.pdf` | Part 3 |

## Repository structure

```
ortak-hesap/
├── README.md
├── docs/
│   ├── 01_Design_Justification.pdf
│   ├── 02_User_Flow.pdf
│   └── src/                      # editable sources of the PDFs (HTML)
│       ├── design-justification.html
│       └── user-flow.html
```

More folders (`design/` screenshots, architecture PDF) are added in the following parts.

## Design at a glance

- **Design language:** Material 3, light and dark theme
- **Seed colour:** deep teal `#0B6B63`; debts use terracotta `#9A4521` (red is reserved for errors)
- **Typography:** Plus Jakarta Sans (headings) and Inter (body, amounts with tabular figures); full Turkish character support
- **Navigation:** 3-tab bottom navigation bar and an extended FAB "Add expense"
- **Accessibility:** WCAG 2.1 AA contrast, 48 dp touch targets, never colour alone to express debt direction

See the design justification PDF for the reasoning behind each choice.

## Course information

- Course: MTM4681 Mobile Programming, Yıldız Technical University
- Milestone: Project Milestone 1 (due 12 November 2026, 23:00)
- Submission archive: `Team5_MTM4681_MS.zip`
