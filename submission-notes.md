 Semantic HTML Prototype — Submission Notes

Repository: (paste your GitHub URL here after you push this project)

1. Pages created
Home (`index.html`), About (`about.html`), Services (`services.html`), and Contact (`contact.html`) — a small prototype site for a fictional health clinic, "Sunrise Community Clinic."

 2. Navigation
A `<nav>` menu inside the `<header>` appears identically on all four pages, with links to Home, About, Services, and Contact. The current page's link is marked with `aria-current="page"`. Body text also includes descriptive inline links (e.g. "book an appointment") pointing to related pages.

3. Semantic HTML elements used
- `<header>` — site title and navigation, on every page
- `<nav>` — the main menu, with `aria-label="Main navigation"`
- `<main>` — the primary content area of each page
- `<section>` — groups related content (e.g. mission, services list)
- `<article>` — individual self-contained items (each service, each team highlight)
- `<aside>` — supplementary info such as opening hours and emergency notes
- `<footer>` — copyright notice on every page

4. Form
The Contact page (`contact.html`) contains the form. It collects a visitor's full name, email address, phone number, preferred service, and an optional message, so the clinic can process appointment requests.

5. Accessibility decisions
- Every form input has a `<label for="">` explicitly associated with its `id`, so screen readers announce the correct field name.
- Images use descriptive `alt` text that explains what's shown, not just a filename.
- Headings follow a logical order (`h1` for the site name, `h2` for section titles, `h3` for individual items) with no skipped levels.
- Link text is descriptive ("book an appointment," "our full range of services") rather than vague phrases like "click here."
- Visible focus outlines are defined in CSS so keyboard users can see which element is focused.
- `aria-current="page"` on the active nav link and `aria-label`/`aria-labelledby` on landmark regions give assistive technology extra context.

 Semantic HTML Prototype — Submission Notes

Name: MUGABI ELIJAH  
Access Number: B36787  
Project: Sunrise Community Clinic (fictional health clinic website)  
Repository: (paste your GitHub URL here after you push this project)

---

1. Project Overview
A four-page prototype website for a fictional community health clinic in Mukono, Uganda. The goal is to demonstrate correct use of **semantic HTML, consistent navigation, an accessible form, and basic responsive styling with a single shared stylesheet (`style.css`).

 2. Pages Created
| Page | File | Purpose |
|------|------|---------|
| Home | `index.html` | Hero banner, reasons to choose the clinic, announcements |
| About | `about.html` | Clinic story, mission, values, team, opening hours, outreach |
| Services | `services.html` | Service cards, sample fees table, hours and emergency aside |
| Contact | `contact.html` | Contact details, appointment request form, hours and emergency aside |

**Folder structure**
```
clinic/
├── index.html
├── about.html
├── services.html
├── contact.html
├── style.css
└── images/
    └── Hospital.jpg
```

3. Navigation
- A `<nav>` menu inside the `<header>` appears identically on all four pages, linking to Home, About, Services and Contact.
- The current page's link is marked with `aria-current="page"` and is highlighted visually by CSS.
- Body text also contains descriptive inline links (e.g. "book an appointment", "our full range of services") pointing to related pages.
- All links are relative, so the site works when opened locally or hosted on GitHub Pages.

4. Semantic HTML Elements Used
| Element | Where and why |
|---------|---------------|
| `<header>` | Site title and navigation, on every page |
| `<nav>` | Main menu, with `aria-label="Main navigation"` |
| `<main>` | Primary content area of each page (one per page) |
| `<section>` | Groups related content, e.g. mission, services, team; each has `aria-labelledby` |
| `<article>` | Self-contained items: each service, each team role, each mission point |
| `<aside>` | Supplementary info: opening hours, emergency notes, community outreach |
| `<footer>` | Copyright notice on every page |
| `<address>` | Contact details on the Contact page |
| `<table>` with `<caption>`, `<thead>`, `<tbody>`, `scope` | Opening hours and fees, with proper header cells |
| `<form>`, `<label>`, `<input>`, `<select>`, `<textarea>` | Appointment request form |

5. Form
The Contact page contains the form. It collects:
- Full name (required)
- Email address (required)
- Phone number (required)
- Preferred service (drop-down list of the six clinic services)
- Message (optional)

A small JavaScript check confirms the name, a valid email format and a phone number before showing a confirmation message. The form is a front-end prototype only; no data is sent to a server.

 6. Accessibility Decisions
- Every form input has a `<label for="">` explicitly linked to its `id`, so screen readers announce the correct field name.
- Images use descriptive `alt` text that explains what is shown, not just a filename.
- Headings follow a logical order (`h1` site name, `h2` section titles, `h3` individual items) with no skipped levels.
- Link text is descriptive ("book an appointment", "our full range of services") rather than vague phrases like "click here".
- Visible focus outlines are defined in CSS so keyboard users can see which element is focused.
- `aria-current="page"` on the active nav link and `aria-label` / `aria-labelledby` on landmark regions give assistive technology extra context.
- Tables use `<caption>` and `scope` attributes so data cells are read with the right headers.
- The form status message uses `role="status"` and `aria-live="polite"` so feedback is announced.
- Colours were chosen with strong contrast between text and background.
- The viewport meta tag and flexible CSS layout keep the pages readable on phones and tablets.
- `lang="en"` is set on every page.

7. Styling and Responsiveness
- One external stylesheet (`style.css`) is shared by all pages for a consistent look.
- CSS variables define the colour palette in one place.
- CSS Grid is used for card layouts, and a media query stacks the header and menu on screens narrower than 600px.
- Images scale with `max-width: 100%` so they never overflow the screen.

 8. Testing Done
- Opened every page in a browser and checked that all navigation links work.
- Checked keyboard navigation (Tab / Shift+Tab) through links and form fields.
- Resized the browser window to confirm the layout adapts to small screens.
- Validated the HTML with the W3C Markup Validator (https://validator.w3.org).

9. Challenges and Lessons Learned
- Keeping the heading hierarchy in order while using `<aside>` and nested sections.
- Choosing between `<section>` and `<article>`: `<article>` is for content that stands on its own, while `<section>` groups related content under a heading.
- Writing meaningful `alt` text and link text instead of generic phrases.

 10. How to Run the Project
1. Download or clone the repository.
2. Make sure the `images` folder contains `Hospital.jpg`.
3. Open `index.html` in any web browser.

11. How to Publish to GitHub
```bash
git init
git add .
git commit -m "Add Sunrise Community Clinic semantic HTML prototype"
git branch -M main
git remote add origin <your-repository-url>
git push -u origin main
```
Then paste the repository URL at the top of this document.

 12. Limitations and Future Improvements
- Connect the form to a backend or email service so requests are actually received.
- Add a map of the clinic location and a photo gallery page.
- Add an online appointment calendar and multilingual support (English and Luganda).
