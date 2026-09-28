# Deployment & Content Editing Guide

## 1. How to Deploy to Cloudflare Pages (Free & Recommended)

This website is a completely static HTML/CSS/JS site, making it incredibly easy and free to host.

### Initial Setup
1. **Push to GitHub**: Create a free GitHub account and push this entire repository to a new private repository.
2. **Sign up for Cloudflare**: Go to [cloudflare.com](https://dash.cloudflare.com/sign-up) and create an account.
3. **Deploy from Git**: 
   * Navigate to **Workers & Pages** -> **Create application** -> **Pages** -> **Connect to Git**.
   * Select your GitHub repository.
   * **Build Settings**: Leave everything blank/default (Framework preset: None, Build command: None, Output directory: leave blank or set to `/`).
   * Click **Save and Deploy**.
4. **Custom Domain**: Once deployed to the `.pages.dev` subdomain, go to the "Custom Domains" tab and follow the prompts to connect `iiskota.com`. Cloudflare will automatically provision a free SSL certificate.

## 2. How to Receive Enquiry Form Emails (Web3Forms)

The contact form is built using Web3Forms. To make it send emails to `indiraschoolkota@gmail.com`:
1. Go to [web3forms.com](https://web3forms.com/) and click "Create your Access Key".
2. Enter your email address (`indiraschoolkota@gmail.com`).
3. You will receive an **Access Key** in your email.
4. Open `index.html` in a text editor (like Notepad or VS Code).
5. Find this line (around line 140):
   ```html
   <input type="hidden" name="access_key" value="YOUR_ACCESS_KEY_HERE">
   ```
6. Replace `YOUR_ACCESS_KEY_HERE` with your actual key.
7. Save the file and upload/push the change. Form submissions will now arrive directly in your inbox.

## 3. How to Edit Content (For School Staff)

You do not need technical knowledge to update basic text or images.

### To edit text on the website (e.g., Principal's Message or Announcements)
1. Open `index.html` in any text editor.
2. Press `Ctrl+F` (or `Cmd+F` on Mac) to find the text you want to change.
   * *Example: Search for "Welcome to Indira International School".*
3. Carefully type your new text between the HTML tags (like `<p>` and `</p>`). **Do not delete the tags themselves.**
4. Save the file.
5. Upload the updated `index.html` file to your hosting provider or push it to GitHub (Cloudflare will auto-deploy the changes in seconds).

### To replace an image (e.g., replacing a placeholder with a real photo)
1. Name your new photo something simple without spaces (e.g., `real-campus.jpg`).
2. Place the new photo in the `/src/assets/` folder.
3. Open `index.html`, find the old image name (e.g., `school_building_hero_1790596964717.jpg`), and replace it with your new file name (`real-campus.jpg`).
4. Save and upload.

*Note: For the best performance, try to compress your real photos using a free site like [tinypng.com](https://tinypng.com/) before uploading them.*
