# Ritik Panchal — Portfolio

A personal portfolio built with HTML, CSS, and JavaScript. It does not need a framework, paid service, package installation, or build step.

## 1. Find your files

Keep these files together in the same folder:

| File | What it does |
| --- | --- |
| `index.html` | All website sections, text, contact details, and links. Edit this for most content changes. |
| `style.css` | Colors, backgrounds, typography, spacing, and responsive layouts. |
| `script.js` | Mobile navigation and the automatic copyright year. |
| `Profile1.png` | Your profile photograph. The filename is case-sensitive on GitHub Pages. |
| `favicon.svg` | The small icon shown in the browser tab. |
| `README.md` | This editing and publishing guide. |
| `Ritik_Panchal_Resume.pdf` | Your original resume. It is **not currently linked** from the website. Review it before publishing. |

## 2. Preview and edit safely

1. Open this folder in VS Code.
2. Open `index.html` in a browser: find the file in Finder and double-click it, or right-click it and choose a browser under **Open With**.
3. In VS Code, open the file you want to change. Press **Command + F** on a Mac to find existing text.
4. Change the text between the HTML tags. Avoid accidentally deleting tags such as `<p>` and `</p>`.
5. Save with **Command + S**, return to the browser, and refresh.
6. Check the edited section at a desktop width and a narrow mobile width. You can use your browser's developer tools to simulate a phone.

**Tip:** Make one small change at a time. If something breaks, undo with **Command + Z**, save, and refresh. Back up your files before a large redesign.

## 3. Update website content

All examples below are in `index.html`. You can use Find to locate the text or class names mentioned.

### Change your introduction or headline

1. Search for `Engineering quality.` or `I help teams`.
2. Edit the visible words, leaving the surrounding tags intact.
3. Update `3+ years of experience` when appropriate. The number is currently written as text; it does **not** update automatically.
4. Save and refresh.

### Add a skill

1. Search for the skill category, such as `Software testing` or `Browser automation`.
2. Find the `<div class="tags">` inside that card.
3. Add a new line before its closing `</div>`:

```html
<span>Your verified skill</span>
```

4. Save and refresh. Only list skills you actually have.

### Update professional experience

1. Search for the company name or its date, such as `JUN 2024 — PRESENT`.
2. Edit the role, dates, description, or list items.
3. To add a responsibility, insert a new item inside the relevant `<ul>`:

```html
<li>Describe your verified contribution here.</li>
```

4. When a current role ends, update its dates and remove the `CURRENT ROLE` badge. Change `class="timeline-content current"` to `class="timeline-content"`.
5. To add a role, copy a complete `timeline-item` article, paste it inside the `timeline` container above older roles, and edit all its details. Check that each opening tag has a matching closing tag.

### Add or update a case study

The existing work entries are **areas of expertise with placeholders**, not claims of completed public projects.

1. Search for the entry title or `DETAILS TO BE ADDED`.
2. Replace the title and description with accurate, shareable details. Change the placeholder label only when you have real details to publish.
3. To add an entry, copy one complete `<article class="work-item"> ... </article>` within the `work-list` container and paste it after an existing entry.
4. Change the number, category, title, description, and label.
5. If you add a link, test it. Do not invent repositories, client details, project results, or URLs; check confidentiality before publishing work material.

### Update education or activities

Search for the institution, degree, or activity name and edit the corresponding heading, description, or date. Save and refresh.

### Change email, phone, or LinkedIn

1. Search for the current detail in `index.html`.
2. Update **every occurrence**, including both the visible text and the link destination in `href`.
3. Keep the correct link format:

```html
<a href="mailto:your-address@example.com">your-address@example.com</a>
<a href="tel:+911234567890">+91 12345 67890</a>
<a href="https://www.linkedin.com/in/your-profile/">LinkedIn</a>
```

4. Save, refresh, and test each link. Email links need a configured mail app; phone links normally open a dialer on supported devices.

The current phone number is intentionally displayed publicly in the contact section. Remove both its visible text and its whole `<a ...>...</a>` element if you no longer want it public.

## 4. Update the photo or appearance

### Replace the profile photo

1. Choose a photo you have permission to publish. Consider cropping and compressing it so it loads quickly.
2. Back up the existing `Profile1.png` if you want to keep it, then replace it with your new image using the **same exact filename and matching image format**. Alternatively, use a new filename and update `src="Profile1.png"` in `index.html` to match it exactly.
3. Refresh the browser. If the old picture remains, try a hard refresh (on most Mac browsers, **Command + Shift + R**).
4. Upload the new image file when updating the published site.

The current file is named `Profile1.png` but contains JPEG image data. Browsers generally identify it by its contents, but for consistency you can replace it with a real PNG, or rename a JPEG to a `.jpg` filename and update the `src` reference and deployment upload accordingly.

### Change colors or background

1. Open `style.css` and search for `Rich, layered light surfaces`. This is the latest background palette and overrides earlier theme rules.
2. In the `:root` rule below that comment, edit values such as `--bg` (page background), `--text` (main text), `--muted` (secondary text), and `--accent` (highlights).
3. The following `body`, `.section-alt`, `.card`, and `.contact-box` rules control gradients and other surfaces. Edit their color values if you want a broader change.
4. Save and refresh. Check text readability, button contrast, and focus indicators on every surface. Some component rules use their own colors, so changing a variable alone will not recolor every element.

There are older theme rules earlier in the file; later matching rules can override them. If a color change has no effect, search for the same selector farther down the file. Keep a backup before removing or reorganizing styles.

### Change the hero portrait shape or size

Search `Art direction` in `style.css`, then find `.profile-card img`. Its `width`, `border-radius`, and `box-shadow` control the portrait. Mobile overrides appear later in `@media` rules; check both desktop and mobile after changes.

### Change an expertise icon

Search the relevant heading in `index.html`, such as `Healthcare / HMIS`. The `<svg>` immediately before it defines the icon. Replace the complete SVG with another accessible, decorative SVG; keep `aria-hidden="true"` on its surrounding `expert-icon` span. Do not remove the visible heading.

## 5. Add a resume download

The website currently says **Resume available on request**; it does not download the original PDF.

1. Review your resume PDF carefully for everything you are comfortable making public, including your phone number and any other personal details. You have chosen to display your phone number on the website; you can still remove it from the PDF if you prefer.
2. Create a public version and save it beside `index.html` as, for example, `resume-public.pdf`.
3. In `index.html`, search for the `<p class="resume-note">` paragraph and replace that whole paragraph with:

```html
<p class="resume-note"><a href="resume-public.pdf" download>Download resume ↓</a></p>
```

4. Save and click the link in your browser. Check that it opens or downloads the intended PDF.
5. When publishing, upload the public PDF and updated `index.html`. Do not upload the original PDF unless you have reviewed and chosen to publish it.

## 6. Publish free with GitHub Pages

1. Sign in or create an account at [GitHub](https://github.com/).
2. Choose **+ → New repository**, name it for example `portfolio`, and select **Public**. Create the repository.
3. Choose **Add file → Upload files**. Upload `index.html`, `style.css`, `script.js`, `favicon.svg`, and `Profile1.png` to the repository root. You may also upload this guide. Upload a resume only after reviewing it for public sharing.
4. Select **Commit changes**.
5. Open the repository's **Settings → Pages**. Under **Build and deployment**, select **Deploy from a branch**, choose your default branch and `/ (root)`, then save.
6. Wait for the deployment to finish; the Pages settings will display the live URL. It usually looks like `https://YOUR-USERNAME.github.io/portfolio/`.
7. Open that URL in a private browser window and on a phone. Verify the photo, navigation, email, phone, LinkedIn, and resume download if you added one.

A public repository makes the files you upload publicly accessible, not just the content visibly linked on the page. Review files before uploading.

### Publish future changes

1. Edit and save files locally, then preview them.
2. Open your repository on GitHub and upload each changed file to the same location and branch. Commit the changes.
3. Wait for Pages to rebuild, then refresh the public URL. If an image or style looks outdated, try a hard refresh.
4. Recheck links and mobile layout after major changes.

## 7. Add the portfolio to LinkedIn

1. Open your LinkedIn profile and find **Featured**. If needed, use **Add profile section → Recommended → Add featured**.
2. Choose **+ → Add a link**, paste your live GitHub Pages URL, and save it with a title such as “Ritik Panchal | QA Portfolio.”
3. You can also add the URL to your contact information, email signature, and job applications. Check the public link before sharing it.

## 8. Quick check before sharing

- Read the content for accuracy, spelling, current role dates, and experience years.
- Check mobile and desktop layouts, scrolling, menu, and keyboard focus.
- Test email, phone, LinkedIn, and any case-study or resume links.
- Confirm the profile photo loads and that filenames match exactly.
- Review the resume and every uploaded file for information you intend to make public.
- Check the browser console for errors and open the public URL in a private window.
