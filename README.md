# Accessible Bin Calendar Generator

A free, single-page tool for creating printable bin collection calendars, including a large-print version for residents with visual impairments.

Staff enter a resident's address and their first collection date for each bin. The tool works out the rest of the year and produces:

- **A large print Word document** with one month per A4 page, large bold dates, each collection day filled in the bin's colour with the bin's name printed in the box, and a key on every page. It can be printed at A3 for residents who need even larger text.
- **A year planner Word document** with the whole year on one A4 page and collection days marked with coloured circles. Days with more than one bin show a split circle.
- **A calendar file (.ics)** that imports into Google Calendar, Outlook and Apple Calendar, with an optional reminder the day before.

Everything runs in the browser. No resident data is sent anywhere.

## Recent addresses and privacy

To save time on streets that come up again and again, the tool remembers the last 10 addresses you made a calendar for, along with their collection dates, extra collections and exceptions. Select one to fill the form back in.

- This is stored in the browser on that computer only (browser local storage). It is never sent to GitHub or anywhere else.
- Anyone using the same browser profile on that computer can see the list. On shared computers, consider switching it off.
- Entries are removed automatically after 90 days. You can remove one address, clear them all, or untick **Remember the last 10 addresses** to switch the feature off and delete what is stored.
- Organisations should check this fits their own data protection policies before use.

## Using it

Use it online at https://charliscurleyme.github.io/Accessible-Bin-Calendar/ or download `index.html` and open it in Chrome or Edge.

1. The first time, choose your settings: **Stirling Council** for Stirling's bins, or **Manual setup** for other councils and organisations. This is remembered, and afterwards shows as a single line you can change.
2. Enter the address and date range.
3. Enter the first collection date for each bin the resident has. Leave the others blank.
4. If a bin is collected on more than one day, select **Add another collection**.
5. Add any one-off exceptions, such as bank holiday changes.
6. Choose **Large print** or **Year planner**, and tick **Add a note to every page** if you need one (for example about festive collections). The tool prompts you when the dates cover Christmas.
7. Download the Word document, the calendar file, or both.

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

Adding `?preset=stirling` to the address opens the page with the Stirling Council settings, which is useful for a team bookmark. Any wording changes already made in that browser are kept.

## Accessibility choices

- Dates are printed in large bold Arial.
- Collection days are filled with a solid colour rather than relying on icons.
- Each bin's name is printed in the day box, so colour is never the only cue.
- Days with more than one collection use a distinct colour and list each bin.
- The year planner is a design-led alternative for general use. It is drawn as a high-resolution image, so it prints crisply but is not suited to screen readers; use the large print version where accessibility matters.
- The key only lists bins the resident actually has.

## Hosting on GitHub Pages

1. Put `index.html` at the root of the repository.
2. In the repository, go to **Settings > Pages**, choose **Deploy from a branch**, and select `main` and `/ (root)`.
3. To show a link to the source code in the page footer, set `REPO_URL` near the top of the main script in `index.html`.

## Licence

MIT licence. See [LICENSE](LICENSE).

The Word documents are built with the [docx](https://github.com/dolanmiu/docx) library, which is bundled into `index.html`. See [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).

Originally developed by Charlis Curley at Stirling Council, Waste Services.
