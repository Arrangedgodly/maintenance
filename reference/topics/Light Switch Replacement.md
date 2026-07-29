# Light Switch Replacement

> Replacing the three common switch types: single-pole, 3-way, and dimmer/slider. Builds the universal photograph-first, one-wire-at-a-time procedure onto the [[Electrical Safety Fundamentals|safety fundamentals]].

## Summary
The universal procedure for every switch: breaker off, verify dead on **every** wire in the box, photograph before disconnecting, and move one wire at a time. Loop wires clockwise under screws; two wires under one screw earns a [[GLOSSARY#Pigtail|pigtail]]. A [[GLOSSARY#Single-pole switch|single-pole]] is symmetric — two blacks on brass, ground on green.

The [[GLOSSARY#3-way switch|3-way]] controls one light from two locations and turns on identifying the [[GLOSSARY#Common terminal (3-way switch)|common terminal]] (the dark screw) — the single wire you cannot mix up. Common on the wrong screw is the classic "works from one side only" failure. The two [[GLOSSARY#Traveler wires (3-way circuits)|traveler]] wires are interchangeable with each other but never go on common.

The [[GLOSSARY#Dimmer switch (slider)|dimmer]] adds two checks: is there a neutral bundle in the box (most modern LED dimmers are [[GLOSSARY#Neutral-required dimmer|neutral-required]]), and does the dimmer type match the bulb? A [[GLOSSARY#TRIAC dimmer (forward-phase / leading-edge)|TRIAC]] dimmer is the home-center default; an [[GLOSSARY#ELV dimmer (reverse-phase / trailing-edge)|ELV]] is smoother for electronic LED drivers. A wrong match flickers, buzzes, or burns out the LED driver. Dimmers use pigtail leads under wire nuts, not screw terminals.

When in doubt, photograph, tag the common, and re-verify dead before reopening a box. Hands-on swaps belong in [[ACTION-ITEMS]].

**Related:** [[Electrical Safety Fundamentals|Electrical safety]] · [[Outlet & GFCI Replacement|Outlets & GFCI]] · [[Ceiling Fan & Light Fixture Replacement|Ceiling fans]] · [[GLOSSARY#Common terminal (3-way switch)]] · [[GLOSSARY#Dimmer switch (slider)]] · [[ACTION-ITEMS]]

## Full procedure

> Hands-on tasks live in [[ACTION-ITEMS]].

## Universal procedure (all switch types)
1. Turn off breaker (use verified panel map).
2. Verify dead — test **every** wire in the box (second circuit may run through).
3. Remove wall plate + mounting screws, pull switch out gently.
4. **Photograph wiring before disconnecting.** Essential for 3-ways.
5. **One wire at a time:** disconnect, connect to same terminal on new switch, repeat.
6. Loop wires **clockwise** around screws (tightening pulls tighter). Never two wires under one screw — use a [[GLOSSARY#Pigtail|pigtail]].

## Type 1 — [[GLOSSARY#Single-pole switch|Single-pole]]
One location, one light. Two brass terminals + ground. Simplest — practice on this first.

- **Two black wires → two brass terminals.** Order doesn't matter (symmetrical).
- **One bare/green → green ground screw.** Always connect, even if old switch skipped it.
- **Neutral not connected** to the switch.

> ⚠️ **White wire on old switch?** May be a hot "switch leg" (older wiring; should have black tape but often doesn't). If white was on brass, put it on brass of new switch. Don't "fix" it without tester verification.

## Type 2 — [[GLOSSARY#3-way switch|3-way]] (two-location control)
Light controlled from two switches (staircase, hallway ends). **One switch in a pair**, not three positions. Two 3-way switches work via a traveler pair.

### The key: identify the [[GLOSSARY#Common terminal (3-way switch)|common]]
Three terminals: **one common + two travelers.**
- **Common screw = dark (black/dark brass)** — distinct from the two brass traveler screws. The wire you must not mix up.
- Traveler screws = brass (two of them).

| Screw | Color | Wire |
|---|---|---|
| Common | **Dark** | Switch 1: always-hot from panel. Switch 2: switched-hot to light. |
| Traveler 1 | Brass | Often red, but **test — never assume by color** |
| Traveler 2 | Brass | Often white, but white is frequently the common (especially at the load-end switch) — **test — never assume by color** |
| Ground | Green | Bare/green |

### Procedure
1. **Photograph before disconnecting.**
2. Identify common — the wire on the dark screw. Tag with tape.
3. Travelers are interchangeable with each other (brass↔brass), but neither goes on common.
4. Connect common → dark screw on new switch. **This step matters most.**
5. Connect two travelers → two brass screws (order irrelevant).
6. Connect ground.

> ⚠️ **Classic failure:** common on a traveler screw → circuit works but only from one location, or state depends on other switch. **If 3-way only works from one side = common on wrong screw.**

> Lost track of common? The safest path is to identify it with the breaker off using a plug-in circuit tracer or by tracing the cable — never assume wire color (white is frequently the common, especially at the load-end switch). If you can't identify common confidently de-energized, **call an electrician** rather than probing a live 3-way box.

## Type 3 — [[GLOSSARY#Dimmer switch (slider)|Dimmer / slider]]
Adds two checks beyond standard switch: **compatibility** and **neutral.**

### Check 1: neutral in the box?
- **Neutral present** (white bundle capped in back) → standard LED dimmer; connect its white lead to bundle.
- **No neutral bundle** → "switch loop" (pre-2011 wiring). Need a [[GLOSSARY#Neutral-required dimmer|no-neutral-rated]] dimmer (leaks current through bulb; works with some LEDs only). Or pro runs a neutral.

### Check 2: match dimmer to bulb
| Dimmer | Works with | Mismatch symptom |
|---|---|---|
| [[GLOSSARY#TRIAC dimmer (forward-phase / leading-edge)|TRIAC]] (forward-phase, "MLV") — home-center default | Incandescent, halogen, LEDs rated "forward-phase" / "TRIAC-compatible" | Flicker, buzz, low-end cutout |
| [[GLOSSARY#ELV dimmer (reverse-phase / trailing-edge)|ELV]] (reverse-phase) | Electronic LED drivers, ELV transformers | Requires neutral; smoother LED |
| Universal / programmable | Both | Removes guesswork; more $ |

> ⚠️ Bulb package = spec sheet. "Dimmable" → check for dimmer type. LED on incompatible dimmer flickers/buzzes; on non-LED-rated dimmer can damage driver. Same-manufacturer bulb+dimmer with compatibility chart = safest.

### Check 3: wattage rating
Don't exceed dimmer's max wattage (usually 600W incandescent; LED-load rating often specified separately and lower). Rarely a problem with low-wattage LEDs unless many bulbs on one circuit.

### Dimmer wiring (pigtail leads, wire-nutted — not screw terminals)
- **Black (line)** → always-hot feed
- **Black (load) or red** → switched-hot to light
- **Green** → ground
- **White** → neutral bundle (skip if no-neutral rated)

## Finishing (all types)
1. Tuck wires neatly (no sharp bends). Switch seats without fighting.
2. Mount switch — "ON" reads upright (single-pole).
3. Install wall plate.
4. Restore breaker.
5. **Test:** single-pole toggles light; 3-way from **both locations, both starting positions**; dimmer full-on → smooth dim → no flicker.

> ⚠️ Doesn't work? **Breaker off before opening box again.** Re-verify dead every time.

## DIY / Pro boundary
| DIY | Call an electrician |
|---|---|
| Like-for-like swap (single-pole, 3-way, dimmer) | New switch location (new wiring run) |
| Adding a dimmer where a switch exists | Aluminum wiring |
| Upgrading to a smart switch (if neutral present) | Switch loop → adding a neutral |
| 3-way you can't diagnose after 2 attempts | Any permit-required work |

## Sources
- [The Spruce — Single-Pole Switch](https://www.thespruce.com/how-to-wire-and-install-single-pole-switches-1152330)
- [The Spruce — Anatomy of a 3-Way Switch](https://www.thespruce.com/anatomy-of-a-three-way-switch-1152436)
- [r/askanelectrician — Identifying Traveler vs. Common](https://www.reddit.com/r/askanelectrician/comments/wapz39/3way_switch_how_do_i_determine_which_is_the/)
- [Lumicrest — ELV/MLV/TRIAC Explained](https://lumicrest.com/elv-mlv-forward-phase-trailing-edge-triac-whats-it-all-mean/)
- [Sunme Lighting — TRIAC Dimmer Guide](https://sunmelighting.com/en/triac-dimmer-guide-how-it-works-led-compatibility-and-uses/)
