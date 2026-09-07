# AP Psychology 2026-27 — card banks

Six vocabulary card banks, one per unit plus the science practices, served at
<https://bethanychamberlain.github.io/ap-psych-study-guides/>.

Each page shows a term and asks the student to write the definition **in their own words**
before the course's wording is revealed. Writing the card is where the learning is, so a
ready-made deck would defeat the point. Cards are stored in the student's own browser: no
accounts, no server, nothing leaves the device except the export they hand in.

Every page is plain HTML with **no external requests** — no webfonts, no CDN, no analytics.

## Do not add the syllabus here

This repository is public. The course syllabus PDF embeds the live Zoom meeting link, the
AP Classroom join code and a staff email address, so it stays on the Learning Lab and must
never be committed here. The same goes for anything with student writing in it, and for
AP Classroom question content, which College Board's terms do not allow to be redistributed.

## Regenerating

Built from the course content plan in the private `hs-teach` repository:

    python3 scripts/build-card-bank-site.py --out /path/to/this/checkout

The build refuses to write a page that makes an external request, and reads each bank's
title out of the generated file rather than repeating it, so the index cannot drift from
the banks it lists.

Cards and materials by Bethany Chamberlain.
