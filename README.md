# Convox
Accessible Canvas assistant.

---

## Overview
Convox provides **screen reading** and **voice navigation** for Canvas so students can access coursework hands-free and eyes-free when needed.

---

## Product Requirements

### Brief Problem Statement
Canvas is not fully accessible for blind and low-vision students. It lacks robust alternative inputs beyond mouse/keyboard, and many UI elements are not reliably labeled for assistive tech. Since much of college work at UNT depends on Canvas, this gap must be closed.

**Convox** delivers:
- A screen reader that consistently reads Canvas content.
- Voice commands that let users navigate, search, and complete core tasks.

### System Requirements
- **Browser:** Google Chrome (current release)
- **I/O:** Microphone (input) and speakers/headphones (output)

### User Profiles

**User Profile 1 — David (Blind Undergraduate Student, 21)**
- **Disability:** Blind since birth  
- **Tech skills:** Experienced with screen readers; uses Siri/voice commands  
- **Goals:** Access assignments/announcements/grades independently; keep up with deadlines  
- **Challenges:** Unlabeled menus/links; multi-step submission flows; reliance on others  
- **How Convox helps:** Clear, consistent reading of Canvas content; voice commands for quick navigation

**User Profile 2 — Amy (Low-Vision Undergraduate Student, 19)**
- **Disability:** Partial vision; struggles with small text/clutter  
- **Tech skills:** Moderate; uses magnification software  
- **Goals:** Find due dates/quizzes/announcements quickly; reduce eye strain  
- **Challenges:** Low contrast icons/text; magnification breaks layout; time wasted hunting  
- **How Convox helps:** Voice navigation to jump directly to courses/assignments/grades; **high-contrast UI mode** for key elements

---

## Features
Provide a numbered list of project-defining features.

- **F1 — Screen Reading:** Read on-page Canvas content to the user.
- **F2 — Voice Commands:** Accept voice commands via microphone input.
- **F3 — Voice Login:** Log in to Canvas without using the keyboard.
- **F4 — Reader Interrupt:** Interrupt reading at any time to issue a command.
- **F5 — Command Chaining:** Execute multiple actions from a single voice input.
- **F6 — High-Contrast Mode (UI):** Optional high-contrast visual theme for low-vision users.

---

## Functional Requirements (User Stories)

| ID  | Name              | Description                                                                                          | Priority |
|-----|-------------------|------------------------------------------------------------------------------------------------------|:--------:|
| R1  | Screen Reader     | When navigating to a page, the system reads the relevant content aloud.                             |    1     |
| R2  | Voice Commands    | Voice can replace mouse/keyboard interactions (click, type, navigate between pages and text boxes). |    1     |
| R3  | Voice Login       | Users can log in to Canvas using voice only.                                                         |    2     |
| R4  | Command Chaining  | As an experienced user, chain multiple commands to perform tasks efficiently.                       |    2     |
| R5  | Reader Interrupt  | Interrupt the reader at any time to issue a new command.                                             |    3     |

**Priority scale:** 1 = High (Critical), 2 = Medium (Important), 3 = Low (Nice-to-have)

---

## Non-Functional Requirements
- **NF1 — Reliability:** Minimal setup; should “just work.”
- **NF2 — Seamlessness:** Must not obstruct Canvas; turning on/off is quick with minimal/no redirects.
- **NF3 — Cross-Platform (Desktop):** Works on Windows and macOS in Chrome.
- **NF4 — ASR Accuracy:** Clearly recognizes user speech; robust to background noise; executes intended commands.
- **NF5 — Error Handling:** If a command is unrecognized, notify the user and prompt to restate.

---

## Privacy & Security
- **Local-first voice processing.**  
- **Cloud ASR is strictly opt-in** and off by default.

---

## Roadmap
- **Week 1–2:** Grammar & Reader  
- **Week 3–4:** Executor & Login  
- **Week 5–6:** Command Chaining & Reader Interrupt

---

## Demo Script
1. Login by voice  
2. Open **Courses → Assignments**  
3. Read assignments due this week

---

## Quick Start (GitHub Desktop)

1. **Clone the repo**  
   GitHub Desktop → **File ▸ Clone repository…** → select repo → **Clone**.

2. **Create a feature branch**  
   **Branch ▸ New Branch…** → `feature/readme-updates` → **Create Branch**.

3. **Edit files**  
   **Repository ▸ Open in &lt;Editor&gt;** → update `README.md`, add docs (e.g., `CONTRIBUTING.md`).

4. **Commit (make several small commits)**  
   In **Changes**, write a message (e.g., `docs: add project overview`) → **Commit to feature/readme-updates**.  
   Aim for 2–3+ logically-scoped commits.

5. **Push the branch**  
   Click **Push origin** to publish your branch.

6. **Open a Pull Request**  
   **Create Pull Request** in Desktop (or on GitHub: “Compare & pull request”).  
   Add a clear title and short description.

7. **Merge to `main`**  
   On GitHub → **Merge pull request** → **Confirm merge** → **Delete branch**.

8. **Sync `main` locally**  
   In Desktop: switch to **main** → **Fetch origin** → **Pull**.

> **Troubleshooting**
> - If push fails, ensure you’re signed into GitHub Desktop.
> - If PR can’t auto-merge, run **Branch ▸ Update from main** (or rebase) and push again.

---

## Screenshots
![Repository view](assets/screenshot-1.png)
![Pull Request flow](assets/screenshot-2.png)

---

## Team
- Vedansh
- Kelly
- Aarya
- Dylan

---

## Sponsor Approval
I have read and approve the material in this document. If there is no external sponsor, the TA or instructor will sign for accuracy/scope.

**Dr. Mohsen Amini Salehi**  
Signature: _______________________________  
Date: September 18, 2025
