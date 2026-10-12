# OffCampus Dubai — Vercel deploy

This folder is a ready-to-deploy static site: `index.html` (logo and styles
embedded, no build step) plus the site icon (favicon) files and `vercel.json`.

## Deploy in the Vercel dashboard (no terminal needed)

1. Go to vercel.com and sign in (or create a free account).
2. Click **Add New → Project**.
3. Choose **Deploy without Git** / drag-and-drop, and drop this whole folder
   onto the upload area (keep the favicon files next to `index.html`).
4. Click **Deploy**. Vercel gives you a live `*.vercel.app` URL immediately.
5. Once you've bought your domain: open the project → **Settings → Domains**
   → add `offcampusdubai.com` and follow Vercel's DNS instructions.

## Deploy with the Vercel CLI instead

```bash
npm i -g vercel
cd offcampus-vercel
vercel        # first deploy, follow the prompts
vercel --prod # promote to your production URL
```

## Deploy via GitHub (best for future edits)

1. Push this folder to a new GitHub repo.
2. In Vercel: **Add New → Project → Import Git Repository**, pick the repo.
3. Framework preset: **Other** (static HTML, no build command needed).
4. Deploy. Every future push to the repo auto-deploys.

## Site icon in Google results

`index.html` links to `favicon.ico`, `favicon-48x48.png`, `favicon-96x96.png`,
`favicon-192x192.png` and `apple-touch-icon.png`. After deploying, open
Google Search Console, inspect your homepage URL and click **Request indexing**.
Google usually shows the new icon within a few days to a couple of weeks.
