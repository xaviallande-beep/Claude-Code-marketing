# Task 15 · Reflection: desktop vs mobile wireframe

*Draft. Adapt it to what you actually did in Figma before submitting.*

**Page:** Pleamar Escuela de Surf, a landing page for a surf school in Somo (Cantabria) with one goal: get a first-time surfer to book a lesson.

## What was the most difficult thing to adapt between versions?

The hardest part was keeping the booking action visible on mobile without filling the screen with buttons. On desktop the "Reservar" button sits in the header and is always visible. On a 390 px screen the header only has room for the logo and a menu icon, so I moved the button into a sticky bar at the bottom of the screen. It only appears once the hero buttons have scrolled out of view, so there are never two booking buttons on screen at once.

The second difficulty was length. Content that fits side by side on desktop (hero and surf report, pricing cards, testimonials, contact and form) has to stack on mobile, and the page grew from about 4,000 px to about 5,500 px. To keep it manageable I put the most-booked plan first and shortened the other two cards, turned the testimonials into a swipe carousel and kept the FAQ as an accordion.

## What was the creation process like?

1. **Content inventory.** I listed every section of the page in order of importance: offer, trust, price, how it works, social proof, objections, booking.
2. **Desktop first.** I drew the 1440 px frame on a 12-column grid, so every block uses 4, 5, 6, 7 or 8 columns and lines up.
3. **Mobile second.** I duplicated the content into a 390 px frame with 4 columns and went section by section, asking "does this still work at this width? If not, what changes?" Each change is numbered on the wireframe.
4. **Review.** I checked the fold line on both: the headline and both main buttons must be visible without scrolling.

I kept the wireframes in greyscale on purpose, so feedback is about structure and hierarchy, not colours.

## What Figma tools did I discover?

- **Frame presets** (Desktop, iPhone) to start at the right sizes.
- **Layout grids**: columns with margins and gutters, which made alignment much faster.
- **Auto layout**, to stack form fields and cards that resize when the text changes.
- **Components and variants** for buttons (primary / secondary) and accordion rows (open / closed).
- **Position "Fixed" when scrolling** (in Prototype mode), to make the mobile booking bar stay at the bottom.

## Screen design principles applied

Visual hierarchy (one H1, one primary button per area), proximity (trust facts next to the CTA), alignment to a grid, consistency (same card and button styles everywhere), the Z-pattern in the header, touch targets of at least 44 px on mobile and keeping key content above the fold.
