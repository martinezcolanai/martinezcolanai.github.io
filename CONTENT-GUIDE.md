# How to update this site

You don't need to install anything to make these changes — you can do all of
this directly on github.com in your browser.

## Add a new publication

1. Go to the `_publications` folder in the repository on GitHub.
2. Click **Add file → Create new file**.
3. Name it something like `2027-my-paper-title.md`.
4. Paste this template and fill it in:

   ```
   ---
   title: "Full title of the paper"
   authors: "Andrés Martínez, Co Author"
   venue: "Journal or conference name, volume, pages, place, dates"
   year: 2027
   order: 80              # see "Ordering" below
   type: "journal"        # see "Where an entry appears" below
   status: "published"    # published | under review | in preparation | presented
   doi: "10.xxxx/xxxxx"   # leave as "" if none
   pdf: "https://..."     # leave as "" if none
   abstract: ""           # optional; shown on the entry's own page
   ---
   ```

5. Commit the change. The site rebuilds automatically within a minute or two.

### Where an entry appears

The `type` field alone decides which part of the page an entry lands in:

| `type`         | Appears under                            |
| -------------- | ---------------------------------------- |
| `journal`      | Publications → Journal articles           |
| `conference`   | Publications → Conference proceedings     |
| `presentation` | Talks                                     |

Spell it exactly as above. Anything else lands in a catch-all group labelled
**Other** at the bottom of Publications — that group exists purely so a typo
is visible rather than making the entry disappear. If you ever see "Other" on
the site, an entry has a misspelled `type`.

### Status

The status is only printed when the work is not out yet. `published` and
`presented` are treated as the normal case and are left unwritten, so a
finished entry just shows its year. Use `under review` or `in preparation`
and that label appears next to the year.

### Ordering

Within each group, entries are sorted by the `order` number, **highest
first**. Years alone are not enough, because several entries share a year and
Jekyll gives no guaranteed order between ties.

Existing entries use 70, 60, 50, 40, 30, 20, 10 on a single scale shared by
all three groups — you do not need to restart the numbering per group, since
only the entries within a group are ever compared. To put a new paper at the
top of its group, give it a number higher than everything above it (e.g. 80).
To slot one in between, pick a number in between (e.g. 45 sits between 40 and
50) — the gaps of ten exist so you rarely have to renumber anything.

### Optional fields

`doi`, `pdf` and `abstract` can be left empty (`""`) or removed entirely —
either way nothing is shown for them. A DOI or PDF link only appears when you
actually give it a value.

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
