# Semantic HTML Prototype — Submission Notes

**Repository:** *(paste your GitHub URL here after you push this project)*

## 1. Pages created
Home (`index.html`), About (`about.html`), Services (`services.html`), and Contact (`contact.html`) — a small prototype site for a fictional health clinic, "Sunrise Community Clinic."

## 2. Navigation
A `<nav>` menu inside the `<header>` appears identically on all four pages, with links to Home, About, Services, and Contact. The current page's link is marked with `aria-current="page"`. Body text also includes descriptive inline links (e.g. "book an appointment") pointing to related pages.

## 3. Semantic HTML elements used
- `<header>` — site title and navigation, on every page
- `<nav>` — the main menu, with `aria-label="Main navigation"`
- `<main>` — the primary content area of each page
- `<section>` — groups related content (e.g. mission, services list)
- `<article>` — individual self-contained items (each service, each team highlight)
- `<aside>` — supplementary info such as opening hours and emergency notes
- `<footer>` — copyright notice on every page

## 4. Form
The Contact page (`contact.html`) contains the form. It collects a visitor's full name, email address, phone number, preferred service, and an optional message, so the clinic can process appointment requests.

## 5. Accessibility decisions
- Every form input has a `<label for="">` explicitly associated with its `id`, so screen readers announce the correct field name.
- Images use descriptive `alt` text that explains what's shown, not just a filename.
- Headings follow a logical order (`h1` for the site name, `h2` for section titles, `h3` for individual items) with no skipped levels.
- Link text is descriptive ("book an appointment," "our full range of services") rather than vague phrases like "click here."
- Visible focus outlines are defined in CSS so keyboard users can see which element is focused.
- `aria-current="page"` on the active nav link and `aria-label`/`aria-labelledby` on landmark regions give assistive technology extra context.
