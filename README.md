# Accessible Bin Calendar Generator

A free, single-page tool for creating large-print, colour-coded bin collection calendars for residents with visual impairments.

Staff enter a resident's address and their first collection date for each bin. The tool works out the rest of the year and produces:

- **A Word document** with one month per A4 page, large bold dates, each collection day filled in the bin's colour, and a key on every page. It can be printed at A3 for residents who need even larger text.
- **A calendar file (.ics)** that imports into Google Calendar, Outlook and Apple Calendar, with an optional reminder the day before.

Everything runs in the browser. No resident data is sent anywhere or stored.

## Using it

Use it online at https://charliscurleyme.github.io/accessible-bin-calendar/ or download `index.html` and open it in Chrome or Edge.

1. Choose your settings at the top: **Stirling Council** for Stirling's bins, or **Manual setup** to create your own.
2. Enter the address and date range.
3. Enter the first collection date for each bin the resident has. Leave the others blank.
4. If a bin is collected on more than one day, select **Add another collection**.
5. Add any one-off exceptions, such as bank holiday changes.
6. Generate the Word document, the calendar file, or both.

## Setting it up for your council

Select **Manual setup**, then **Edit bins and wording**. For each bin you can change:

- the name shown on screen
- the colour (text is set to black or white automatically, whichever reads better, and the contrast ratio is shown)
- the label printed in each day's box
- the description in the key
- the calendar file event title
- the usual frequency and collection day

You can also set your organisation name, a footer for every page (for example a contact number), the key heading, the colour used for days with more than one bin, and the calendar reminder time.

Settings save automatically in your browser. To share a setup with colleagues, select **Save settings to a file** and send them the file. They can load it with **Load settings from a file**.

Adding `?preset=stirling` to the address always opens the page with the standard Stirling Council settings, which is useful for a bookmark.

## Accessibility choices

- Dates are printed in large bold Arial.
- Collection days are filled with a solid colour rather than relying on icons.
- Each bin's name is printed in the day box, so colour is never the only cue.
- Days with more than one collection use a distinct colour and list each bin.
- The key only lists bins the resident actually has.

## Hosting on GitHub Pages

1. Put `index.html` at the root of the repository.
2. In the repository, go to **Settings > Pages**, choose **Deploy from a branch**, and select `main` and `/ (root)`.
3. To show a link to the source code in the page footer, set `REPO_URL` near the top of the main script in `index.html`.

## Licence

MIT licence. See [LICENSE](LICENSE).

The Word documents are built with the [docx](https://github.com/dolanmiu/docx) library, which is bundled into `index.html`. See [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).

Originally developed by Charlis Curley at Stirling Council, Waste Services.
