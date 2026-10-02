# Social Media Text Formatter

A free, client-side **Unicode text styler for WhatsApp, Instagram, Twitter/X, and other social media**. Type your text once and instantly get it rendered in 12 stylish Unicode fonts — then copy any style with one click. No login, no tracking, everything runs in your browser.

🔗 **Live:** https://girishlade111.github.io/Social-Media-Text-Formatter/

## Features

- **12 text styles** — Bold, Italic, Bold Italic, Monospace, Cursive, Gothic (Fraktur), Bubble, Strikethrough, Underline, Wide, Uppercase, Lowercase
- **Live conversion** — every style updates as you type
- **One-click copy** — each style card has its own Copy button with visual feedback ("Copied!")
- **Unicode, not fonts** — the styled text is plain Unicode characters, so it works in WhatsApp chats, Instagram bios, tweets, Discord, and anywhere text is accepted — no font installation needed
- **Dark, responsive UI** — Tailwind CSS layout that adapts from mobile to desktop
- **100% client-side** — no backend, no build step, no analytics, works offline after first load

## Tech Stack

- Plain HTML, CSS, JavaScript (single `index.html` file, no bundler)
- [Tailwind CSS](https://tailwindcss.com/) via CDN for styling
- [Inter](https://fonts.google.com/specimen/Inter) font via Google Fonts
- Unicode character maps for font styles; combining characters (U+0336, U+0332) for strikethrough/underline

## Quick Start

No installation needed — the app is a single static file.

```bash
git clone https://github.com/girishlade111/Social-Media-Text-Formatter.git
cd Social-Media-Text-Formatter
# open index.html in any browser, or serve it:
npx serve .
```

## Project Structure

```
.
├── index.html   # entire app: markup, Tailwind styles, and formatting logic
└── README.md
```

## How It Works

Character maps translate each letter/digit into its styled Unicode equivalent (e.g. `a` → `𝗮` for Bold). The `formatters` array pairs each style with a transform function; `createFormatterCard` builds one UI card per style, and every `input` event re-renders all cards. Copy uses a temporary `<textarea>` + `document.execCommand('copy')` for maximum browser compatibility.

## Deploy Notes

Static site — deployable anywhere that serves static files (GitHub Pages, Cloudflare Pages, Netlify, or any static host). No environment variables, no build command.

---

**Built by Girish Lade** — https://ladestack.in
