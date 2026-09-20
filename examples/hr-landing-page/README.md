# HR services landing page

A single-file, dependency-free landing page for a fractional HR / people
operations practice. No build step, no framework — open `index.html` in a
browser, or drop it on any static host.

## Swap these before publishing

| Placeholder | Where | Replace with |
| --- | --- | --- |
| `Northline HR` | `<title>`, nav, footer | Your practice name |
| `hello@example.com` | contact section, footer | Your email |
| `+1 (555) 010-0143` | contact section | Your phone |
| `$X,XXX` | pricing tiers | Your rates, or delete the section |
| `Client logo` ×5 | trust strip | Your client marks, or delete the strip |
| Form `<form id="intro-form">` | contact section | A real form endpoint |

The contact form validates name and email client-side, then tells the visitor
it isn't connected to anything. Point it at a form service (Formspree, Basin,
Netlify Forms) and remove the `e.preventDefault()` in the inline script, or
delete the form and keep the mailto link.

## Content notes

The copy describes a generic fractional HR engagement — audit, stabilize, run
— using standard US HR terms of art (I-9, FLSA classification, EEO-1, ACA
1095-C, Form 941, COBRA, open enrollment). Read it as a starting draft, not a
statement about your practice: rewrite anything that doesn't match what you
actually do.

Nothing on the page claims a client, a result, or a metric. That was
deliberate — add your own, once they're true.

The compliance rhythm section carries a note that filing obligations vary by
headcount, entity type, and state. Keep something like it; the page should not
read as legal advice.

## Design

- Type: Newsreader (headings) and Instrument Sans (body) from Google Fonts,
  with system fallbacks, so the page still reads offline.
- Color: a deep green-teal accent on green-biased neutrals, defined once as
  CSS custom properties.
- Themes: light and dark, following `prefers-color-scheme` and honoring an
  explicit `data-theme` attribute if you add a toggle.
- Responsive down to ~360px; every grid collapses to one column.
