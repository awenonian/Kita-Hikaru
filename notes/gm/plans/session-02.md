# Session 2 — plan

Prep the world, not the plot. What is true, and what each party does this week
if unopposed. None of it is a sequence.

## Recap check (S2 open)

Player recap: Kita picked up a coding task, then a crew contacted her; the crew
is targeting the company that gave her the task and owns her apartment; she
scoped their systems, found sinister stuff, decided to help the crew "and maybe
try to get a little more money out of the company while doing it." Matches the
notes; no absences. Nothing to fix.

## Situation, day 2 morning

- 21 cr. Rent 30 cr due day 9. #6 deadline **end of day 4** (accepted day 0).
  #9 burner hold lapses **end of day 5**. Nib's hold lapses **end of day 3**.
- Run: **night of day 5** (Jess will confirm). Inspection: **day 6, 1000**. The
  run is the night before the inspection.

## Parties this week, unopposed

- **Jess:** overnight sends: walkthrough happening day 3; run night of day 5;
  "What does your drone need to carry? Tell me now, Korrask builds to spec." She
  does not know about the inspection and will not move the run for it unless
  told why (and then only if it costs the crew nothing).
- **Korrask:** wants to see Miku up close at the Lantern; will build any rig Kita
  specs (she's good, fast, and loud about it). Will offer, unprompted, to "fix
  the little one's stupid screen" — she thinks 7 characters is a defect.
- **Ilyre:** wants to "meet properly" — will message Kita directly (Jess gave her
  the code) on day 2 or 3. Talks a lot. Holds the office layout (below). Thinks
  the receptionist is Pim.
- **Whistle ("Compliance Engineering"):** day 2, messages the *burner* on #9:
  polite ETA request, offers a 25 cr "expedite bonus" for delivery by end of day 3.
  Day 4 if still silent: second message, cooler, cc's "Office of the Director."
  Fills the Tally-notices clock.
- **The Tally:** if #6 and #9 both get submitted, the module is complete and
  deployment begins (clock fills fast — ~4 days to live in all 5 properties,
  Coil Street first since 14-C is on the audit). Payment releases from Specwork
  escrow on acceptance (~1 day after submission, after Whistle runs the
  integration tests).
- **Odessa:** day 4, "Confirming Thursday 1000. —O." Day 6, 1000, at the door
  with Cadmus Vell and one Brightwell security contractor.
- **Lolo:** day 2 message (see her file).
- **Nib:** hold ends day 3. If Miku comes with 6 cr he's pleased. "Someone's been
  asking about you, little bird" is spent (Korrask). New line: Korrask came back
  and bought Nib's whole tray of servo couplings and called him a genius by
  association. He's insufferable about it.
- **Gaspar Ilk:** sore. Owes a Free Captains fence **Dunmore Kask** (half-orc, fences out of a bar in the Arms called the Low Tide).
  Ilk knows: Brightwell, the field office, "in a few nights." Sells it to Kask
  for debt relief; Kask sells it on to Brightwell security as a "tip" for cash.
  **Oracle (S2 open): YES, AND — Ilk went to Kask the night of day 1, and Kask has
  already sold it on to Brightwell security (day 2 morning).** Effect: from the
  night of day 3, one Brightwell contractor sits *inside* the field office
  overnight (lobby chair, awake-ish), and the drive-by patrol doubles (~2200,
  0000, 0200, 0400). Brightwell knows "a break-in, this week, freelancers" — not
  who, not the night, nothing about a drone. **Telegraph:** Ilyre's day-3
  walkthrough sees a folding chair and a thermos behind the counter; Jess hears
  Ilk paid off Kask in full; Teodor mentions "night shift" to Ilyre.

## The Marrow Street field office (truth)

Ground floor of **Marrow Street Stack**, two blocks from Coil Street. Brightwell
logo over a frosted door. Open 0900–1700.

- **Front:** lobby, a counter, receptionist **Teodor** (day only). Ilyre's way in
  is by day, as a prospective tenant, to plant something or prop something.
- **Back office:** four desks, a printer, a wall of ring binders nobody uses.
  Terminals are thin clients on `MRW-INT` — logged out at night, auto-lock.
- **Storeroom:** the Brightwell crates of reclaimed BRW-ACX units (Nib's van). 41
  units, counted, on a clipboard. Brightwell counts their scrap.
- **Server closet:** behind the back office. A BRW-ACX lock on it (Kita knows
  this lock better than anyone now). Inside: one rack, the `MRW-INT` box, a
  switch with free ports, a small UPS. No external route.
- **Ceiling vents:** Small-creature-sized duct runs from a grille in the
  storeroom to a grille over the back office. Miku fits. Duct is dusty (a trail).
- **Maintenance crawlway** from the storeroom out to the district crawl network;
  connects (via ~300 ft of crawl) to the back room of the empty Tallow & Leaf
  unit. Neither Ilyre nor Jess knows. (Loose clue; Kita could find it from
  district maintenance maps — Computers or Society, or by Miku scouting.)
- **Security at night:** front door + closet door are BRW-ACX (DC 16 to hack per
  ruling; she already knows where the debug header is, so finding it is free). Two ceiling cameras (front, back office) on a local
  NVR in the server closet — not the closet itself. A Brightwell security
  contractor **patrol** checks the door from outside at ~2300 and ~0300 (drive-by,
  not inside). Motion sensor in the lobby only.
- **What's on MRW-INT:**
  - Lease DB: every Spindle Cross renewal + addendum. Signed addenda carry a
    watermark sigil — **coin inside a keyhole** (Mammon; Occultism DC 15 to
    recognise as Mammon; recognising it as *infernal* needs no roll for her).
  - Default filings (the 11) + the audit list: **14-C "log anomaly — verify"**
    and "access fault — tamper suspected."
  - **TITHE deploy mirror**: compiled firmware builds pushed to building locks.
    It *pulls* from `vault.tallyhall.int/tithe` — the canonical repo is at
    Tallyhall HQ in the Eye, not here. Deleting here = 1–2 day delay, not
    destruction. Discoverable by any look at the deploy config (no roll).
  - Also: an outbound nightly sync job to "CH-MIRROR" (the *Countinghouse*) —
    the ledger mirror. Seen as a hostname only.
- **What the crew needs:** Venn's records (renewal addenda + default filings).
  Kita's own wants are hers to bring.

**The `Network`-less problem:** Miku can't hack (ruling). Miku *can* physically
plug in a tap/relay Kita builds (Miku's Thievery +3 via Manual Dexterity for
fiddly placement; plugging into a free switch port is not fiddly — no roll).
Then Kita hacks from home through the relay. Building the relay: Crafting, an
ordinary job for her, few cr of parts — **from Nib**. Don't suggest it; let the
player find it or another way.

## Possible openings (commit to none)

1. Day 2 morning, 14-C: Jess's overnight message ("what does your drone need to
   carry?"), and an unread notification on the burner account. Lean here.
2. Ilyre calls — voice — instead of messaging. (Save; strong tone scene.)

## Encounter prep (if it goes physical)

Look up statblocks in the skill before running any fight. Brightwell security
contractor ~ level 1 human guard. Cadmus Vell ~level 2 + imp. Telegraph first.
