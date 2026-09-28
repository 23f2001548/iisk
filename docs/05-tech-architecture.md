# Technical Architecture & Stack

## 1. Recommended Tech Stack
For a simple, fast, and low-maintenance informational website, we recommend a **Static Site Generation (SSG)** approach or pure static files.
* **Core**: HTML5, Vanilla CSS (following the Design System), and minimal Vanilla JavaScript. (Avoid heavy frameworks to keep the site blazing fast on mobile networks).
* **Hosting**: **Cloudflare Pages** or **Netlify**. Both offer generous free tiers perfect for static sites. They provide built-in SSL (HTTPS), global CDNs for fast loading, and easy deployment from a Git repository.
* **Form Handling**: **Web3Forms** or **Formspree**. These services provide a simple API endpoint to post form data and receive it directly via the school's email, eliminating the need for a backend server or database.

## 2. Folder Structure
```text
/indira-international-school
├── /docs                 # Project documentation (Phase 1 files)
├── /src                  
│   ├── /assets           # Images, logos, PDF downloads
│   ├── /css              # Vanilla CSS files (index.css, variables.css)
│   ├── /js               # Minimal logic (mobile menu, form validation)
│   └── /components       # Reusable HTML snippets (if using a basic SSG like Eleventy or Vite)
├── index.html            # Home Page
├── about.html            # About Us
├── academics.html        # Academics
├── facilities.html       # Facilities
├── admissions.html       # Admissions
├── disclosure.html       # Mandatory Public Disclosure
└── contact.html          # Contact Us
```
*(If the build remains pure HTML without a generator, the root will just hold the `.html` files).*

## 3. Form to Email Flow
1. User submits the Enquiry form on the Contact page.
2. JavaScript intercepts the form, performs basic validation (e.g., ensuring 10-digit phone number).
3. Data is sent securely via a POST request to Web3Forms/Formspree.
4. The service sends a formatted email to `schoolindirainternational@gmail.com` and `indiraschoolkota@gmail.com`.
5. User sees a success message on the website.

## 4. Content Maintenance Strategy
Since there is no CMS, the content will be maintained directly in the code repository.
* Items that change rarely (like Vision, Mission, history) remain hardcoded in HTML.
* Items that might change occasionally (Announcements, new PDF links for CBSE disclosure) can be updated by editing the specific HTML file and pushing to GitHub, which auto-deploys via Netlify/Cloudflare.
* *Alternative*: If staff are completely non-technical, a simple free headless CMS like Decap CMS or Sanity can be integrated later, but for MVP, manual edits keep it simple and unbreakable.

## 5. Domain & Hosting Setup
* **Domain**: The school owns or needs to own `iiskota.com`. The DNS records will be pointed to Cloudflare Pages/Netlify.
* **SSL/HTTPS**: Handled automatically and for free by the hosting provider.

## 6. Estimated Costs (INR)
* **Hosting**: ₹0 / year (Cloudflare Pages or Netlify Free Tier).
* **Form Handling**: ₹0 / year (Web3Forms free tier covers up to 250 submissions/month, which is usually enough for local school enquiries).
* **Domain Renewal (`iiskota.com`)**: ~₹800 to ₹1,000 / year (depending on the registrar like GoDaddy or Namecheap).
* **Total Running Cost**: ~₹800 to ₹1,000 per year.
