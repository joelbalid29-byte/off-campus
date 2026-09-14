# OffCampus Dubai — Vercel deploy

This folder is a ready-to-deploy static site. It's just one self-contained
`index.html` (logo and styles are embedded, no build step, no dependencies).

## Deploy in the Vercel dashboard (no terminal needed)

1. Go to vercel.com and sign in (or create a free account).
2. Click **Add New → Project**.
3. Choose **Deploy without Git** / drag-and-drop, and drop this whole folder
   (`index.html` + `vercel.json`) onto the upload area.
4. Click **Deploy**. Vercel gives you a live `*.vercel.app` URL immediately.
5. Once you've bought your domain: open the project → **Settings → Domains**
   → add `offcampusdubai.com` (or whatever you buy) and follow Vercel's DNS
   instructions (usually just an A/CNAME record at your registrar).

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
3. Framework preset: **Other** (it's static HTML, no build command needed).
4. Deploy. Every future push to the repo auto-deploys.

No environment variables, build command, or output directory settings are
needed — Vercel serves `index.html` as-is.
