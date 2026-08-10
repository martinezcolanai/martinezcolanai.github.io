# How to update this site

You don't need to install anything to make these changes — you can do all of
this directly on github.com in your browser.

## Add a new publication

1. Go to the `_publications` folder in the repository on GitHub.
2. Click **Add file → Create new file**.
3. Name it something like `2027-my-paper-title.md`.
4. Paste this template and fill it in (delete the placeholder files once you
   have real entries):

   ```
   ---
   title: "Full title of the paper"
   authors: "A. I. Martínez Colán, E. Chatzi, R. Steenbergen"
   venue: "Journal or conference name, volume(issue), pages"
   year: 2027
   type: "journal"        # journal | conference | preprint
   status: "published"    # in preparation | under review | published | planned
   doi: "10.xxxx/xxxxx"   # leave blank quotes "" if none yet
   pdf: "https://..."     # leave blank quotes "" if none yet
   abstract: "One or two sentence summary of the paper."
   ---
   ```

5. Commit the change. The site rebuilds automatically within a minute or two.

## Edit the Home page text

Open `index.html` at the root of the repository and edit the text inside the
`<section>` blocks directly. Each section is labelled with a
`<p class="eyebrow">` marker (e.g. "Current research") so you can find the
right block.

## Replace the portrait placeholder

Upload your photo to `assets/img/` (e.g. `portrait.jpg`, ideally around
800×1000 px, portrait orientation), then change the image path in the bio
section of `index.html` from `portrait-placeholder.svg` to your file name.
The photo is displayed in grayscale automatically; remove the
`filter: grayscale(100%)` line in `assets/css/main.css` if you want colour.

## Change the published email

The email shown in the sidebar is set once in `_config.yml` under
`author: email:`.
