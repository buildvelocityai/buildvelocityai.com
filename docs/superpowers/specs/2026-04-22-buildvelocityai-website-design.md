# Build Velocity AI — One-Page Website Design Spec
**Date:** 2026-04-22
**Output:** Single `index.html` file with embedded CSS and JS. No external dependencies.

---

## Overview

A clean, modern, dark-themed one-page marketing site for **Build Velocity AI**, an AI automation agency that builds custom chatbots for local businesses. The site converts visitors into leads by showcasing the problem, solution, social proof, pricing, and a live demo.

---

## Tech Stack

- **Single file:** `index.html` with `<style>` and `<script>` blocks
- **No frameworks, no CDN dependencies**
- **CSS:** Custom properties for theming, Flexbox/Grid for layout
- **JS:** Vanilla — Intersection Observer for scroll animations, smooth scroll, mobile nav toggle
- **Form:** `mailto:` action (no backend required)

---

## Color Palette & Typography

| Token | Value | Usage |
|---|---|---|
| `--bg-primary` | `#0a0a0f` | Page background |
| `--bg-surface` | `#1a1a2e` | Cards, nav |
| `--bg-surface-2` | `#16213e` | Alternate section bg |
| `--accent` | `#2563eb` | Buttons, highlights |
| `--accent-hover` | `#1d4ed8` | Button hover state |
| `--text-primary` | `#f8fafc` | Body text |
| `--text-muted` | `#94a3b8` | Subtext, labels |

**Font:** System font stack — `-apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif`

---

## Page Structure

### 1. Sticky Navigation
- Left: "Build Velocity AI" logo (text, accent-colored)
- Right: anchor links — Problem, Solution, Pricing, Demo — plus a "Get Started" CTA button (scrolls to contact)
- Mobile: hamburger menu collapses nav links
- Background: `--bg-surface` with subtle bottom border

### 2. Hero Section
- Full-viewport-height (`100vh`)
- Headline: **"Never Miss a Patient Inquiry Again"** (large, white)
- Subheadline: *"We build custom AI chatbots for local businesses that capture leads and answer questions 24/7 — even while you sleep."* (muted)
- CTA button: **"See a Live Demo"** → opens `https://creator.voiceflow.com/share/69dd92f5d352ed76bf779c26/development` in a new tab
- Background: radial gradient blue glow behind headline for depth

### 3. The Problem
- Section title: "Sound Familiar?"
- 3 pain point cards (icon + title + description):
  1. **Visitors Leave Without Answers** — Potential customers land on your site after hours and leave when no one responds.
  2. **Inquiries Go Unanswered** — Phone calls and contact forms pile up overnight, and leads go cold by morning.
  3. **Staff Overwhelmed** — Your front desk answers the same questions dozens of times a day instead of focusing on real work.
- Card style: `--bg-surface` background, red/orange warning icon accent

### 4. The Solution
- Section title: "Your Always-On AI Assistant"
- Brief intro paragraph
- 3 solution points (icon + title + description):
  1. **Answers Instantly** — Responds to customer questions in seconds, 24/7, with accurate info about your business.
  2. **Captures Lead Info Automatically** — Collects name, contact details, and inquiry type without any staff involvement.
  3. **Notifies Your Team Immediately** — Sends real-time alerts so your team can follow up when it matters most.
- Background: `--bg-surface-2` (alternate)

### 5. How It Works
- Section title: "Up and Running in 48 Hours"
- 3 numbered steps in a horizontal row (stacks on mobile):
  1. **We Learn Your Business** — We gather your FAQs, services, hours, and policies.
  2. **We Build Your Custom Chatbot** — Trained on your business, live in 48 hours.
  3. **You Start Capturing Leads** — Sit back while your chatbot works around the clock.
- Step connector line between numbers (desktop only)

### 6. Pricing
- Section title: "Simple, Transparent Pricing"
- Single pricing card (centered, prominent):
  - **$500** one-time setup fee
  - **$200/month** ongoing
  - **No contracts. Cancel anytime.**
  - Feature list: Custom-trained chatbot, Lead capture & notifications, Ongoing updates & support, 24/7 uptime
  - CTA button: "Get Started" → scrolls to contact section
- Background: `--bg-surface`

### 7. Demo
- Section title: "See It In Action"
- Subtext: "Chat with a live example of the AI we build for businesses like yours."
- Large CTA button: **"Try the Live Demo"** → opens Voiceflow link in new tab
- Subtle animated pulse on the button for attention

### 8. Contact
- Section title: "Let's Build Your Chatbot"
- Form fields: Name, Email, Business Name, Message (textarea)
- Submit button: "Send Message"
- Form action: `mailto:` (opens default mail client)
- Background: `--bg-surface-2`

### 9. Footer
- "© 2026 Build Velocity AI. All rights reserved."
- Centered, muted text

---

## Interactions & Animations

- **Scroll animations:** Elements fade + slide up on enter (Intersection Observer, `opacity: 0 → 1`, `translateY: 30px → 0`)
- **Smooth scroll:** All anchor links scroll smoothly via CSS `scroll-behavior: smooth`
- **Button hover:** Scale up slightly (`transform: scale(1.03)`) + darken background
- **Mobile nav:** Toggle class on hamburger click; nav links stack vertically

---

## Responsiveness

- **Breakpoint:** 768px
- Below 768px: nav collapses, 3-column grids become 1-column, hero text scales down
- No horizontal scroll at any viewport width

---

## Constraints

- No backend — form uses `mailto:` action
- No external fonts or icon libraries — use Unicode/emoji icons or CSS-drawn shapes
- File must work when opened directly from disk (no localhost required)
