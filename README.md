# Dog Guard Referral Partner Kit

The dealer drop-off kit for referral partners (realtors, HOA managers, developers, veterinarians, groomers and daycares). It is one web page: a dealer fills in their details on the left, every piece updates, and each piece prints on its own.

Live copy: https://dogguard-referral-kit.netlify.app (access code: LocalPro)

## What is in this folder

- `index.html` is the whole kit: layout, copy, styles and the print logic, all in one file. Edit this to change wording, colors or layout.
- `photos/` holds the seven photos the pieces use (porch, yard, driveway, flags, consult, consult2, lawn). To swap a photo, replace the file and keep the same name; nothing else needs to change. Keep them under about 400 KB each so the page stays quick.
- `logo.png` is the Dog Guard logo, white on navy, used as-is.

## Where things are in index.html

- The file is divided by banner comments: `CORE`, `REALTOR`, `HOA / COMMUNITY`, `DEVELOPER / BUILDER`, `VETERINARIAN`, `GROOMER / DAYCARE`, `PLAYBOOK`, `NOTES`. Inside each, every printable piece is a `<div class="piece">` with its heading, size and copy in plain HTML right below it (for example "Leave-behind card", "How It Works one-pager", "Partner referral card").
- The access code is near the top of the script: `var ACCESS_CODE = "LocalPro";`
- Brand colors are set once in the CSS variables at the top of the `<style>` block (navy `#002F6C`, gold `#FFC72C`).
- Photo slots are `<img data-photo="PORCH">` style tags; the name maps to the file in `photos/` through the `DG_PHOTOS` list near the top of the script.

## Editing on GitHub

Open the file on GitHub, click the pencil icon, make the change, and click "Commit changes". Every save is kept, so anything can be rolled back from the History view. Once the Netlify site is connected to this repository, each save publishes to the live address within a minute or so.

To preview a change before saving, download `index.html` together with the `photos/` folder and `logo.png` into one folder and open `index.html` in a browser; the page runs entirely in the browser, with no server needed.

## Status

Draft for review. Copy is a first pass; graphics and layout are open for revision. Print-ready PDF or Word versions come after the copy is approved.
