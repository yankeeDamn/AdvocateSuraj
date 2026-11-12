# Advocate Suraj Lala — professional information site

A single-page, bilingual English/Bengali static website. It uses semantic HTML, inline CSS and vanilla JavaScript, with Tailwind CSS and Google Fonts loaded from their CDNs. There is no backend, form, cookie, or tracking code.

## Edit the site

Open `index.html` and edit the `CONFIG` object near the top of the file. Replace the sample email, office address, enrolment details, bar association, qualification, office hours and last-updated date with verified information. Clear a string (`""`) or use an empty qualifications array (`[]`) to omit optional information. Contact fields containing `XXXX` are hidden. The WhatsApp number is country code plus number, digits only; verify it before publishing.

- `portraitUrl`: optional URL of an image you have permission to use. The portrait area stays typographic when blank.
- `mapEmbedUrl`: optional Google Maps embed URL for the office. Use an embed URL, not a search or sharing URL. The map placeholder appears when blank.
- `ecourtsProfile`: public profile link; blank hides the link.
- `profileNote`: optional short factual profile paragraph.

To edit or add translations, update the `data-en` / `data-bn` values in the HTML. The language button switches all page strings and updates the WhatsApp prefilled message; the preference is saved in `localStorage` inside `try/catch`.

Before publishing, check every professional detail, verify the contact number, and replace or remove all remaining `XXXX` placeholders. Keep the footer disclaimer accurate and have the advocate verify it.

## WhatsApp message

The page builds a `https://wa.me/<country-code-and-number>?text=<encoded-message>` link from `CONFIG.whatsappNumber`. English and Bengali enquiry messages are encoded when the language changes. Buttons open in a new tab with `rel="noopener"`.

## Deploy free on Netlify

1. Go to [Netlify](https://www.netlify.com/) and sign in or create an account.
2. Choose **Add new site → Import an existing project**, connect the GitHub repository `yankeeDamn/AdvocateSuraj`, and select `main`.
3. Leave the build command empty and set the publish directory to `.` (the repository root), then deploy.
4. Netlify serves `index.html` directly. Add a custom domain in site settings if desired.

You can also deploy the same static root on Vercel with no build command and `.` as the output directory.
