# Design System: Indira International School

## 1. Visual Theme & Atmosphere
A trustworthy, academic, and accessible interface. The density is balanced (Daily App Balanced) to ensure readability on small mobile screens. Variance is predictable but not boring, using structured asymmetry. Motion is calm, focused on tactile feedback rather than flashy animations. The atmosphere is professional, welcoming, and clearly focused on education.

## 2. Color Palette & Roles
The design system supports both **Light** and **Dark Mode** via CSS variables (`body.dark-mode`), swapping Canvas, Surface, Text, and Border colors while maintaining the Academic Blue accent.
* **Canvas White** (`#F9FAFB`) / Dark (`#121212`) — Primary background surface for a clean, breathable look.
* **Pure Surface** (`#FFFFFF`) / Dark (`#1E1E1E`) — Card and container fill.
* **Charcoal Ink** (`#18181B`) / Light Text (`#F9FAFB`) — Primary text, ensuring high contrast and readability.
* **Muted Steel** (`#71717A`) / Light Muted (`#A1A1AA`) — Secondary text, descriptions, and metadata.
* **Whisper Border** (`rgba(226,232,240,0.5)`) / Dark Border (`rgba(255,255,255,0.1)`) — Card borders, 1px structural dividers.
* **Academic Blue** (`#1E3A8A`) / Bright Blue (`#3B82F6`) — Accent color for CTAs, buttons, and active states.

## 3. Typography Rules
* **Display:** `Outfit` (or `Satoshi`) — Track-tight, controlled scale, weight-driven hierarchy. Modern sans-serif that looks premium.
* **Body:** `Outfit` — Relaxed leading, maximum 65 characters per line for desktop readability.
* **Hindi Support:** `Noto Sans Devanagari` — Clean fallback for Hindi toggles.
* **Banned:** `Inter`, `Times New Roman`, generic system fonts, pure black (`#000000`).

## 4. Component Stylings
* **Buttons:** Flat, no outer glow. Tactile push feedback (-1px translate) on active. Accent fill (Academic Blue) for primary, outline for secondary. High contrast white text on primary. Minimum 44px height for mobile touch targets.
* **Cards:** Generously rounded corners (1rem to 1.5rem). Diffused whisper shadow. Used only when elevation serves hierarchy (e.g., highlighting a specific facility). 
* **Inputs/Forms:** Label above the input, error reporting below. Focus ring in Academic Blue. Standard gap spacing. No floating labels to keep it simple and accessible.
* **Images:** Soft rounded corners. Embedded inline where appropriate. Never overlapping text.

## 5. Layout Principles
* **Mobile-First Focus:** Strict single-column collapse below 768px. All tap targets at least 44px.
* **Grid Architecture:** CSS Grid over Flexbox math. Max-width containment (e.g., 1200px centered) for desktop viewing.
* **Spacing:** Generous internal padding and vertical section gaps. Elements must breathe. No overlapping elements. 
* **Avoidance:** No 3-column equal card layouts horizontally if it feels generic; use asymmetric grids or alternating left-right blocks for features (Facilities/Academics).

## 6. Motion & Interaction
* **Tactile Interactions**: Spring physics for button presses. 
* **Hover States**: Subtle background shifts or gentle translation (e.g., cards lifting 2px on hover on desktop).
* **Scroll Animations**: Elements fade and slide up as they enter the viewport using lightweight `IntersectionObserver` (`.animate-on-scroll` class).
* **Performance**: Animate exclusively via `transform` and `opacity`. No heavy JavaScript scrolljacking.

## 7. Anti-Patterns (Banned)
* No emojis anywhere.
* No generic AI copywriting clichés ("Unleash your potential", "Next-Gen education").
* No 3-column equal generic feature grids.
* No scroll-jacking or bouncy chevrons ("Scroll down").
* No overlapping text on complex images without a solid overlay.
* No neon glows, intense drop shadows, or gradient text.
* No pure black text (`#000000`).
