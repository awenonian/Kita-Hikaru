# State — GM-facing

The truth behind the ledger. Secrets, who is actually where, what is moving
offscreen, clocks and how far along they are, what a thing really is.

Terse and revised freely, like the player-facing ledger — but this one is
allowed to know things.

Mark anything that hasn't reached play yet, so a later session doesn't mistake
your decision for something the table established.

## Chaos factor

**5** — how much the world intrudes, 1 to 9. Feeds `scripts/oracle.py`.

Move it one step after a scene: up if the player ended less in control than
they started, down if more. Not further, and not because a scene felt slow.

## Clocks

Day 0 = the morning session 1 opens.

| Clock | Segments | Filled | What happens when it completes |
|---|---|---|---|
| Rent (due day 9) | 9 days | 0 | Rent unpaid → late fee, then Brightwell "arrears notice" — which under the addendum is a second default trigger. |
| Inspection of 14-C | 6 | 0 | Odessa's notice arrives day 1 for day 6. If refused/no access → Cadmus Vell logs "refusal of entry"; 14-C flagged non-compliant; default clock starts. |
| TITHE build (fragments #6–9) | 4 | 1 (Kita took #6; has NOT delivered — now knows what it does. If she delivers, fills; if she sabotages/stalls, the Tally finds another contractor, ~3 days) | Each fragment taken by a contractor fills one (~2–3 days each; #6 goes to someone else in 2 days if Kita doesn't take it). Then deployment. |
| TITHE deployment | 4 | 0 | Compliance module live in all 5 Spindle Cross properties: smart locks can seal units and auto-log refusals; defaults harvest at scale. |
| Crew finds Miku | 3 | 3 — COMPLETE S1 day 0 late cycle: Korrask met Miku at Nib's | Korrask waits at Nib's on Miku's cycle. Fills on each Miku trip to the Sump or each Nib conversation about "the builder." Complete → the crew makes contact through Miku. |
| Venn's window | 10 days | 0 | Venn's legal filing window; if the crew can't deliver, Jess hires Gaspar Ilk (sloppy), the run goes loud, Brightwell tightens security. |
| Nib holding gimbal parts (6 cr) | 3 days | 0 | Parts go back on the pegboard; Nib mildly put out, not angry. |
| Lolo's studio | 3 weeks | 0 | Pinwheel Motion hires someone else. Lolo is gently crushed; tells Kita only if asked. |
| Hikaru relocation | ~10 weeks | 0 | Aiko and Tomas leave for Aballon. Aiko sends the message ~2 weeks before, regardless. |

## The truth (session zero; NOT YET IN PLAY unless marked)

- **Tallyhall Financial** — legitimate on paper. Inside it, **the Tally**: a cell of **Mammon** worshippers (archdevil of Erebus, Hell's vaults; per GM Core thought to have "ascended to a purely digital form along with the evolution of mortal currencies"). Leader **Director Sabine Ostrava**. Owns Specwork and Brightwell Residential.
- **The addendum.** On lease renewal, tenants click through a linked addendum. It is a real infernal contract: on *default*, the tenant pledges "assets, tangible and intangible, in this world and any other." In Hell's accounting that includes the soul, collected at death. Default triggers include "breach of inspection compliance" and "arrears."
- **TITHE** — the compliance module for Brightwell's new smart locks, built from nine anonymous Specwork fragments (sliced by Whistle on Ostrava's office's instructions) so no contractor sees the whole. Fragment #6 (in Kita's queue) converts "access refused" events into a breach record. Kita's distinctive style would be identifiable in the finished machine if she writes it.
- **Kita signed the renewal** ~2 months ago, unread. She's postponed two inspections. Odessa faked the second as "completed," which is the *only* reason 14-C isn't already flagged. The audit will expose it.
- **Eleven Spindle Cross households** have been evicted via default so far. Their debts (and pledges) are held by the Tally. They're scattered — some in the Spike, one family with relatives in the Armada.
- **Remote recon (S1 day 1, crit):** Kita confirmed the lease-processing DB is on `MRW-INT`, internal-only. She saw the 9-module `tithe` build on a careless staging box and grabbed her own module's full interface spec. She did NOT see: the signed infernal addenda, the Mammon sigil, Whistle's name, or which specific units are flagged (that's all on the internal segment / in the contracts). No trace left.
- **The crew's job:** Hollis Venn (Abadaran, First Vault) hired the *Tin Lantern* to pull lease-processing records from the **Brightwell field office** (ground floor of **Marrow Street Stack**, another Spindle Cross Brightwell building, two blocks from Kita). Venn thinks it's ordinary fraud. Abadar's courts would void infernal clauses as fraud if proven — this is how tenants get saved.
- **Leaving Absalom:** Tallyhall mirrors the Tally's ledgers to a data vault aboard **the *Countinghouse***, a Tallyhall-owned ship in the Armada that periodically jumps to Verces. The Tally reports to a wider Mammonite network off-station. Destroying the Absalom copy doesn't free anyone; the off-station ledger is where the pledges live.
- **The damp corner** in 14-C: slow leak from a cracked coolant line behind the wall panel. Harmless now. It is exactly what an inspection would write up.
- **Tallow & Leaf** owner **Ravae Ost** (lashunta) moved to Castrovel. Shop space now empty, for lease — by Brightwell.

## Player preferences (table)

- **Fail-forward.** A failed roll should cost something or teach something, not dead-end. Reserve "now they're hunting you" for critical failures. Investigation especially never dead-ends.

## Events not yet surfaced

- **S1 day 0:** Brightwell's system logged a `TAMPER_SUSPECTED` event on 14-C's lock (interior side). It lands in Cadmus Vell's compliance queue. Effect: when Odessa's notice goes out (day 1), it carries an added line that the access system flagged a fault and the lock will be checked at inspection. Vell takes a personal interest in 14-C now.

## Rulings

Rules calls made where the system was silent or unclear. Once made, they hold —
a ruling that drifts between sessions is worse than either version applied
consistently.

| Situation | Ruling | When |
|---|---|---|
| BRW-ACX lock hacking | Commercial smart lock, level 2 → Hack DC 16 (PF2e level-DC). Opening interior housing is ordinary for a mechanic: no roll. Fail = tamper event sent to Brightwell; crit fail = 1-hr tamper lockdown (bolt thrown, won't open either side) + notification; success = access, local log entry of debug-port session; crit = no trace. | S1 day 0 |
| Drone control range | Ignored by player choice. Friction comes from Miku's limits and jobs needing Kita present. | Session zero |
| Acting through Miku | Kita's modifiers for what she does through Miku (speech, perception, knowledge); Miku's for what its body does (Stealth, Acrobatics, attacks, Thievery/manipulation). No hacking through Miku without Network customization. | Session zero |
| Standard robot customizations | May fill a drone's commercial customization slots. | Session zero |
| Anxiety | No mechanics. GM may apply ad hoc circumstance penalties when her state would plausibly impair a check. | Session zero |
| Modify on Miku | Still requires Kita adjacent. | Session zero |
| Drone at 0 HP | Mechanic drone rule (emergency reboot, 1 HP after 1 minute) overrides the generic robot-companion "broken" track. | Session zero |

---
