# Convox — Accessible Canvas Assistant
> Make Canvas truly usable for blind and low-vision students with reliable **screen reading** + **voice navigation**.

[![TypeScript](https://img.shields.io/badge/TypeScript-MV3-blue)](#)
[![Chrome Extension](https://img.shields.io/badge/Chrome-Extension-success)](#)
[![A11y](https://img.shields.io/badge/WCAG-2.2%20AA-important)](#)
[![License](https://img.shields.io/badge/License-MIT-lightgrey)](#)

---

## 🧭 Overview
**Convox** is a Chrome/Edge browser extension that adds:
- A **smart reader** that speaks Canvas content in a logical, accessible order.
- **Voice commands** to navigate courses, read due dates, open assignments, fill forms, and submit—hands-free.
- **Reader interrupt** (Stop/Pause/Resume) and basic **command chaining** (“Go to Courses → CSCE 1040 → Assignments → read due this week”).

This project addresses key barriers that blind/low-vision students encounter on Canvas by combining semantic DOM parsing, ARIA mapping, and a deterministic command grammar for fast, predictable control.

**Sponsor:** Dr. Mohsen Amini Salehi  
**Team:** Kelly · Aarya · Dylan · Vedansh

---

## 🎯 Goals
- Enable blind/low-vision students to **log in**, **navigate**, **keep up with deadlines**, and **submit work** independently and quickly.
- Be **private-by-default** (local voice by default), **fast**, and **robust** to Canvas DOM changes.

---

## 📌 Features (MVP)
- **F1. Screen Reader** — Read page/section/selection with roles & states announced.
- **F2. Voice Commands** — Replace click/typing/navigation with spoken commands.
- **F3. Voice Log-in** — Guided, secure flow to fill credentials without keyboard.
- **F4. Reader Interrupt** — “Stop/Pause/Resume” and speed controls on demand.
- **F5. Command Chaining (basic)** — 2–3 linked intents in one utterance.

**Stretch**
- F6. “What’s due this week?” summaries
- F7. High-contrast / large-type theme toggle
- F8. Personal shortcuts (latest announcements, schedule, etc.)

**Functional Requirements (User Stories)**
- **R1 Screen Reader (P1)**  
- **R2 Voice Commands (P1)**  
- **R3 Voice Log In (P2)**  
- **R4 Command Chaining (P2)**  
- **R5 Reader Interrupt (P3)**

**Non-Functional**
- NF1 Reliability · NF2 Seamlessness · NF3 Cross-Platform · NF4 ASR accuracy · NF5 Error handling

---

## 🏗️ Architecture
**Extension (MV3)**
- **Content Script:** semantic extraction (headings/landmarks/regions/tables), ARIA role mapping, action executor (click/focus/type/nav), observer for live updates.
- **Background Service Worker:** intent router, command grammar/NLU, session state (current page, list index), preferences.
- **Overlay (React):** minimal UI for mic state, speech rate, help panel, theme toggle.

**Voice Layer**
- **MVP:** Browser **Web Speech API** (ASR) + **SpeechSynthesis** (TTS).
- **Optional Helper (Tier-2):** Local ASR (whisper.cpp or faster-whisper via small service) for offline privacy & higher accuracy.
- **Cloud Fallback (opt-in):** Azure/Google Speech if user explicitly enables.

---

## 🧰 Tech Stack
- **TypeScript + Vite + Chrome MV3**
- **React + Tailwind** (tiny overlay only)
- **chevrotain** (or nearley) for **command grammar**
- **axe-core** for a11y checks (dev)
- **Playwright** (E2E), **Jest/Vitest** (unit)

---

## 📂 Repo Structure
