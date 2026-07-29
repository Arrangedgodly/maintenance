# Electrical Safety Fundamentals

> The safety gate every electrical lesson depends on. Covers the verify-dead protocol, the hot/neutral/ground mental model, wire gauge vs breaker matching, and the GFCI/AFCI split.

## Summary
The one non-negotiable rule before touching any wire: flip the [[GLOSSARY#Circuit breaker|breaker]], verify dead with a [[GLOSSARY#Non-contact voltage tester|tester]], and test the tester first on a known-live [[GLOSSARY#Circuit|circuit]]. "I flipped the breaker" is never enough — panels are mislabeled, shared neutrals feed boxes from two breakers, and a white wire may be a hot switch leg. Every wire is live until a tester says otherwise.

Three [[GLOSSARY#Hot / Neutral / Ground|conductors]]: hot (black, brass), neutral (white, silver), and ground (bare/green, safety path only). Match [[GLOSSARY#Wire gauge (AWG)|wire gauge]] to breaker — 14 AWG on a 20A breaker starts fires. Know the [[GLOSSARY#GFCI (Ground Fault Circuit Interrupter)|GFCI]] vs [[GLOSSARY#AFCI (Arc Fault Circuit Interrupter)|AFCI]] split: GFCI protects people from shock (wet areas), AFCI protects property from arc fires (living areas); modern kitchens need both. A [[GLOSSARY#Multimeter|multimeter]] confirms dead definitively; a circuit-breaker finder builds your panel map.

DIY stops at like-for-like device swaps and existing-box work; new circuits, [[GLOSSARY#Junction box|junction box]] overstuffing, scorching, and aluminum wiring are pro territory. Track every hands-on task in [[ACTION-ITEMS]], and feed results into the [[Master Seasonal Checklist|master seasonal checklist]] (annual GFCI test).

**Related:** [[Light Switch Replacement|Light switches]] · [[Outlet & GFCI Replacement|Outlets & GFCI]] · [[Ceiling Fan & Light Fixture Replacement|Ceiling fans]] · [[GLOSSARY#GFCI (Ground Fault Circuit Interrupter)]] · [[GLOSSARY#AFCI (Arc Fault Circuit Interrupter)]] · [[ACTION-ITEMS]]

## Full procedure

> Hands-on tasks live in [[ACTION-ITEMS]].

## The non-negotiable rule (before touching any wire, every time)
1. **Turn off the correct breaker.**
2. **Verify dead with a tester.**
3. **Test the tester first** on a known-live circuit.

Electricians call it "test before you touch." Three steps — the only thing separating safe DIY electrical from a shock.

## Why "I flipped the breaker" isn't enough
- Panels are mislabeled constantly (electrician, previous owner, renovations).
- A circuit may be powered from two breakers (shared neutral, 240V).
- Multiple circuits often run through one box (common in multi-switch boxes).
- → Only a tester tells you whether the specific wire you'll touch is live.

## The mental model: hot / neutral / ground
| Conductor                                    | Color          | Function                                                       | Screw  |
| -------------------------------------------- | -------------- | -------------------------------------------------------------- | ------ |
| [[GLOSSARY#Hot / Neutral / Ground\|Hot]]     | Black (or red) | Carries current IN. Assume live until proven dead.             | Brass  |
| [[GLOSSARY#Hot / Neutral / Ground\|Neutral]] | White          | Carries current OUT, completes circuit.                        | Silver |
| [[GLOSSARY#Hot / Neutral / Ground\|Ground]]  | Bare/Green     | Safety path only — carries fault current. No current normally. | Green  |
**Circuit complete** = current flows panel hot → load → panel neutral. Ground sits outside normal flow.

> ⚠️ A white wire in a switch box may be a "switch leg" serving as hot. Should be re-identified with black tape/marker but often isn't. **Always verify with tester — never assume from color alone.**

## Wire gauge (AWG) and breakers
| Wire | Max breaker | Typical use |
|---|---|---|
| 14 AWG | 15A | Lighting, general receptacles |
| 12 AWG | 20A | Kitchen, bathroom, laundry, microwave |
| 10 AWG | 30A | Electric dryer (240V double-pole) |

> ⚠️ **Never put a larger breaker on a smaller wire.** 20A breaker on 14 AWG → wire overheats → insulation melts → fire in wall. Match breaker to wire gauge.

## GFCI vs AFCI
| | [[GLOSSARY#GFCI (Ground Fault Circuit Interrupter)|GFCI]] | [[GLOSSARY#AFCI (Arc Fault Circuit Interrupter)|AFCI]] |
|---|---|---|
| Protects | **People** (shock) | **Property** (fire) |
| Detects | Current leak (~5 mA mismatch hot↔neutral) | Dangerous arcing signature |
| Required in | Bathrooms, kitchens, garages, outdoors, laundry, unfinished basement, within 6 ft of sinks | Bedrooms, living rooms, family rooms, dining rooms, kitchens, hallways, closets, laundry |
| Not required in | — | Bathrooms, garages, outdoors |
| Form | Receptacle or breaker | Usually breaker (sometimes receptacle) |

**Kitchen overlap (modern NEC):** requires **both** GFCI and AFCI. Solutions: dual-function AFCI/GFCI breaker, or dual-function receptacle.

## Know your panel
- Find it; confirm accessible (not behind furniture/in closed closet).
- **Main breaker:** big double-pole at top (100/150/200A). Kills power to whole panel. Emergency "everything off."
- **Single-pole breakers:** thin, one slot, 120V (lights, outlets).
- **Double-pole breakers:** thick, two slots, 240V (dryer, oven, AC, water heater).
- **Audit the labels:** flip → see what stops → write down. Factory label is wrong until verified. Use a radio/lamp or a circuit-breaker finder (~$25).

## Tools
| Tool | For | Cost |
|---|---|---|
| **Non-contact voltage tester** | Verify-dead. First tool on every job. | $15 |
| Multimeter (digital) | Definitive voltage + continuity | $25–40 |
| Circuit-breaker finder | Map breakers to outlets/switches | $25 |
| Insulated screwdrivers (slotted + Phillips) | Terminal screws, cover plates | $15 |
| Wire strippers / combo tool | Strip, cut, bend loops | $15 |
| Needle-nose pliers (insulated) | Bend loops, reach into boxes | $15 |

Start with the non-contact tester — you'll use it on every electrical job for life.

## DIY / Pro boundary
| DIY (after fundamentals + switch practice) | Call a licensed electrician |
|---|---|
| Like-for-like switch/outlet replacement | New circuit or extended circuit |
| Light fixture swap (existing box, same wiring) | Panel upgrade / replacement |
| Ceiling fan (where fan-rated box exists) | Aluminum wiring (any) |
| Breaker replacement (same amperage, same wire gauge) | Any permitted work |
| Panel mapping | Subpanel addition / service entrance / meter |

> ⚠️ **Red flags — stop and call a pro:**
> - **Aluminum wiring** (common 1965–1973) — fire risk, special connectors (AlumiConn, COPALUM) required.
> - **Box packed full of wires** or any signs of **scorching/melting** — overloaded circuit, needs diagnosis not a DIY swap.

## Sources
- [Mike Holt — GFCI and AFCI (2023 NEC)](https://www.mikeholt.com/newsletters.php?action=display&letterID=2750)
- [Expert CE — GFCI vs AFCI Requirements](https://expertce.com/learn-articles/gfci-vs-afci-nec-requirements/)
- [Family Handyman — GFCI vs AFCI](https://www.familyhandyman.com/article/gfci-vs-afci/)
- [The Spruce — Wire a Single-Pole Light Switch](https://www.thespruce.com/how-to-wire-and-install-single-pole-switches-1152330)
- [Dummies — Replace a Light Switch](https://www.dummies.com/article/home-auto-hobbies/home-improvement-appliances/electrical/how-to-replace-a-light-switch-185346/)
