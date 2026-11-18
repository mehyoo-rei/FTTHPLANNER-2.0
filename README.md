# FTTH Local Planner

A map-based tool for planning FTTH networks: place OLTs, poles, FBT splitters,
cassettes, NAP boxes and customer drops, draw cable routes between them, and
get a live fiber optical budget (dBm) for every NAP — plus a topology tree
view. Runs entirely in the browser; no server or account needed.

## Try it right now

Just open `index.html` in a browser (double-click it, or drag it into a
browser tab). Everything works offline except the map tiles themselves,
which need an internet connection to load street maps.

## Get it on the web / as an "app" (GitHub Pages) — no coding required

1. **Create a GitHub account** at [github.com](https://github.com) if you
   don't have one already.
2. Click the **+** icon top-right → **New repository**. Name it something
   like `ftth-planner`, leave it **Public**, and click **Create repository**.
3. On the new repo page, click **Add file → Upload files**.
4. Drag in all the files from this folder (`index.html`, `manifest.json`,
   `sw.js`, `icon-192.png`, `icon-512.png`, `README.md`), then click
   **Commit changes**.
5. Go to the repo's **Settings** tab → **Pages** (left sidebar).
6. Under **Build and deployment → Source**, choose **Deploy from a branch**.
   Under **Branch**, choose `main` and folder `/ (root)`, then **Save**.
7. Wait about a minute, then refresh the Pages settings page — it'll show
   your live URL, something like:

   `https://<your-github-username>.github.io/ftth-planner/`

That URL is now your planner, live on the web, shareable with anyone.

## Install it like an app on your phone

Once it's live on that URL:

- **Android (Chrome):** open the URL → tap the **⋮** menu → **Add to Home
  screen** (or you may see an **Install app** banner). It'll get its own
  icon and open full-screen, like a real app.
- **iPhone (Safari):** open the URL → tap the **Share** icon → **Add to
  Home Screen**.

This works because the project includes a `manifest.json` (app name, icon,
colors) and a small `sw.js` service worker, which is what makes browsers
offer the "install" option.

## Updating it later

Whenever you want to change something (new feature, fix, etc.), just come
back to this chat, ask for the change, and re-upload the updated
`index.html` to the same GitHub repo — click into the file on GitHub, click
the pencil (**Edit**) icon, delete everything, paste the new content, and
commit. GitHub Pages will redeploy automatically within a minute or two.

If you'd rather work with `git` on a computer instead of the web upload
flow, that works the same as any normal repo — clone it, edit, `git add`,
`git commit`, `git push`.

## Data storage

Your network layout autosaves to your browser's local storage on whichever
device you're using — it isn't synced between devices and isn't uploaded
anywhere. Use the **Export CSV** button regularly to keep a backup of your
NAP list, or use **Save** and note that reloading the exact same browser on
the exact same device will bring your layout back.

## What's inside

| File            | Purpose                                          |
|-----------------|---------------------------------------------------|
| `index.html`    | The entire app — map, topology view, all logic    |
| `manifest.json` | Makes the app installable (name, icon, colors)    |
| `sw.js`         | Lets the app shell open even with a weak signal   |
| `icon-192.png`, `icon-512.png` | App icons                        |
