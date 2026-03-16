---
name: frontend-design
description: Load Mindful Academy frontend design guidelines, brand rules, and anti-generic guardrails before writing any frontend code
user-invocable: true
---

# Mindful Academy — Frontend Design Guidelines

You are now operating under the Mindful Academy frontend design system. Apply every rule below for all HTML/CSS/JS you write in this project.

## Brand Colors
- Primary orange: `#E8621A`
- Dark bg: `#111` / `#1A1A1A` / `#222`
- Text primary: `#fff`
- Text secondary: `#cccccc` / `#aaaaaa`
- Never use default Tailwind blue/indigo (blue-600, indigo-500, etc.)

## Typography
- Display/headings: `Cormorant Garamond` (serif)
- Body: `Inter` (sans-serif)
- Large headings: `letter-spacing: -0.03em`
- Body line-height: `1.7`
- Never use the same font for headings and body

## Shadows
- Never use flat `shadow-md`
- Use layered, color-tinted shadows with low opacity
- Example: `box-shadow: 0 4px 24px rgba(232,98,26,0.12), 0 1px 4px rgba(0,0,0,0.3)`

## Gradients & Texture
- Layer multiple radial gradients for depth
- Add grain/texture via SVG noise filter where appropriate
- Hero backgrounds: animated canvas or CSS gradient + grain overlay

## Animations
- Only animate `transform` and `opacity`
- Never use `transition-all`
- Use spring-style easing: `cubic-bezier(0.34,1.56,0.64,1)`

## Interactive States
- Every clickable element must have `hover`, `focus-visible`, and `active` states
- No exceptions

## Spacing
- Use intentional consistent spacing tokens (8px grid)
- Not random Tailwind steps

## Depth System
- Base surfaces: `#1A1A1A`
- Elevated: `#222` / `#2d2d2d`
- Floating (modals, dropdowns): `#333`

## Images
- Add gradient overlay: `bg-gradient-to-t from-black/60`
- Add color treatment layer with `mix-blend-multiply`

## Output Format
- Single `index.html` unless told otherwise
- All styles inline or in `<style>` block
- Tailwind via CDN: `<script src="https://cdn.tailwindcss.com"></script>`
- Placeholder images: `https://placehold.co/WIDTHxHEIGHT`
- Mobile-first responsive

## Brand Assets
- Logo and assets live in `brand_assets/` — always check before designing
- Use real assets where available; never replace with placeholders if real asset exists

## Reference Image Workflow
- If reference image provided: match layout, spacing, typography, color exactly
- Do not improve or add to the design — match it precisely
- Screenshot → compare → fix → re-screenshot (minimum 2 rounds)

## Local Server
- Always serve on `http://localhost:3000` via `node serve.mjs`
- Never screenshot a `file:///` URL

## Hard Rules
- Do not add sections/features not in the reference
- Do not "improve" a reference — match it
- Do not use `transition-all`
- Do not use default Tailwind blue/indigo as primary
