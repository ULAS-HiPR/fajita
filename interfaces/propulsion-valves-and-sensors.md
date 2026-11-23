\# Propulsion valves and sensors



One row per valve, igniter and sensor on the propulsion system, and whether

Fajita drives or reads it. Blanks and question marks are questions for

propulsion (James). Nothing here is decided; see \[decisions.md](../decisions.md).



Updated 23 November 2026 with James's answers to Serafina's questions. James

expects more information on Thursday 26 November.



Scope, from James in the Fajita Discord post on 23 November (Seán agreed):

Fajita sits by the two main valves; it actuates both main valves, fires the

igniter's e-matches, reads pressure transducers and runs the abort procedures.

There are three tanks (fuel, oxidiser, nitrogen), each with a vent valve, and

two e-regs, each on its own board in the plumbing between the tanks.



\## Valves and igniter



Seven valves on the vehicle for now (James, 23 Nov): two main propellant

valves, three vents and two e-reg valves.



Servo model not chosen. James: treat every servo as a regular servo of about

35 kg torque for now (inferred: 35 kg·cm, the usual hobby-servo rating). Its

current is unknown until we read a datasheet for a representative servo; the

power board needs it.



| Item | What it does | Fajita's? | What moves it | Where | Current | Unpowered state | Source |

| --- | --- | --- | --- | --- | --- | --- | --- |

| Main fuel valve | Lets fuel into the engine | Yes | Servo, \~35 kg, model not chosen. No angle sensor (Jay, 20 Nov); James now unsure about angle sensors | By the engine, beside Fajita | ? (need a datasheet) | Holds position (servo). Acceptable? | James, 23 Nov; Jay, 20 Nov |

| Main oxidiser valve | Lets nitrous into the engine | Yes | Servo, \~35 kg, model not chosen. Angle sensor: James unsure | By the engine, beside Fajita | ? (need a datasheet) | Holds position (servo). Acceptable? | James, 23 Nov |

| Vent, fuel tank | Releases the tank's pressure, including after an abort | ? Not answered 23 Nov (O-8) | Servo, \~35 kg, model not chosen | Fuel tank | ? (need a datasheet) | Must open without power (LV-0190); a plain servo holds position, so this needs a spring return, a normally open solenoid or a relief valve | James, 23 Nov |

| Vent, oxidiser tank | As above | ? Not answered 23 Nov (O-8) | As above | Oxidiser tank | ? | As above | James, 23 Nov |

| Vent, nitrogen tank | As above | ? Not answered 23 Nov (O-8) | As above | Nitrogen tank | ? | As above | James, 23 Nov |

| e-reg valve 1 | Meters nitrogen into a propellant tank to hold its pressure (inferred) | No: e-reg board 1 | Servo (D-21Nov.10)? | Plumbing between tanks | Not on Fajita's power budget unless Fajita powers the e-reg boards (?) | ? | James, 23 Nov; D-21Nov.10 |

| e-reg valve 2 | As above, for the other propellant tank (inferred) | No: e-reg board 2 | Servo? | Plumbing between tanks | As above | ? | James, 23 Nov |

| Igniter e-match A | Lights the igniter, which lights the engine | Yes | Fajita firing channel: arm switch, high side, low side, continuity check | Engine | All-fire / no-fire? E-match model not chosen | Not firing | James, 23 Nov; LV-0030 |

| Igniter e-match B (redundant) | As above, if A fails | Yes | Its own channel, or shared with A? (open) | Engine | As above | Not firing | James, 23 Nov |

| Fill valves | Load propellant and nitrogen | Not among the seven vehicle valves, so probably ground-side (inferred). Confirm | | | | | Not mentioned; LV-0110, 0130, 0150 |



James calls it "a normal e-match", which suggests a pyrotechnic igniter

rather than a torch with its own valves (inferred). Confirm, since the table

also lists an igniter PT.



\## Sensors



About eight pressure transducers (PTs) on the vehicle. Fajita should read

four of them directly (James, 23 Nov); which four is open.



| Item | Measures | Fajita reads it? | Where | Output type | Source |

| --- | --- | --- | --- | --- | --- |

| PT, engine | Chamber pressure | One of the four? (close to Fajita) | Engine | ? | James, 23 Nov |

| PT, igniter | Igniter pressure (why, if the igniter is pyrotechnic?) | One of the four? (close to Fajita) | Igniter | ? | James, 23 Nov |

| PT, fuel tank | Tank pressure | One of the four? | Fuel tank | ? | James, 23 Nov |

| PT, oxidiser tank | Tank pressure | One of the four? | Oxidiser tank | ? | James, 23 Nov |

| PT, nitrogen tank | Tank pressure | One of the four? | Nitrogen tank | ? | James, 23 Nov |

| PT, e-reg 1 | Regulated pressure (inferred) | One of the four, or a cross-check over the e-reg link (D-21Nov.10)? | e-reg 1 | ? | James, 23 Nov |

| PT, e-reg 2 | Regulated pressure (inferred) | As above | e-reg 2 | ? | James, 23 Nov |

| PT, spare | ? | ? | ? | ? | James, 23 Nov |

| Thermocouples (TCs) | Temperature | ? Needed, not specced yet (James) | ? | Thermocouple | James, 23 Nov |

| Angle sensors | Valve position | ? James not sure they're wanted | On the servo valves except main fuel (Jay, 20 Nov) | ? | James, 23 Nov; Jay, 20 Nov |



\## Count check



Resolved 23 November: seven valves on the vehicle for now (two main, three

vents, two e-regs). The Notion brief's "about nine servo valves, three per

bank" is out of date.



\## Still to ask propulsion (26 November)



1\. Which vents does Fajita drive, and which tank is at the bottom?

2\. Which four PTs does Fajita read?

3\. How many TCs, where, and does Fajita read them?

4\. Angle sensors on the valves: yes or no, and on which?

5\. Servo model, or at least a representative one, for its stall current.

6\. E-match model, for its all-fire and no-fire current.

7\. Are the fill valves on the ground?

8\. Is the igniter pyrotechnic, and if so, what is the igniter PT for?



