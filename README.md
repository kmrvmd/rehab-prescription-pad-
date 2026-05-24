[README.md](https://github.com/user-attachments/files/28188729/README.md)
# Rehab Prescription Pad

A private, single-file web app for generating Dr. Villanueva's Physical Therapy /
Rehabilitation Prescriptions as PDFs. Works on iPhone and Desktop. All data is
stored locally in the browser — nothing is sent to a server.

The whole app is one file: **`index.html`**. There is no build step.

## Deploy to Vercel (via GitHub)

1. **Create a GitHub repo.** Go to <https://github.com/new>, name it (e.g.
   `rehab-prescription-pad`), set it to **Private**, and create it.

2. **Add the files.** Upload `index.html` (and this `README.md`) to the repo —
   either with "Add file → Upload files" on github.com, or with git:

   ```bash
   git init
   git add index.html README.md
   git commit -m "Rehab Prescription Pad"
   git branch -M main
   git remote add origin https://github.com/<your-username>/rehab-prescription-pad.git
   git push -u origin main
   ```

3. **Connect Vercel.** Go to <https://vercel.com>, sign in with GitHub,
   click **Add New → Project**, and import the repo.

4. **Deploy.** No configuration is needed — Vercel serves `index.html` as a
   static site. Click **Deploy**. You'll get a URL like
   `https://rehab-prescription-pad.vercel.app`.

5. **Use it.** Open the URL on your iPhone and tap **Share → Add to Home Screen**
   so it opens like an app. Open the same URL on your Desktop too.

Every time you push a change to GitHub, Vercel redeploys automatically.

## Keeping it private

The Vercel URL is unguessable but technically public. For an extra layer, in the
Vercel project go to **Settings → Deployment Protection → Vercel Authentication**
and enable it — then only your logged-in Vercel account can open the app.

## Notes on your data

- Saved prescriptions, settings, and custom items live in the browser's local
  storage **on each device**. They are not synced between iPhone and Desktop.
- Use **Settings → Export backup** to save a `.json` file, and **Import backup**
  to load it on another device or after clearing your browser.
- Clearing browser data / site data will erase saved prescriptions — keep a
  backup file if that matters to you.
