# LANGIT WAU STUDIO

ICT2215 Assessment 2: a fictional Malaysian Wau Bulan workshop studio. One HTML page, one external CSS file, three local photographs, original SVG motifs, a YouTube embed and a display-only form. No JavaScript, framework, package installation or build step.

Coursework author: **LiuYiyuan**, Student ID **i24029050**, Class **8C2**. Course: **ICT2215 — Web Design and Development with Multimedia**. Student academic contact: [i24029050@student.newinti.edu.my](mailto:i24029050@student.newinti.edu.my). This is the student's academic email, not a commercial contact for the fictional studio.

## Launch locally

Recommended browser: current Google Chrome or Microsoft Edge. Open PowerShell in this folder (the folder containing `index.html`), then run:

```powershell
python -m http.server 8000
```

Open **http://localhost:8000/**. Keep the terminal running during the demonstration; stop with Ctrl+C. If port 8000 is occupied, use `python -m http.server 8001` and open http://localhost:8001/.

If Python is unavailable, open this folder in VS Code, install the **Live Server** extension by Ritwick Dey, right-click `index.html` and select **Open with Live Server**. Use the HTTP URL it opens. Double-clicking the HTML file also loads local images and styles, but HTTP is the primary demonstration method and gives YouTube a normal referring origin.

The page, photographs and typography work offline. The YouTube player, linked sources and licence pages require internet access. Do not equate a loaded thumbnail with successful playback. Test the play control again on the actual presentation computer/network. See `docs/verification.md` for the observed result in this environment.

## Files

- `index.html`: four main sections (`home`, `about`, `services`, `contact`), navigation, form, media and expandable credits.
- `css/style.css`: shared palette, layout, component styles and responsive rules.
- `assets/images/`: three licensed, optimised local JPEGs.
- `MEDIA-CREDITS.md`: authors, source and licence links, modifications and reuse obligations.
- `docs/design-notes.md`: short design rationale; not an Assessment 3 report.
- `docs/verification.md`: original rubric audit and link to the current refinement review.
- `docs/refinement-review.md`: exact refinement changes, before/after screenshots and current verification.
- `docs/browser-results.json` and PNGs: genuine automated browser evidence.

## Explain the code

1. Start with the document language, character encoding, viewport meta tag and external stylesheet link.
2. `header` and `nav` contain ordinary fragment links. For example, `href="#about"` scrolls to `section id="about"`. `main` has a skip-link destination; each section has a heading.
3. The hero, story, workshop cards and contact layout use CSS Grid. Flexbox aligns navigation, buttons and smaller rows. `.container` caps the content at 1200px.
4. CSS variables in `:root` keep the palette consistent. Georgia supplies the editorial headings; the system sans-serif handles body text without a font download.
5. `object-fit: cover` fills selected image frames without stretching. Width and height attributes reserve image space. The video iframe uses `aspect-ratio: 16 / 9`.
6. At 760px and below, multi-column layouts stack and navigation stays visible. At 1050px and below, gaps and padding reduce. Focus outlines and reduced-motion rules support accessible use.
7. Every form field has an explicit label. The explanation above the fields identifies the form as display-only. There is no send or inactive demo button. The sole form button is `type="reset"`, which clears the fields. `method="dialog"` has no network submission: outside a dialog element the browser aborts form submission, providing extra protection against implicit Enter submission. Fields deliberately have no `name` attributes because this demo must not serialize data. There is no endpoint, script or storage code.
8. The three inline workshop SVGs represent the wau silhouette, floral pattern and wind. They are decorative (`aria-hidden="true"`); nearby text gives each offering its meaning.

## Two small live modifications

1. **HTML text:** in `index.html`, find `A little bamboo. A world of possibility.` Replace it with `Discover Malaysian craft, one detail at a time.` Save and refresh. Explain that the paragraph content changes while its class and styling remain intact.
2. **CSS spacing:** in `css/style.css`, find `.workshop { padding: 29px; ... }` and change `29px` to `35px`. Save and refresh at a desktop width above 1050px. Explain that padding adds space inside every workshop card through one repeated class. Restore afterward if desired.

Practise both changes personally. These instructions do not establish the student's ability to explain or independently modify the code.

## Coursework limits

No Assessment 1 materials or lecturer-provided rubric documents were present; alignment is **NOT VERIFIED**. The implementation follows the pasted brief, not unseen coursework. Workshops, studio identity and enquiry flow are illustrative; no real availability, prices, staff or contact details are asserted. No grade is predicted. Full source ownership does not remove the photographs' CC BY-SA attribution and share-alike obligations.
