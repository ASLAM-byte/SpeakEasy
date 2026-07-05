# 🎙️ SpeakEasy — Speaking Practice App

<div align="center">

**A beautiful, feature-rich web app to sharpen your public speaking, interview skills, and vocabulary — one spin at a time.**

![Next.js](https://img.shields.io/badge/Next.js-16-black?style=for-the-badge&logo=next.js)
![React](https://img.shields.io/badge/React-19-61DAFB?style=for-the-badge&logo=react)
![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?style=for-the-badge&logo=typescript)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-v4-38BDF8?style=for-the-badge&logo=tailwindcss)
![Framer Motion](https://img.shields.io/badge/Framer_Motion-12-pink?style=for-the-badge&logo=framer)

</div>

---

## ✨ Overview

**SpeakEasy** is an interactive speaking-practice platform that helps users build confidence in three key areas through a fun slot-machine-style interface:

| Mode | Description |
|------|-------------|
| 🎲 **Random Topics** | Spin to get a random speaking topic filtered by language, difficulty, and category |
| 🧠 **Interview Prep** | Practice behavioral, leadership, communication, and technical interview questions |
| 📖 **Learn Vocab** | Expand your vocabulary with rich word cards — definition, pronunciation, example usage, and speaking tips |

The UI is crafted with a warm cream + deep forest green + amber editorial aesthetic, smooth Framer Motion animations, and an iconic animated slot-machine lever.

---

## 🖼️ Features

### Core Experience
- 🎰 **Slot Machine Spin** — Animated lever (drag or click) generates a new topic/question/word with a satisfying scroll animation
- ⌨️ **Keyboard Shortcuts** — `Space` to spin, `Ctrl+1/2/3` to switch tabs, `Esc` to close modals
- 🔊 **Sound Effects** — Subtle audio feedback on spin and timer completion

### Topic Generator
- 100+ topics across 12+ categories: General, Technology, Finance, Debate, ELI5, Hot Takes, Pitch, Roast, Conspiracy, Gen-Z, Millennial, and Random
- Filter by **Language** (13 languages including English, Spanish, French, Arabic, Hindi, and more), **Difficulty** (Easy / Medium / Hard), and **Category**

### Interview Prep
- 100+ questions covering Behavioral, Leadership, Communication, and Technical types
- **Answer Frameworks** — STAR, PREP, PPF accordion panels with examples
- **Sample Answer Modal** — Structured answers broken into labelled sections per framework

### Vocabulary Builder
- 200+ words with: Part of speech, Pronunciation guide, Definition, Example sentence, and a Speaking Angle tip
- Difficulty and language filters

### Timer
- Dedicated full-page circular countdown timer
- SVG animated progress ring
- `−0:30` / `+0:30` quick adjustment buttons
- Play / Pause / Reset controls
- 🎉 Confetti celebration on completion

### Speech Analysis Page
- Upload or record audio
- Visual waveform display
- Metrics dashboard: Confidence, Grammar, Vocabulary, Pacing, and more

### History & Favorites
- Persistent history of the last 100 generated items (stored in `localStorage`)
- Save favorites with a single click — persisted across sessions

### Settings
- 🌙 **Dark / Light / System** theme
- 🎨 Accent color picker
- ♿ Animation toggle (reduced motion support)
- 🔇 Sound toggle

---

## 🏗️ Tech Stack

| Technology | Purpose |
|---|---|
| **Next.js 16** (App Router) | Framework, routing, SSR |
| **React 19** | UI, concurrent features |
| **TypeScript 5** | Type safety, strict mode |
| **Tailwind CSS v4** | Utility-first styling with custom design tokens |
| **Framer Motion 12** | Page transitions, slot animations, lever gestures |
| **Zustand 5** | Global state (history, favorites, settings, filters) |
| **Lucide React** | Icon set |
| **canvas-confetti** | Timer completion celebration |
| **Cloudflare Workers** | Edge deployment (`wrangler.toml`) |

---

## 📁 Project Structure

```
speakeasy/
├── app/
│   ├── layout.tsx              # Root layout with providers & SEO
│   ├── page.tsx                # Home page (3-tab editorial layout)
│   ├── timer/page.tsx          # Circular countdown timer
│   ├── speech-analysis/page.tsx
│   ├── confidence/
│   ├── fluency/
│   ├── daily-routine/
│   ├── learn/
│   ├── profile/
│   ├── progress/
│   └── settings/
├── components/
│   ├── layout/                 # FloatingNav, EditorialPanels, FloatingActions
│   ├── random-topics/          # SlotMachineCard, Lever, TopicFilters
│   ├── interview-prep/         # FrameworkAccordion, SampleAnswerModal
│   ├── vocab/                  # VocabCard, VocabPanel
│   └── timer/                  # TimerModal, CircularTimer
├── data/
│   ├── topics.ts               # 100+ topics (category / difficulty / language)
│   ├── vocabulary.ts           # 200+ vocab words
│   ├── interviewQuestions.ts   # 100+ interview questions
│   ├── frameworks.ts           # STAR, PREP, PPF definitions
│   └── sampleAnswers.ts        # Structured sample answers
├── store/
│   └── appStore.ts             # Zustand store (persisted to localStorage)
├── hooks/
│   └── useSound.ts
├── lib/
│   └── utils.ts
├── types/
│   └── index.ts
└── constants/
    └── index.ts
```

---

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
|---|---|
| `Space` | Spin / generate new content |
| `Ctrl + 1` | Switch to Random Topics tab |
| `Ctrl + 2` | Switch to Interview Prep tab |
| `Ctrl + 3` | Switch to Learn Vocab tab |
| `Esc` | Close open modal |

---

## 🎨 Design System

| Token | Value | Usage |
|---|---|---|
| Background | `#F9F5EB` | Warm cream canvas |
| Primary | `#134F43` | Deep forest green |
| Accent | `#E8A23B` | Warm golden amber |
| Secondary | `#b8a8d4` | Soft lavender (lever / timer ring) |
| Font (headings) | Cormorant Garamond | Serif editorial headings |
| Font (body) | Inter | Clean sans-serif body text |

---

## 📄 License

This project is **source-private**. The deployed application is publicly accessible for use.  
Unauthorized copying, modification, or redistribution of the source code is not permitted.

---

<div align="center">
Made with ❤️ for better speakers everywhere.
</div>
