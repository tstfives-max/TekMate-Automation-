# TekMate Automation — Website Master Prompt

> Paste everything below the line into your AI website builder (Lovable, v0, Bolt, Framer AI, Claude, Cursor, etc.).
> **Content** comes from the live TekMate site (https://www.tekmateautomation.in/).
> **Design** must be a faithful re-skin in the style of **https://thenoema.site/**.
> Lines marked `[VERIFY]` should be checked against the live site before launch.

---

## ROLE

You are a senior product designer and front-end engineer. Build a production-ready, single-page marketing website for **TekMate Automation Pvt. Ltd.**, a smart home automation company in Patna, Bihar.

**The rule for this project:** keep TekMate's content and swap in Noema's design.
- Every piece of **content** (copy, services, products, contact details) comes from TekMate, listed below. Do not invent services, clients, testimonials or statistics.
- Every piece of **design** (layout, typography, color, spacing, components, motion, section rhythm) is copied from **https://thenoema.site/**.

---

## STEP 1: STUDY THE DESIGN REFERENCE FIRST

Open **https://thenoema.site/** and extract its design system before writing any code. Record these values as CSS custom properties on `:root`:

| Token | What to capture from thenoema.site |
|---|---|
| `--bg`, `--bg-alt` | Page background and alternate section background |
| `--ink`, `--ink-muted` | Primary and secondary text colors |
| `--accent` | Accent / highlight color used on CTAs, links, markers |
| `--line` | Hairline / border color |
| `--font-display` | Headline typeface (family, weights, italic usage, letter-spacing) |
| `--font-body` | Body typeface, size, line-height |
| `--font-mono` (if used) | Eyebrow / label / number typeface |
| `--radius` | Corner radius on buttons, cards, images |
| `--space-*` | Section padding, grid gutter, max content width |
| Motion | Scroll reveals, hover states, marquee, cursor, page-load sequence, easing & durations |

Then mirror these from Noema:
- **Navigation:** placement, logo treatment, link style, CTA button, mobile menu behaviour.
- **Hero composition:** headline scale, line breaks, alignment, supporting text position, imagery or graphic treatment, CTA style.
- **Section rhythm:** order and visual weight of sections, use of eyebrows and labels, numbered lists, split layouts, full-bleed bands.
- **Components:** buttons, cards, list rows, dividers, tags/pills, FAQ/accordion, form fields.
- **Footer:** structure, size of the wordmark, column layout.
- **Overall mood:** match Noema's tone exactly (whitespace, contrast, restraint). Don't introduce glassmorphism, neon gradients, or a "tech startup" look unless Noema uses them.

> If you cannot open the reference URL, stop and ask me for screenshots. Do not guess Noema's look.

---

## STEP 2: CONTENT (TekMate, use as-is)

### Brand
- **Name:** TekMate Automation Pvt. Ltd.
- **Category:** Smart Home Automation Solutions
- **Positioning:** Over 15 years of expertise in smart home automation, covering automated lighting, climate control, smart locks and surveillance systems.
- **Location:** Patna, Bihar, India

### Navigation
Home · About · Products · Why TekMate · Contact. Primary CTA: **Get a Free Consultation** (or Noema's CTA pattern with this label).

### Hero
- **Eyebrow:** Smart Home Automation · Patna
- **Headline (adapt line-breaks to Noema's hero):** *Smarter homes. Safer living. Effortless control.*
- **Subtext:** From automated lighting and climate control to smart locks and surveillance systems, TekMate brings over 15 years of expertise to make your home intelligent, secure and energy-efficient.
- **CTAs:** `Get a Free Consultation` (primary) · `Explore Products` (secondary)

### About
TekMate Automation designs and installs complete smart home systems for homes and businesses across Patna and Bihar. With over 15 years of hands-on expertise, we put lighting, climate, security and convenience in one system you control from your phone or voice assistant. `[VERIFY: years-of-experience claim]`

### Products / Solutions (one card or row each, in Noema's list or card style)
1. **Automated Lighting** — Scenes, schedules and dimming, controlled from your phone or by voice.
2. **Climate Control** — Automated thermostats that learn your preferences and habits to keep you comfortable and cut waste.
3. **Smart Door Locks** — Keyless, app-controlled entry with access logs and remote locking.
4. **CCTV Surveillance** — HD cameras with remote monitoring from anywhere.
5. **Motion Detectors & Real-Time Alerts** — Instant notifications the moment something moves.
6. **Smart Touch Switches** — Modern touch panels that replace traditional switchboards.
7. **Alexa-Ready Homes** — Control your entire home with your voice.
8. **Water Tank Sensors** — Automatic level monitoring to prevent overflow and dry-runs.

### Why TekMate (feature list, use Noema's numbered or split-column style)
- **Security** — Smart locks, CCTV, motion detectors and real-time alerts with remote monitoring.
- **Energy Efficiency** — Automated thermostats and lighting adjust to your preferences and habits, minimizing waste.
- **Convenience** — One app and one voice command for the whole home.
- **Local Expertise** — Patna-based team handling consultation, installation and support. `[VERIFY]`
- **15+ Years of Experience** `[VERIFY]`

### How It Works (only if Noema has a process or step section)
01 Consultation → 02 Custom Design → 03 Professional Installation → 04 Ongoing Support `[VERIFY: TekMate's actual process]`

### Final CTA band
- **Headline:** Ready to make your home smart?
- **Subtext:** Book a free consultation with our automation experts.
- **Button:** `Call 91423 50754` / `Get a Free Consultation`

### Contact
- **Address:** Ayodhya Villa, Near Patna Tyre Mall, Tribuvan More, Khagaul Road, Patna, Bihar 801503
- **Phone:** +91 91423 50754 (alternate listed online: +91 87920 97889) `[VERIFY which is primary]`
- **Email:** khalid@tekmateautomation.in
- **WhatsApp:** floating button linking to `https://wa.me/919142350754` `[VERIFY number]`
- **Contact form fields:** Name, Phone, Email, Property type (Apartment / Villa / Office / Other), Interested in (multi-select of the products above), Message.
- Embed a Google Map of the address.

### Footer
TekMate wordmark (sized like Noema's footer wordmark) · quick links · products · contact block · `© {current year} TekMate Automation Pvt. Ltd. All rights reserved.`

---

## STEP 3: TECHNICAL REQUIREMENTS

- **Stack:** semantic HTML5 + modern CSS (custom properties, grid, `clamp()` type scale) + vanilla JS. If you are a React-based builder, use React + Tailwind and map the Noema tokens into the Tailwind theme.
- **Responsive:** mobile-first; breakpoints at 640 / 1024 / 1440 px; no horizontal scroll; hamburger nav on mobile using Noema's mobile pattern.
- **Motion:** reproduce Noema's animations with CSS + `IntersectionObserver` (or GSAP if Noema clearly uses it). Respect `prefers-reduced-motion`.
- **Imagery:** use high-quality smart-home photography (modern Indian homes, lighting scenes, touch panels, door locks, cameras) treated to match Noema's image style (crop, radius, grain, duotone, etc.). Use descriptive `alt` text.
- **Accessibility:** WCAG 2.1 AA contrast, visible focus states, keyboard-navigable menu and form, `aria-label` on icon buttons.
- **Performance:** Lighthouse ≥ 90 on all categories; lazy-load images; preload display font; no layout shift.
- **SEO:**
  - `<title>`: TekMate Automation | Smart Home Automation in Patna, Bihar
  - Meta description: Smart home automation in Patna: automated lighting, climate control, smart locks, CCTV surveillance and Alexa-ready homes. 15+ years of expertise. Free consultation.
  - Open Graph and Twitter tags, favicon, and `LocalBusiness` JSON-LD with the address, phone, email and geo above.
- **Forms:** client-side validation; submit to a configurable endpoint (Formspree / Web3Forms / mailto fallback); success and error states styled like Noema.
- **Deliverable:** a single `index.html` (inline CSS/JS) **or** a clean project folder, plus a short README on how to edit content and deploy to Vercel/Netlify.

---

## STEP 4: QUALITY CHECKLIST (verify before you finish)

- [ ] Placed side by side with thenoema.site, it reads as the same design system with TekMate's content.
- [ ] No content was invented: no fake testimonials, client logos, awards or stats.
- [ ] All `[VERIFY]` items are flagged to me in your final message.
- [ ] Phone, email, WhatsApp and map links all work.
- [ ] Looks correct at 375 px, 768 px, 1280 px and 1920 px.
- [ ] Reduced-motion and keyboard navigation both work.
