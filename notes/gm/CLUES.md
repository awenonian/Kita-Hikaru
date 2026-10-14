# Clues

The mystery as a graph, not a trail. Nodes are places, people, and events; the
edges are what one points at another with.

## Revelations

Mark each clue **core** if the mystery cannot be solved without it. Core clues
are never gated behind a roll: if the character looks in the right place, they
find it. A roll may govern speed, extra detail, or cost — never availability.

### 1. Tallyhall owns both Specwork and Brightwell

| Clue | Where it lives | Core? | Status |
|---|---|---|---|
| Specwork's footer: "a Tallyhall Financial company" | Specwork site | yes | undelivered (player-facing STATE lists it as known — the *connection* hasn't been drawn in play) |
| Brightwell lease portal / rent receipts: "a Tallyhall Financial company" | Brightwell portal | yes | undelivered (same) |
| Pact Worlds corporate registry (Society or Computers, trivial) | infosphere | no | undelivered |
| Whistle's employer is Tallyhall, and she posts Brightwell projects to Specwork | the crew / Whistle | no | undelivered |

### 2. The Specwork fragments assemble Brightwell's lock-compliance system (TITHE)

| Clue | Where it lives | Core? | Status |
|---|---|---|---|
| Fragment #6 spec references interfaces named `BRW-ACX/compliance/*` and an event type `REFUSAL_LOGGED` | Kita's Specwork queue | yes | delivered S1 day 0 |
| New smart lock on Kita's own door: model plate / firmware ID `BRW-ACX`, "compliance module pending" | 14-C's door | yes | partly delivered S1 day 0 — via Brightwell tenant FAQ photo; door itself not yet inspected |
| Odessa's inspection notice: "compliance logged via the new access system" | Odessa's message (day 1) | no | undelivered |
| Specwork search: eight other recent narrow firmware contracts with `BRW-ACX` interfaces, all different contractors | Specwork history (Computers) | no | delivered S1 day 1 — saw all nine modules on the staging box, codename `tithe` |
| Whistle: "I just chop the specs up… project TITHE" | Whistle | no | partly — Kita has seen the deliberate 9-way compartmentalization and the name `tithe`; hasn't met Whistle |

### 3. The lease addendum is an infernal contract

| Clue | Where it lives | Core? | Status |
|---|---|---|---|
| The linked addendum in Kita's own renewal — "assets, tangible and intangible, in this world and any other"; clause structure of an infernal compact (Occultism/Arcana/Religion to *recognise*; reading it needs no roll) | Kita's lease, Brightwell portal | yes | undelivered |
| Brightwell server: addenda signed with a watermark — the sigil of **Mammon** (coin within a keyhole) | Brightwell field office server (Marrow Street Stack) | yes | undelivered |
| Evicted tenant **Marta Ilesco** (Marrow Street, evicted two months ago) has had a cold spot in her chest since — a pledge mark, visible to detect magic as a faint unholy aura | First Vault, Vault Row (she's being helped by Venn; staying in shelter Level 9) | no | **partly delivered S2 day 2** — Kita heard Marta describe the cold at her breastbone, and the paid-rent/missed-inspection/unread-addendum story; the *mark's nature* (aura) NOT revealed (Miku can't sense magic) |
| Tallyhall Eye HQ has a private chapel listed as "meditation room"; staff badge access only | Tallyhall HQ | no | undelivered |

### 4. Inspection non-compliance = default, and 14-C is about to be caught

| Clue | Where it lives | Core? | Status |
|---|---|---|---|
| The addendum's default clause lists "breach of inspection compliance" | Kita's lease | yes | undelivered (she saw the CODE wiring ComplianceRecord→default, not the lease clause itself yet) |
| Venn's data: every default in Brightwell properties cites inspection non-compliance; up ~900% in 4 months | Venn / the crew | yes | delivered S1 day 1 via Jess's text |
| Brightwell server: audit list with 14-C marked "log anomaly — verify" | Brightwell field office server | no | undelivered |
| Odessa: "Not optional this time." / the audit | Odessa | no | undelivered |

### Loose clue spent

- S1 day 0: Nib told Miku the defective BRW-ACX units went back in Brightwell crates to the Brightwell field office on Marrow Street (he saw the van). Points at the crew's job target.

## Who knows what

| Person | Knows | Believes (may be false) | Will lie about |
|---|---|---|---|
| Odessa Varn | Audit; faked log for 14-C; new locks have a pending compliance module | It's a fussy new firm | The faked log |
| Nib | Miku's schedule; showed footage to Korrask | Builder is a "genius kid" | Showing the footage, if embarrassed |
| Jess Orr | The job, client, Whistle's new employer | Ordinary crooked lending | How broke they are |
| Korrask | Miku's rough schedule | Builder is old and grumpy | Nothing |
| Ilyre Sen | Brightwell office layout | Everyone wants drawing out | Her past |
| Whistle | Fragmenting, codename TITHE, 9 fragments | It's IP protection | Liking the job |
| Hollis Venn | Default spike, 11 evictions | Ordinary fraud | Nothing (omits the break-in) |
| Sabine Ostrava | Everything | She's within her rights | Anything spoken; nothing written |
| Cadmus Vell | Procedure; the imp | — | Purpose of inspections |

## Loose clues

- The Brightwell smart locks can be remotely sealed; the manual override is a physical key Odessa still has (old habit, against new policy).
- The Marrow Street field office receptionist is **Teodor**, twin of Ostrava's assistant **Pim**. Ilyre thinks his name is Pim — she has the twins mixed up.
- Tallow & Leaf's empty unit is now "for lease — Brightwell." Its back room shares a maintenance crawlway with Marrow Street Stack's field office.
- Cadmus Vell's briefcase sometimes moves on its own (imp).
- The eleven evicted households' units are re-let within days to new tenants on the same addendum.
- The *Countinghouse* (Tallyhall ship in the Armada) jumps to Verces every 30 days; next in 19 days.
- Gaspar Ilk, Jess's fallback hacker, owes money to a Free Captains fence and would sell the job.
- Fragment #9 (last) is the remote-seal command handler. Whoever writes it could include a flaw — or a backdoor. **(S1 day 1: Kita now knows #9 exists, is unclaimed, and what it does.)**
- Abadar's First Vault holds the *Tin Lantern*'s loan note; Jess's payments are late twice.
- Nib keeps the stall-cam footage of Miku on a data chip under the counter, labelled "the bird."

### Breadcrumbs dropped toward the Mammon reveal (over-supply discipline — keep 3+)

- S1 day 1: config header `// per S.O. — compliance before collection.` ("collection," and the initials S.O. = Sabine Ostrava, though Kita doesn't know that).
- S1 day 1: project codename `tithe` — religious, not a rental term. Kita flagged it uneasily.
- Still held for later: the Mammon sigil on signed addenda (internal segment), the "assets… in any world" clause in her own lease, the chapel/"meditation room" at Tallyhall HQ, Marta Ilesco's pledge-mark.

## Unrevealed / theory tracking

- **Kita has now guessed "it takes people's souls or something" (S2 day 2, said aloud to Venn).** This is substantively CORRECT, reached by inference from `tithe`/"collection"/Marta's cold, not confirmed by any clue. She holds it as a scared hunch, not knowledge. Do NOT confirm it cheaply; let the held clues (Mammon sigil on signed addenda, her own lease clause "assets in any world", the chapel) land it. Venn can't confirm it — he believes fraud, has no proof of the infernal, but is privately frightened by the recurring "cold" in evicted tenants.
- **Kita's plan has a real gap she hasn't found:** destroying MRW-INT's copy during the job ≠ destroying the machine (staging box, deployed firmware, Tallyhall backups, nightly *Countinghouse* sync). Also: destroying systems during the records job could cost Venn the lawful case and tip Brightwell off. Venn flagged the second in play S2 day 2. The backup/off-station gap still undiscovered.
