# Advocate Suraj Lala — professional information site

A single-page static website with English, Bengali and Hindi language options. It uses semantic HTML, inline CSS and vanilla JavaScript, with Tailwind CSS and Google Fonts loaded from their CDNs. Subtle reveal and accent animations respect reduced-motion preferences. There is no backend, form, cookie, or tracking code.

## Edit the site

Open `index.html` and edit the `CONFIG` object near the top of the file. The supplied email, Rampurhat location/address, office hours, LL.B. qualification and Rampurhat Bar Association membership are populated. Verify them before deployment. Clear optional strings (`""`) or use an empty qualifications array (`[]`) to omit a field. The WhatsApp number is country code plus number, digits only; verify it before publishing.

- `portraitUrl`: path or URL of the portrait. The supplied portrait is in `images/advocate-suraj-lala.webp`; replace the file or clear this field to hide it.
- `mapEmbedUrl`: Google Maps embed URL for the office. The current value searches the supplied Rampurhat location; update it if the map pin should point to a more precise office location.
- `ecourtsProfile`: public profile link; blank hides the link.
- `profileNote`, `profileNoteBn`, `profileNoteHi`: the English, Bengali and Hindi About paragraphs. Keep these factual and neutral. Do not add case records, client names, outcomes, ratings, testimonials, experience claims, fee offers or solicitation language.

To edit translations, update the `data-en`, `data-bn` and `data-hi` values in the HTML. The language selector switches page text, metadata, contact details and the WhatsApp prefilled message. The preference is saved in `localStorage` inside `try/catch`.

Before publishing, verify each professional detail, map location and contact number. Keep the footer disclaimer accurate and have the advocate verify it.

## WhatsApp message

The page builds a `https://wa.me/<country-code-and-number>?text=<encoded-message>` link from `CONFIG.whatsappNumber`. English, Bengali and Hindi enquiry messages are encoded when the language changes. Buttons open in a new tab with `rel="noopener"`.

## Deploy free on Netlify

1. Go to [Netlify](https://www.netlify.com/) and sign in or create an account.
2. Choose **Add new site → Import an existing project**, connect the GitHub repository `yankeeDamn/AdvocateSuraj`, and select `main`.
3. Leave the build command empty and set the publish directory to `.` (the repository root), then deploy.
4. Netlify serves `index.html` directly. Add a custom domain in site settings if desired.

You can also deploy the same static root on Vercel with no build command and `.` as the output directory.
