# Outlet & GFCI Replacement

> Two skills in one note: swapping a standard [[GLOSSARY#Receptacle (outlet)|receptacle]] and adding [[GLOSSARY#GFCI (Ground Fault Circuit Interrupter)|GFCI]] protection. Covers the critical termination-method decision and the line-vs-load rule that makes GFCIs actually protect.

## Summary
Same universal procedure as switches: breaker off, verify dead, photograph, one wire at a time. The critical decision is the termination method — [[GLOSSARY#Side-wire (screw terminal)|side-wiring]] is the gold standard, [[GLOSSARY#Back-wire (screw-pressure-plate)|back-wiring]] is reliable, and [[GLOSSARY#Back-stab (push-in) connection|back-stabbing]] is the fire-causing one to abandon on sight. On a [[GLOSSARY#Duplex receptacle|duplex]], black to brass, white to silver, ground to green; two cables means pigtail or use both screw sets, and leave the [[GLOSSARY#Break-off tab (receptacle)|break-off tab]] unless you're splitting a half-hot. Buy [[GLOSSARY#Tamper-resistant (TR) receptacle|tamper-resistant (TR)]] receptacles — required since 2008.

The [[GLOSSARY#GFCI (Ground Fault Circuit Interrupter)|GFCI]] is the highest-value safety upgrade in an older home: one at the start of a circuit protects every outlet after it via [[GLOSSARY#Downstream protection|downstream protection]]. The whole job hinges on getting [[GLOSSARY#Line vs. load (receptacle wiring)|line vs load]] right — LINE is the cable from the panel, LOAD runs onward. Swapped line/load powers up but defeats protection; both cables on LINE leaves downstreams unprotected. Identify line with a tester **before** landing wires, then test (press TEST, watch the lamp die, RESET, confirm downstreams also die).

GFCI even protects ungrounded two-prong circuits — it detects a hot/neutral imbalance, not a ground wire — so it's the cheap retrofit for old homes, labeled "No Equipment Ground." Track every install and annual test in [[ACTION-ITEMS]].

**Related:** [[Electrical Safety Fundamentals|Electrical safety]] · [[Light Switch Replacement|Light switches]] · [[Master Seasonal Checklist|Seasonal checklist]] · [[GLOSSARY#GFCI (Ground Fault Circuit Interrupter)]] · [[GLOSSARY#AFCI (Arc Fault Circuit Interrupter)]] · [[ACTION-ITEMS]]

## Full procedure

> Hands-on tasks live in [[ACTION-ITEMS]].

## Universal procedure (same as switches)
1. Breaker off. Verify dead — test top + bottom of receptacle + every wire.
2. Remove plate + mounting screws, pull receptacle out.
3. **Photograph wiring** before disconnecting (esp. GFCI line/load).
4. One wire at a time: disconnect → matching terminal on new device.
5. Tuck, mount, plate. Restore power. Test.

## The critical quality decision: termination method

| Method | How | Verdict |
|---|---|---|
| **[[GLOSSARY#Back-stab (push-in) connection|Back-stab]]** (push-in) | Wire into spring-loaded hole | ⛔ **Avoid.** Spring loosens → arcing → fires. 14 AWG only. **If found, move wires to screw terminals.** |
| **[[GLOSSARY#Back-wire (screw-pressure-plate)|Back-wire]]** (screw-pressure-plate) | Wire under plate, clamped by adjacent screw | ✓ Reliable. 15A + 20A. Pro-favored for speed. |
| **[[GLOSSARY#Side-wire (screw terminal)|Side-wire]]** (screw terminal) | Clockwise hook under screw | ✓ **Gold standard.** Most defensible. Default. |

> **How to tell back-stab from back-wire:** both have back holes. Back-stab = spring holds wire, screw is unrelated. Back-wire = tightening the adjacent screw clamps the wire. If the screw affects the wire in the hole → back-wire (good). If not → back-stab (bad).

## Standard receptacle wiring
- **Black (hot)** → brass (smaller slot side)
- **White (neutral)** → silver (larger slot side)
- **Bare/green** → green

**Two cables (in + out):** pigtail (most reliable — device failure doesn't kill downstream) OR both wires on device's two screw sets (faster, device failure kills downstream).

> Don't remove the [[GLOSSARY#Break-off tab (receptacle)|break-off tab]] unless deliberately splitting (switched half-hot). If old receptacle had it removed, photograph + match.

> **Buy [[GLOSSARY#Tamper-resistant (TR) receptacle|tamper-resistant (TR)]] receptacles** — required by NEC since 2008. Internal shutters block foreign objects. Slightly stiff to plug into; normal.

## GFCI installation — adding protection

> Highest-value electrical safety upgrade in an older home. GFCI at the first outlet on a circuit protects every outlet after it.

### The key: LINE vs LOAD

| Terminal | Connects | Protects |
|---|---|---|
| **LINE** (always used) | Cable from panel | The GFCI receptacle itself |
| **LOAD** (optional) | Cable(s) going downstream | Every outlet after this one ([[GLOSSARY#Downstream protection|downstream protection]]) |

### Identify which cable is line vs load
**Do this with wires capped and separated — never with exposed, loose conductors energized.**
1. **Breaker OFF, verify dead.** Disconnect old receptacle, photograph first.
2. Cap each cable's black wire in its own wire nut; keep whites separated too.
3. **Briefly energize** (breaker ON). Non-contact tester → the cable whose black reads hot is **LINE**.
4. **Breaker OFF, verify dead** again before landing any wire.
5. Other cable (not hot) = LOAD (runs onward to next outlet).

> ⚠️ Don't guess. Swapped line/load → GFCI may power up but won't protect correctly, won't reset, or test button behaves wrong. If you can't identify LINE confidently with capped wires, use a plug-in circuit tracer (breaker off) — or call an electrician. Never probe live, loose conductors.

### Wiring
1. Breaker OFF, verify dead.
2. Strip ~¾" (use strip gauge on back of GFCI).
3. **LINE black → brass LINE. LINE white → silver LINE.**
4. Extending protection? **LOAD black → brass LOAD, LOAD white → silver LOAD.** Remove warning tape first.
5. Not extending? Leave LOAD empty + tape on. Cap downstream wires, push to back.
6. Ground → green screw.
7. Mount, plate, restore power.

### Test after install (non-negotiable)
1. Lamp into GFCI. On.
2. Press **TEST**. Lamp off, Reset pops out.
3. Press **RESET**. Power restored.
4. If LOAD used: lamp into each downstream outlet, press TEST on GFCI → each should lose power. Confirms downstream protection.

> **Won't reset?** Check (1) line/load swapped, (2) downstream ground-fault still present, (3) some GFCIs need firm RESET after first power-up. Still nothing → device defective or wiring error; re-verify with breaker off.

### Three classic GFCI mistakes
1. **Both cables on LINE** → GFCI works but downstream NOT protected. Symptom: TEST kills GFCI but downstream stays live. Move downstream cable to LOAD.
2. **Swapped line/load** → powers up but won't protect/reset. Re-identify with tester.
3. **Forgot ground** → GFCI still protects (works on current imbalance, not ground). But if equipment ground present, connect it to green screw.

## GFCI on ungrounded (two-prong) circuits
**GFCI provides shock protection even without a ground wire** — detects hot/neutral current imbalance, not ground. This is the cheapest major safety upgrade for older homes. Label the receptacle "No Equipment Ground" (stickers in the box) — equipment still isn't grounded, but shock protection is real.

## Where GFCI required (prioritize adding if missing)
Per NEC 210.8 (2020/2023): bathrooms, kitchens (all receptacles serving countertops + the dishwasher/disposal circuit), garages, outdoors, laundry, unfinished basements, crawl spaces, and accessory buildings. Find first outlet on circuit (closest to panel), install GFCI there with downstream on LOAD → whole circuit protected. (Pre-2020 code used a "within 6 ft of sinks" trigger; current code is broader.)

## DIY / Pro boundary
| DIY | Call electrician |
|---|---|
| Like-for-like receptacle swap | New circuit / new outlet location |
| Adding GFCI to existing box | Replacing a service panel |
| Converting two-prong to GFCI (no ground) | Aluminum wiring |
| Moving back-stab to screw terminals | Any permit-required work |

## Sources
- [r/askanelectrician — Side Wire vs Back Wire](https://www.reddit.com/r/askanelectrician/comments/rz3l4l/best_practice_side_wire_vs_back_wire_not_back_stab/)
- [Leviton — Back vs Side Wiring](https://leviton.com/support/literature/blogs/back-wiring-vs-side-wiring)
- [Electrical Technology — Back/Side/Push-in](https://www.electricaltechnology.org/2026/02/back-wiring-side-wiring-push-in-wiring-backstab-lever-edge.html)
- [Norge Electric — GFCI Line vs Load](https://norskelectric.com/blog/gfci-line-vs-load-afci-vs-gfci/)
- [r/electrical — Both wires on LINE mistake](https://www.reddit.com/r/electrical/comments/mgnn56/why_would_a_gfci_be_wired_like_this_and_instead/)
