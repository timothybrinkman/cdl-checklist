# cdl-checklist

Mobile-first Class A CDL practice app for the vehicle inspection, the air brake check, and the basic control skills test. It's one self-contained page you can use while standing next to the truck.

**Live:** https://timothybrinkman.github.io/cdl-checklist/

## What's in it

| Tab | Content |
|---|---|
| Inspection | The modernized Class A vehicle inspection checklist, in test order, with what to say for each item |
| Air Brake | The four-part air brake check (gauge & governor cut-out → leakage rate → low-air warning → emergency brake activation) |
| Skills & Road | The four basic control exercises, how they're scored, road-test automatic failures, and older maneuvers kept for practice only |
| Daily Extras | Good daily checks that are **not** on the test checklist |
| Review | Missed items, exam-sim history, and buttons to clear data |

Practice modes (switch at the top):

- **Guided**: the item and its explanation, tap to check off
- **Memory**: the item name only; say it out loud, reveal the answer, then grade yourself
- **Exam sim**: the test order with explanations hidden until you finish; misses are saved to Review. This is an unofficial simulation, not DMV scoring.

All data stays in your browser (`localStorage`). There are no accounts, frameworks, or build step.

## Offline

`sw.js` caches the app after the first visit, so it opens with no signal. App files are fetched network-first, so whenever you have signal you get the latest content; the cached copy is used only when the network fails.

## Sources

- [Nebraska CDL Driver's Manual, March 2026 (PDF)](https://dmv.nebraska.gov/sites/default/files/doc/Nebraska%20MOD%20CDL%20Driver's%20Manual%20-%20March%202026.pdf). This is the authority; if the app and the manual disagree, the manual wins.
- The exam checklist, air brake steps, and skills exercises follow the AAMVA modernized test text (Sections 11–12), which the Nebraska manual is based on.

## Files

`index.html` (the app), `sw.js` (offline cache), `manifest.webmanifest` + `icon*.{svg,png}` (Add to Home Screen).
