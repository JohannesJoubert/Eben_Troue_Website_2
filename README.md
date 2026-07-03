# Eben & Anje — Troue Webwerf 🌿

Wedding website for Eben Spangenberg & Anje Millard — 11 December 2026, Rosemary Hill Farm, Pretoria.

A single static `index.html` — no build step, no dependencies. RSVPs are handled by **Netlify Forms**.

## Deploy: GitHub → Netlify

### 1. Push to GitHub
1. Create a new repository on GitHub (e.g. `eben-anje-troue`).
2. Upload `index.html` and this `README.md` (drag-and-drop on github.com works fine, or use git):
   ```bash
   git init
   git add .
   git commit -m "Wedding website"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/eben-anje-troue.git
   git push -u origin main
   ```

### 2. Connect to Netlify
1. Log in at [app.netlify.com](https://app.netlify.com) → **Add new site → Import an existing project**.
2. Choose **GitHub** and select your repository.
3. Leave the build settings empty (no build command, publish directory = root) and click **Deploy**.
4. Your site goes live at `something.netlify.app` — rename it under **Site configuration → Site details → Change site name** (e.g. `eben-en-anje.netlify.app`).

Every push to `main` will automatically redeploy the site.

### 3. Get RSVPs sent to your email (important!)
Netlify detects the RSVP form automatically on the first deploy. Submissions are collected under the **Forms** tab in your Netlify dashboard. To also receive each RSVP by email:

1. In Netlify: **Site configuration → Notifications → Form submission notifications** (on some plans: **Forms → Settings → Notifications**).
2. **Add notification → Email notification**.
3. Set the email to: `johjacjou@gmail.com`, form: `rsvp`, event: *New form submission*.

### 4. Test it
Submit a test RSVP on the live site and check that:
- It appears under **Forms → rsvp** in the Netlify dashboard.
- The notification email arrives at johjacjou@gmail.com.

> **Note:** The form only works on the deployed Netlify site — not when opening `index.html` directly from your computer, and not on GitHub Pages. Netlify's free tier includes 100 form submissions per month, which resets monthly — plenty for a wedding guest list, but if you expect more than 100 RSVPs in a single month, keep an eye on it.

## Still to fill in (placeholders)
Search `index.html` for `plekhouer` / `[` to find them:
- Story milestone dates and stories (met, first date, official, engagement)
- Photos — replace the dashed placeholder blocks with `<img>` tags
- Dress code, RSVP deadline, and final day programme
