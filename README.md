# Store Capsules

A blush-themed store directory: capsules, stores, owners, camera apps, employee allowances and recent updates. It is a static site (no build step, no server).

## Put it online (GitHub Pages)

1. Create a new repository on GitHub.
2. Upload everything in this folder (`index.html`, `data.json`, `.nojekyll`, `README.md`) to the repository root.
3. Go to **Settings > Pages**, set **Source** to *Deploy from a branch*, choose `main` and `/ (root)`, then **Save**.
4. After a minute your site is live at `https://<your-username>.github.io/<repo-name>/`.

## Manager editing

- Everyone can view. To edit, tap **Manager login** and enter the password.
- The starting password is `Manager@2026`. Change it before sharing the link:
  1. Open the site, press F12, open the Console and run:
     `crypto.subtle.digest('SHA-256',new TextEncoder().encode('YOUR NEW PASSWORD')).then(b=>console.log([...new Uint8Array(b)].map(x=>x.toString(16).padStart(2,'0')).join('')))`
  2. Copy the long text it prints.
  3. In `index.html`, find `const PWH='` and replace the text inside the quotes with it.
- In edit mode you can add, rename and delete capsules, stores and updates, edit allowances, and change the site name, colours, text and logo (**Customize**, **Upload logo**).

## Making your edits visible to everyone

Edits are saved in the manager's own browser first. To publish them:

1. In edit mode tap **Export data.json**.
2. In your repository, upload that file over the existing `data.json` (Add file > Upload files, commit).
3. Everyone sees the new data after the page refreshes (GitHub can take a minute).

## Good to know

- The password check runs in the browser, so it keeps casual visitors out but is not real security. Anyone can read `index.html` and `data.json`.
- GitHub Pages sites are public. The directory contains owner names, addresses and phone numbers, so only publish it if that is acceptable, or host it somewhere with a login.
