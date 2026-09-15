# AP Psychology 2026-27: card banks

Vocabulary card banks served at
<https://bethanychamberlain.github.io/ap-psych-study-guides/>.

**One page per teaching week, plus a unit archive.** The index opens on the week the course
is actually in, computed in the page from the year plan's dates, and the numbering matches
the Week 01, 02, 03 modules in the Learning Lab. The six unit pages are kept at their
original URLs as a revision view, which is the shape AP Classroom and the exam use.

The weekly split exists because the course is a two-pass spiral: the fast pass covers the
whole syllabus in thirteen sessions and the deep pass covers it again. Unit and week are
therefore unrelated axes, and week 02 alone spans two units, so "the unit we are in" was a
question with no answer. Students said so.

Each page shows a term and asks the student to write the definition **in their own words**
before the course's wording is revealed. Writing the card is where the learning is, so a
ready-made deck would defeat the point.

**A card follows the student across every page.** One store keyed by term, so a term met in
week 02 and again in week 09 is one card that gets sharpened, not two that get written.

## What leaves the browser

Cards are stored in the student's own browser. When a student presses **Save my work**, the
cards they have written are posted to the teacher's own Google Sheet together with the code
they were issued, and nothing else: no name is in the page, none is on the wire, and the code
maps to a name only inside the Sheet. Nothing is ever sent on its own.

Every page is plain HTML with **no external requests**: no webfonts, no CDN, no analytics.
The build refuses to write a page that makes one.

## Do not add the syllabus here

This repository is public. The course syllabus PDF embeds the live Zoom meeting link, the
AP Classroom join code and a staff email address, so it stays on the Learning Lab and must
never be committed here. The same goes for anything with student writing in it, and for
AP Classroom question content, which College Board's terms do not allow to be redistributed.

## Regenerating

Built from the course content plan in the private `hs-teach` repository:

    python3 scripts/build-card-bank-site.py --out /path/to/this/checkout \
      --sync-from /path/to/this/checkout/card-bank-unit1.html

**`--sync-from` is not optional for what ships here.** Without it the pages are built with no
code gate and no Save button, and nothing in the output says so except the privacy wording.
It reads the endpoint and key out of a page already in this checkout, so neither is ever
retyped.

The build reads each bank's title out of the generated file rather than repeating it, so the
index cannot drift from the banks it lists, and it refuses to write if the weekly pages and
the schedule disagree about how many terms the year holds.

Cards and materials by Bethany Chamberlain.
