# PrepAI — AI-Powered Placement Preparation Website

A fully static, single-file HTML website for an AI-driven placement preparation platform targeting engineering students. No frameworks, no build step — open in any browser.

---

## Quick Start

```bash
# Clone or download the file
open ai-placement-prep.html       # macOS
start ai-placement-prep.html      # Windows
xdg-open ai-placement-prep.html   # Linux
```

That's it. No dependencies to install, no server required.

---

## File Structure

```
ai-placement-prep.html    # Entire website — HTML + CSS + JS in one file
README.md                 # This file
```

---

## Sections

| Section | Description |
|---|---|
| **Navbar** | Fixed top bar with smooth-scroll links and a CTA button |
| **Hero** | Headline, subtext, CTA buttons, and an animated terminal mock interview |
| **Stats Bar** | Key social proof numbers (students placed, questions practiced, pass rate) |
| **Features** | 6-card grid covering the platform's core capabilities |
| **Topics Table** | DSA + CS fundamentals with difficulty tags and progress bar indicators |
| **Interview Demo** | Chat UI showing an AI interviewer mid-session with live feedback |
| **Roadmap** | 5-step student journey from skill assessment to final mock week |
| **Testimonials** | 3 student success cards with company and college details |
| **Pricing** | Free / Pro / Campus tiers with feature comparison |
| **CTA + Footer** | Final conversion section and footer navigation |

---

## Design System

### Fonts
Loaded from Google Fonts — requires an internet connection to render correctly.

| Role | Family |
|---|---|
| Display / Headings | Space Grotesk (700) |
| Body / UI | Inter (400, 500, 600) |
| Terminal / Code | JetBrains Mono (400, 500) |

### Color Palette

| Variable | Hex | Usage |
|---|---|---|
| `--navy` | `#0B1120` | Page background |
| `--card` | `#141c2e` | Card backgrounds |
| `--indigo` | `#6366F1` | Primary actions, accents |
| `--indigo-light` | `#818CF8` | Hover states, subtle accents |
| `--mint` | `#34D399` | Success, progress, live indicators |
| `--amber` | `#F59E0B` | Warnings, medium difficulty |
| `--coral` | `#F87171` | Hard difficulty tags |
| `--text` | `#F0F4FF` | Primary text |
| `--text2` | `#94A3B8` | Secondary / body text |
| `--text3` | `#64748B` | Muted / metadata text |

---

## Customization

### Changing the brand name
Search for `PrepAI` and `Prep<span class="dot">AI</span>` and replace with your brand name.

### Updating stats
Find the `.stats-row` section and edit the numbers inside `.stat-num` elements.

### Adding/removing pricing tiers
Each plan is a `.price-card` div inside `.pricing-grid`. Copy, edit, or remove cards freely.

### Swapping the terminal content
Edit the `.terminal-body` div in the hero section. Lines use these classes:
- `.term-sys` — system/meta messages (gray)
- `.term-q` — interviewer speech (mint green)
- `.term-a` — candidate speech (muted)
- `.term-score` — score/evaluation lines (amber)

### Updating topic rows
Each row in the topics table is a `.topic-row` div. Adjust the topic name, difficulty tag class (`tag-easy`, `tag-medium`, `tag-hard`), problem count, and the `width` percentage on the `.progress-bar` div.

### Changing currency / pricing
The pricing section uses `₹` (Indian Rupee). Find and replace with your currency symbol and amounts.

---

## Responsive Behavior

| Breakpoint | Behavior |
|---|---|
| `> 768px` | Two-column layouts for Interview Demo and Roadmap sections |
| `< 768px` | All grids collapse to single column (handled via JS resize listener) |
| `< 640px` | Navbar links hidden; Topics table shows only first 2 columns |

---

## Extending the Site

To turn this into a functional app, the natural next steps are:

- **Auth** — Add Clerk, Supabase Auth, or Firebase for user accounts
- **Practice engine** — Connect a LeetCode-style code editor (e.g. Monaco Editor via CDN)
- **AI interviews** — Wire the chat UI to the Anthropic API (`claude-sonnet-4-20250514`)
- **Resume review** — Accept PDF uploads, send to AI API with a structured review prompt
- **Progress tracking** — Store completion data in localStorage or a backend (Supabase / Firebase)
- **Payments** — Integrate Razorpay (India) or Stripe for the Pro and Campus plans

---

## Browser Support

Works in all modern browsers. No polyfills needed.

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

---

## License

MIT — free to use, modify, and deploy for personal or commercial projects.
