# Hohyeon Lee — portfolio site

A static site: `index.html` plus the `img/` and `video/` folders. No build step, no server.

## 1. Put it on GitHub

1. Sign in at github.com and click **New repository**. Name it (for example `portfolio`), keep it **Public**, do not add a README, and create it.
2. On the empty repo page click **uploading an existing file**, drag in everything from this folder (`index.html`, `404.html`, `.nojekyll`, `README.md`, the `img` and `video` folders), and press **Commit changes**.
   The video is about 7 MB and the largest image about 1 MB, so everything is under GitHub's limits.

## 2. Turn on GitHub Pages

1. In the repo go to **Settings → Pages**.
2. Under **Build and deployment** choose **Deploy from a branch**, branch `main`, folder `/ (root)`, and save.
3. After a minute or two the page shows a link like `https://YOURNAME.github.io/portfolio/`. Open it: the site should be live.

## 3. Attach your own domain

1. Buy a domain from any registrar (Cloudflare, Namecheap, Squarespace Domains, Gabia, Hosting.kr…).
2. In the registrar's DNS settings add these records (replace `YOURNAME` with your GitHub username):

   | Type  | Name | Value                      |
   |-------|------|----------------------------|
   | A     | @    | 185.199.108.153            |
   | A     | @    | 185.199.109.153            |
   | A     | @    | 185.199.110.153            |
   | A     | @    | 185.199.111.153            |
   | CNAME | www  | YOURNAME.github.io         |

3. Back in **Settings → Pages → Custom domain**, type your domain (for example `hohyeonlee.com`), save, and tick **Enforce HTTPS** once the check passes (DNS can take from a few minutes to a day to propagate).
4. GitHub writes a `CNAME` file into the repo for you; `CNAME.example` here only shows what it will contain and can be deleted.

## Updating the site later

Replace the files in the repo (drag-and-drop upload again, or ask Claude for a new deploy folder). Pages republishes automatically within a minute.

## Adding or changing work

All work data lives in one place in `index.html`: the `WORKS` array near the top of the script, in display order. Each entry has the title, year, kind (`painting` or `sculpture`), media, dimensions, image base name, optional extra `views`, optional `video`, alt text and the description paragraphs. Images follow the naming `img/<name>.jpg` (large, ~2200 px), `img/<name>-m.jpg` (~1100 px) and `img/<name>-s.jpg` (~480 px). The per-page colour atmosphere is in the `SCENES` object just below the forest code.
