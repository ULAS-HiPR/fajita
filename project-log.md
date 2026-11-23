# Project Log

Append-only; oldest to newest. Add a dated correction instead of rewriting an
earlier entry. Spelling and broken links may be corrected in place.

[`current-system.md`](current-system.md) is the canonical snapshot. This log
preserves how it changes.

## 22 November 2026: repository created

* Seán made this repository in ULAS-HiPR and asked for it to be set up the way
Ogma2 is arranged.
* Seeded from the [Notion brief](https://app.notion.com/p/3e3cc5f72fe281c1959de7809c5ae47d) and Ogma2's decisions as of 22 Nov: purpose,
what it must demonstrate, interfaces, external rules, the parts one person
can own, and the open questions (as Open rows in `decisions.md`).
* Owner: Serafina. Helpers: Rory, Arnav.
* Discussion lives in the Fajita post in Discord's avionics-projects forum.

## 22 November 2026: EuRoC meeting date corrected

* The seed copied "25 Nov" for the EuRoC meeting from the Notion brief. Jay,
in #avionics on 20 Nov, answering whether the avionics meeting would run at
18:00 Thursday next week: "No, we'll be doing the EuRoac meeting then". So
it's Thursday 26 November, 6pm; place not stated. Fixed here and in Notion.

## 22 November 2026: brought in line with Ogma2's later decisions

* Seán asked for every avionics brief to match the latest decisions. Checked
the Notion brief and this repository against Ogma2's decisions up to
D-22Nov.30 and fixed what had gone stale: USB-C stays at the av-bay, not the
panel (D-21Nov.4); the arm-switch headers (D-21Nov.12); the umbilical's
Churro end, J801 (D-22Nov.6); the PROP and ACT branches retry after a fault
and limit at 19.4 A minimum (D-22Nov.4), whichever of these applies here.

## 23 November 2026: valve and sensor table started

* Seán asked for one row per valve and sensor Fajita drives or reads. Started
`propulsion-valves-and-sensors.md` from what the repo already says; blanks are questions for propulsion on 26 Nov.

## 23 November 2026: Fajita's scope from propulsion

* James, in the Fajita Discord post (Seán agreed): Fajita, which propulsion
calls the ECU, sits by the two main valves. It actuates both main valves,
fires the igniter's e-match, reads pressure transducers and runs the abort
procedures, plus the software states (abort, fill, launch and so on).
* Three tanks (fuel, oxidiser, nitrogen), each with a vent valve. James
suggested Fajita might drive the bottom tank's vent and the e-reg boards the
top two. That conflicts with Ogma2's D-21Nov.10 (Fajita can vent whatever
the e-reg does).
* Two e-regs, each on its own board in the plumbing between the tanks, where
D-21Nov.10 had one e-reg board. About eight PTs: engine, igniter, three
tanks, two e-regs and a spare.
* Updated the valve and sensor table.

## 23 November 2026: James's answers on valves, servos, PTs and the igniter

* Serafina asked James four questions; summary of his answers:

  * Seven valves on the vehicle for now: two main propellant valves, three
vents and two e-reg valves. That settles the count check; the Notion
brief's nine is out of date. Not answered: which vents Fajita drives and
which tank is at the bottom.
  * Servo model not chosen; size the power board for a regular servo of
about 35 kg torque for now. Its current still needs a datasheet.
  * Fajita reads four of the PTs directly; which four is open. Not sure about
angle sensors. Thermocouples will be needed but aren't specced yet.
  * The igniter uses a normal e-match plus one redundant: two e-matches.
Model not chosen, so all-fire and no-fire currents are unknown.
* Updated `interfaces/propulsion-valves-and-sensors.md`: the answers above,
a second e-match row, a list of what is still to ask on 26 Nov, and its
Markdown fixed so the headings and tables render.
* James expects more information on Thursday 26 November.

