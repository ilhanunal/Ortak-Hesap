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
| Wireframes (14 screens, clickable) | [Figma - Ortak Hesap Wireframes](https://www.figma.com/design/7qLkitp03UVHnm8bihpD8y) | Anyone with the link can view |
| Mockups (14 screens, Material 3) | [Figma - Ortak Hesap Mockups and Prototype, page "Mockups"](https://www.figma.com/design/Lp0KlXl0ggJ9jWSF42ItWa) | Anyone with the link can view |
| Prototype (clickable flow) | [Figma - same file, page "Prototype"](https://www.figma.com/design/Lp0KlXl0ggJ9jWSF42ItWa?node-id=3-239) | Anyone with the link can view |

How to try the prototype: open the Prototype page, press **Present** (play button) and choose the flow **"Main flow (start at onboarding)"**. Transitions used: push (forward / back), move-in from the bottom (FAB and custom split sheet) and dissolve (tabs and dialogs).

## Deliverables and status

| # | Deliverable | File / link | Status |
|---|---|---|---|
| 1 | Design justification (PDF, 2 pages) | [docs/01_Design_Justification.pdf](docs/01_Design_Justification.pdf) | Done |
| 2 | User flow diagram (PDF) | [docs/02_User_Flow.pdf](docs/02_User_Flow.pdf) | Done |
| 3 | Wireframes (Figma) | see Figma links, preview: [design/wireframes-overview.png](design/wireframes-overview.png) | Done |
| 4 | Mockups (Figma) | see Figma links, preview: [design/mockups-overview.png](design/mockups-overview.png) | Done |
| 5 | Prototype (Figma) | see Figma links (page "Prototype") | Done |
| 6 | Architecture and protocols (PDF) | [docs/03_Architecture_and_Protocols.pdf](docs/03_Architecture_and_Protocols.pdf) | Done |

## Architecture at a glance

- **Pattern:** MVVM (Model-View-ViewModel) with a Repository layer; `provider` + `ChangeNotifier` for state.
- **Layers:** View (Flutter widgets) -> ViewModel -> Repository interfaces -> data sources (Firebase Auth, Cloud Firestore, FCM, Storage, camera, share, deep links).
- **Key protocols and interfaces:** HTTPS/TLS, OAuth 2.0 / OpenID Connect (Google sign-in), Cloud Firestore real-time listeners with offline cache, Firebase Cloud Messaging, Android App Links (invite links), camera/QR scanning, share sheet.
- **Model layer logic:** integer money in kuruş, fair equal-split rounding, greedy debt simplification (at most n-1 payments).

Details, diagrams and the full protocol table are in [docs/03_Architecture_and_Protocols.pdf](docs/03_Architecture_and_Protocols.pdf).

## Repository structure

```
ortak-hesap/
├── README.md
├── docs/
│   ├── 01_Design_Justification.pdf
│   ├── 02_User_Flow.pdf
│   ├── 03_Architecture_and_Protocols.pdf
│   └── src/                      # editable sources of the PDFs (HTML)
│       ├── design-justification.html
│       ├── user-flow.html
│       └── architecture-protocols.html
└── design/
    ├── wireframes-overview.png   # preview of the Figma wireframes
    └── mockups-overview.png      # preview of the Figma mockups
```

The editable design work stays in Figma (links above).

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
- Submission: archive uploaded to online.yildiz.edu.tr (Team 5)
