# Fajita decisions

One row per decision, newest first. **Decided** rows override older text
anywhere in this repository. **Proposed** rows wait for the owner. **Open**
rows need an answer and someone to give it. **Replaced** rows are kept so old
references still resolve. Only Serafina moves a row to Decided.

IDs: `D-<day><month>.<n>`, as in Ogma2 (D-2Dec.1 is the first decision of
2 December).

Decisions about the core that bind Fajita live in [Ogma2's decisions](https://github.com/ULAS-HiPR/Ogma2/blob/main/decisions.md);
[current-system.md](current-system.md) lists them.

## Decided

| ID | Date | Decision | Why | Still to check |
| --- | --- | --- | --- | --- |

## Proposed

| ID | Date | Proposal | Why | Downside | Alternative | Smallest test |
| --- | --- | --- | --- | --- | --- | --- |

## Open

| ID | Question | Who answers | Note |
| --- | --- | --- | --- |
| O-1 | Propulsion's requirements | James / propulsion | Due at the EuRoC meeting, Thu 26 Nov, 6pm |
| O-2 | Each valve's unpowered state, and what opens the vent if PROP or Fajita dies | Serafina with propulsion |  |
| O-3 | What Fajita does if Burrito, CAN or the operator link drops mid-fill | Serafina |  |
| O-4 | Whether the vent command after an abort travels on Fajita's own link or on Burrito's radio over bus 1 | Serafina with Seán |  |
| O-5 | PROP eFuse fault mode: latch-off or retry (open in Ogma2 as 'Fajita owner') | Serafina |  |
| O-6 | Integration date | James |  |
| O-7 | The chamber, assumed for 4 January | Propulsion |  |

## Replaced

| ID | Was | Replaced by |
| --- | --- | --- |
