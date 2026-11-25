# APS Northwest Section: Meeting Archive

An archive of past APS Northwest Section annual meetings, for members, prospective attendees, and future organizers.

**Live site:** https://aps-northwest.github.io/meeting-archive/

The official page for the current meeting is on the [APS Northwest Section site](https://engage.aps.org/nws/meetings/annual). That page changes every year and updates slowly. This archive keeps what organizers published elsewhere, so it does not disappear.

## What is here

- `index.qmd`: the landing page. It has the section description, the Executive Committee roster, and the table of past and current meetings.
- `meetings/YYYY/`: one folder per meeting that has its own pages. Each has an `index.qmd` and, if needed, more pages and an `images/` folder. 2026 is the model: a meeting page rebuilt from the published website, plus the program guide.
- `_quarto.yml`: site settings and navigation.
- `.github/workflows/publish.yml`: renders the site with Quarto and publishes it to GitHub Pages every time `main` changes.

## Maintaining the site

The site rebuilds and publishes itself whenever a change reaches the `main` branch. Nobody needs Quarto to make a change.

**Small edits on github.com** (adding a link, fixing a typo): open the file, for example `index.qmd`, click the pencil icon, edit, and commit to `main`. The live site updates in a minute or two. The Actions tab shows progress. A red X there means the build failed, and the previous version of the site stays up. The error message names the problem, usually a typo in the table or a missing file.

**Larger changes** (a new meeting page with images): work on your computer. You need [Quarto](https://quarto.org) and Git.

```
git clone git@github.com:APS-Northwest/meeting-archive.git
cd meeting-archive
quarto preview       # live preview while you edit .qmd files
git add -A
git commit -m "Describe the change"
git push
```

Do not commit the rendered `_site/` folder. GitHub builds it.

Anyone who would rather not edit can send links or files to the current Chair, who will add them.

## Adding a meeting

1. Make `meetings/YYYY/index.qmd`. Start from `meetings/2026/index.qmd`.
2. In `index.qmd`, add the year's row to the table, or fill in the blank cells. The "APS archive" column links to the schedule and abstracts at `https://meetings-archive.aps.org/nws/YYYY/`. The "Meeting site" column links to the organizers' page in this archive, or to their original site if it is still live.
3. Add images, program guides, and other files under `meetings/YYYY/`. Convert the organizers' source (Markdown or Quarto) when it exists. Prefer that to a PDF or a link that may vanish.
4. Check the pages with `quarto preview`, then commit and push.

## What to leave out

This repository is public. Before publishing a meeting, remove:

- registration, abstract submission, and travel grant links, which expire
- discount codes and booking links
- WiFi and meeting passwords
- personal email addresses and phone numbers (venue and hotel names and addresses are fine)

Keep what the meeting published about itself: dates, location, schedule, speakers, travel and lodging information, student awards, and the organizing committee's names.

## Sources for older meetings

- The APS Meeting Archive covers most years: `https://meetings-archive.aps.org/nws/YYYY/`.
- The Internet Archive (web.archive.org) often has the organizers' own sites.
- The section's records of past meetings and locations are kept by the Secretary/Treasurer and the Chair.

## Status

Meetings with their own page here: 2026. APS archive links are in the table for 2008 to 2025. Local organizer sites for earlier years, and APS links for 2007 and before, still need to be found.
