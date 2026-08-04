# Gather Signal — Infographic Builder

A small web tool that builds on-brand Gather Signal infographics (bar, horizontal
bar, line, pie, donut, area, and a big-number stat callout) and downloads them as
PNGs sized for the monthly long-form article.

It runs entirely in the browser — no accounts, no server, nothing to install. All
of its parts (the Carbon charting library, the export library, and the Merriweather
font) are bundled in this folder, so it works even if outside services change.

## Using it each month
1. Open the tool's URL (see "Publishing" below).
2. Pick a chart type.
3. Enter your data (type rows, or paste a table from a spreadsheet and click "Fill rows from paste").
4. Add a title, optional subtitle, category label, and source line.
5. Optional: click the ◈ on one row to highlight that point in Signal Blue.
6. Click "Download PNG."

## Comparing two data sets (bar & line)
Tick "Compare a second data set" (shows for bar, horizontal bar, and line). A second
value field appears on each row, plus two name fields. You get two bars per category
(or two lines) — the first set in Progress Orange, the second in Signal Blue, with a
legend. The single-point highlight is off while comparing (colors are by data set then).

## More field options
- **Axis labels** (bar, horizontal bar, line, area): optional horizontal and vertical axis
  titles — e.g. "Quarter" on the horizontal axis and "Dollars" or "%" on the vertical.
- **Stat callout**: enter up to three data rows to show one, two, or three stats side by
  side in a row. Highlight one with the ◈ to make it Signal Blue.
- **Source line & links**: any web address you type (e.g. gathersignal.com/survey) shows in
  Progress Orange as a link. Note — a downloaded PNG is a flat image, so the link is not
  clickable inside the file itself; to make it truly clickable, place the link in your
  article around the image. Showing the URL as text (as it does) lets readers find it.

## One-time setup: add your wordmark
Drop your official wordmark PNG into the `assets/` folder, named exactly:

  assets/signal-wordmark-black.png

The tool stamps it in the lower-right of every export. Until it's there, exports
simply omit the wordmark (nothing breaks). Use your real PNG — don't recreate it.

## Publishing to GitHub Pages (turns this folder into a URL)
1. Create a new repository at github.com/hdavis-ship-it (e.g. "gather-signal-infographics"). Public.
2. Upload the CONTENTS of this folder (index.html, vendor/, fonts/, assets/) to the repo.
   (On github.com: "Add file" → "Upload files" → drag everything in → Commit.)
3. In the repo: Settings → Pages → "Build and deployment" → Source: "Deploy from a branch",
   Branch: main, folder: / (root) → Save.
4. Wait ~1 minute. GitHub shows the live URL (like https://hdavis-ship-it.github.io/gather-signal-infographics/).
   Bookmark it — that's your tool.

Tip: run exports from the published URL (not by double-clicking the local file); the
font embeds reliably over the web.

## Brand notes baked in
- Categorical colors use the Progress Orange tint ramp (Dark Orange → Progress Orange → tints).
- Signal Blue is reserved for one highlighted "signal" point only.
- Independent White background, Impact Black labels, Merriweather titles, Arial category labels.
- No gradients on data (per the Signal brand doc).
