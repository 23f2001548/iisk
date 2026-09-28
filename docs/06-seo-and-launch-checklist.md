# SEO, Performance, and Launch Checklist

## 1. Local SEO & Meta Information
* [ ] **Google Business Profile (GBP)**: Ensure the school's GBP for "Indira International School, Raipura, Kota" is claimed, verified, and linked to the new website (`iiskota.com`).
* [ ] **Title Tags**: Descriptive titles for each page (e.g., `Indira International School | Best CBSE School in Raipura, Kota`).
* [ ] **Meta Descriptions**: Unique, compelling descriptions under 160 characters for key pages.
* [ ] **Open Graph Tags**: Add `og:title`, `og:image`, and `og:description` for better link sharing on WhatsApp and Facebook.

## 2. Schema Markup (Structured Data)
* [ ] Implement `EducationalOrganization` or `School` Schema.org JSON-LD on the Home page.
* Include properties: name, address, telephone, email, logo, sameAs (social links).

## 3. Performance & Asset Optimization
* [ ] **Images**: Compress all campus and gallery images. Serve in Next-Gen formats like WebP. Keep file sizes under 200KB where possible.
* [ ] **Caching & CDN**: Leverage Cloudflare or Netlify's built-in CDN edge caching.
* [ ] **Minification**: Minify CSS and JS before production deployment.
* [ ] **Target**: Achieve a Google Lighthouse Mobile Performance Score of **90+**.

## 4. Accessibility (a11y)
* [ ] **Contrast**: Ensure text colors (e.g., Charcoal Ink on Canvas White) meet WCAG AA contrast ratios.
* [ ] **Alt Text**: All meaningful images must have descriptive `alt` attributes (e.g., `alt="Students experimenting in the chemistry lab"`).
* [ ] **Tap Targets**: Mobile buttons and links must be at least 44x44px.
* [ ] **Form Labels**: All inputs in the Enquiry form must have associated `<label>` tags.

## 5. Launch / Testing Checklist
* [ ] Test form submission and verify emails are received at both school email addresses.
* [ ] Test WhatsApp click-to-chat link to ensure it opens the app correctly with a pre-filled message.
* [ ] Test the phone number `tel:` link on an actual mobile device.
* [ ] Verify all Mandatory Public Disclosure PDFs download correctly.
* [ ] Check responsive layout on small mobile (e.g., iPhone SE), standard mobile, and desktop.
* [ ] Generate and submit `sitemap.xml` and `robots.txt` to Google Search Console post-launch.
