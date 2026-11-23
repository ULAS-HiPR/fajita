\# Propulsion valves and sensors



One row per valve, igniter and sensor on the propulsion system, and whether

Fajita drives or reads it. Blanks and question marks are questions for

propulsion (James). Nothing here is decided; see \[decisions.md](../decisions.md).



Updated 23 November 2026 from James in the Fajita Discord post (Seán agreed

with the scope): Fajita sits by the two main valves; it actuates both main

valves, fires the igniter's e-match, reads pressure transducers and runs the

abort procedures. There are three tanks (fuel, oxidiser, nitrogen), each with

a vent valve, and two e-regs, each on its own board in the plumbing between

the tanks.



\## Valves and igniter



|Item|What it does|Fajita's?|What moves it|Where|Current|Unpowered state|Source|

|-|-|-|-|-|-|-|-|

|Main fuel valve|Lets fuel into the engine|Yes|Servo; no angle sensor (Jay, 20 Nov)|By the engine, beside Fajita||Holds position (servo). Acceptable?|James, 23 Nov; Jay, 20 Nov|

|Main oxidiser valve|Lets nitrous into the engine|Yes|Servo; angle sensor?|By the engine, beside Fajita||Holds position (servo). Acceptable?|James, 23 Nov|

|Vent, bottom tank (which tank?)|Releases that tank's pressure, including after an abort|Proposed: Fajita ("maybe", James)||Bottom tank||Must open without power (LV-0190)|James, 23 Nov|

|Vents, top two tanks|As above|Proposed: the e-reg boards ("maybe", James). Conflicts with D-21Nov.10: Fajita must be able to vent whatever the e-reg does||Top two tanks||Must open without power (LV-0190)|James, 23 Nov|

|e-reg valve 1|Meters nitrogen into a propellant tank to hold its pressure (inferred)|No: e-reg board 1|Servo (D-21Nov.10)?|Plumbing between tanks||?|James, 23 Nov; D-21Nov.10|

|e-reg valve 2|As above, for the other propellant tank (inferred)|No: e-reg board 2|Servo?|Plumbing between tanks||?|James, 23 Nov|

|Igniter e-match|Lights the igniter, which lights the engine|Yes|Fajita's firing channel: arm switch, high side, low side, continuity check|Engine|E-match all-fire / no-fire?|Not firing|James, 23 Nov; LV-0030|

|Fill valves|Load propellant and nitrogen|? On the vehicle or on the ground?|||||Not mentioned; LV-0110, 0130, 0150|



\## Sensors



James counts about eight pressure transducers (PTs) on the vehicle. Which of

them Fajita reads directly is open.



|Item|Measures|Fajita reads it?|Where|Output type|Source|

|-|-|-|-|-|-|

|PT, engine|Chamber pressure|? (close to Fajita)|Engine||James, 23 Nov|

|PT, igniter|Igniter pressure (is the igniter a torch with its own valves?)|? (close to Fajita)|Igniter||James, 23 Nov|

|PT, fuel tank|Tank pressure|?|Fuel tank||James, 23 Nov|

|PT, oxidiser tank|Tank pressure|?|Oxidiser tank||James, 23 Nov|

|PT, nitrogen tank|Tank pressure|?|Nitrogen tank||James, 23 Nov|

|PT, e-reg 1|Regulated pressure (inferred)|? Or a cross-check over the e-reg link (D-21Nov.10)|e-reg 1||James, 23 Nov|

|PT, e-reg 2|Regulated pressure (inferred)|? As above|e-reg 2||James, 23 Nov|

|PT, spare|?|?|?||James, 23 Nov|

|Temperature sensors|?|?|?||Not mentioned 23 Nov; in the Notion brief|

|Angle sensors|Valve position|?|On the servo valves except main fuel (Jay, 20 Nov)||Not mentioned 23 Nov|



\## Count check



Fajita Notion: about nine servo valves, three per bank. James (23 Nov): two main

valves, three vents and two e-regs, which is seven. Are the other two fill

valves, igniter valves, or did the plan change?





