# Fajita current system

Updated 22 November 2026. Decisions live in [decisions.md](decisions.md); this file states
what is true now. Nothing is designed, built or flown yet.

Owner: Serafina. Helpers: Rory, Arnav. Next milestone: Propulsion's requirements at the EuRoC meeting (25 Nov); requirements captured by 14 Dec.

Seeded from the [Notion brief](https://app.notion.com/p/3e3cc5f72fe281c1959de7809c5ae47d) and from Ogma2's decisions as they stood on
22 November. Where they disagree, Ogma2's decisions win, and the difference is
listed below.

## Purpose

Run the engine's valves and sensors from fill to burnout, and leave the vehicle safe after an abort. Fajita is ours; propulsion sets its requirements, and it governs itself ([D-20Nov.2](https://github.com/ULAS-HiPR/Ogma2/blob/main/decisions.md)).

## Must demonstrate

- Valve actuation and sensor readings on the bench with the real valves.
- Safe behaviour when bus 1 or Burrito drops out.
- A remotely controlled vent or offload after an abort (LV-0190).
- Six hours on the rail from the PROP pack.

## Interfaces

Set by Ogma2's decisions unless marked proposed. Changing one needs the other
owner's agreement and a row in both repositories.

| With | What | Ogma2 decision |
| --- | --- | --- |
| Burrito | CAN bus 1: Harwin Gecko 3-way to Burrito's J501 (Fajita's end has to match), 500 kbit/s Classical CAN, two nodes, fixed termination. Carries permissions, mode, slow state and health; no sensor streams, nothing unsafe when stale. | [D-18Nov.4](https://github.com/ULAS-HiPR/Ogma2/blob/main/decisions.md), [D-2Nov.9](https://github.com/ULAS-HiPR/Ogma2/blob/main/decisions.md) |
| Churro | Power from Churro's 6S PROP branch, through an eFuse. Churro keeps PROP powered through an abort so Fajita can vent. Fajita converts to its actuators' voltages itself. | [D-21Nov.1](https://github.com/ULAS-HiPR/Ogma2/blob/main/decisions.md) |
| e-reg | The e-reg is its own board on its own CAN link to Fajita, never on bus 1. Fajita keeps the main valves and overpressure protection, with its own pressure transducers or a cross-check of the e-reg's, so it can vent whatever the e-reg does. | [D-21Nov.10](https://github.com/ULAS-HiPR/Ogma2/blob/main/decisions.md) |
| Access panel | One USB-C at the panel for integration; no firmware over CAN, nothing flashed on the rail. | [D-19Nov.9](https://github.com/ULAS-HiPR/Ogma2/blob/main/decisions.md), [D-21Nov.4](https://github.com/ULAS-HiPR/Ogma2/blob/main/decisions.md) |

## Also known

- About nine servo valves, three per bank, with angle sensors on all but the main fuel valves; no propulsion solenoids (Jay, 20 Nov, per the Notion brief).
- A servo stays where it is when it loses power, so the vent must open without power: a spring-return actuator, a normally-open solenoid on the vent only, or a relief valve set below the tank's limit. Every other valve's unpowered state is written down and accepted in review (ECU-06, LV-0190).

## External rules

LV-0190 (remote vent or offload after an abort); LV-0030 (igniter armed and disarmed with nobody within 15 m); LV-0110, 0130, 0150 (loading); LV-1020 (hold-down); Appendix E1 (valve power disconnect); LV-0300–0320 (the PROP pack: no LiPo, charged through the umbilical, 6 h); SE-0010–0030 (launch control, propulsion's).

## Parts one person can own

1. Valve servo drivers, angle sensing and the E1 power disconnect
2. Sensor front ends: pressure and temperature
3. The sequence and the links: fill, fire and abort logic with propulsion; bus 1 to Burrito; the vent path after an abort
4. Power and harness: the PROP feed, regulation, connectors, PTFE wire near the nitrous

## Timeline

| Milestone | Date |
| --- | --- |
| Requirements captured | 14 December 2026 |
| Schematics reviewed | 28 December 2026 |
| PCBs laid out and ordered | 11 January 2027 |
| Boards in hand | 1 February 2027 |
| Testing, firmware and integration | from 1 February 2027 |
| All electronics on one table | 3 weeks before the integrated vehicle |

From the [Electronics page](https://app.notion.com/p/3c8cc5f72fe28092aaf7dc3baacb4f67)'s avionics timeline.

## State

Repository created 22 November 2026. No requirements, schematic, layout or
firmware yet. Open questions are in [decisions.md](decisions.md#open).
