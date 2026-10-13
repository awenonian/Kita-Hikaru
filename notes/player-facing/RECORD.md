# Record

What happened, in play order. Append as you go — small bits during play, not a
write-up at the end. Never tidy it; the mess is the point.

Only what came from play goes here. If you're filling a gap with something
plausible, you've stopped recording and started inventing.

Quote the player rather than describing them. "I'd rather not say" is worth
more than *declined to answer*.

---

<!-- Session 1 begins here. -->

## Session 1 — day 0, morning, 14-C

- Opened in 14-C: rent reminder (30 cr, 9 days, "a Tallyhall Financial company"), balance 1 cr, Harrow-Dyne contract cancelled unpaid last week. New Specwork job in queue: access-controller event handler, 60 cr, 4-day deadline, stub interfaces `BRW-ACX/compliance/ingest`, event `REFUSAL_LOGGED`. Miku charged; Sump run due tonight.
- Kita: "Let's look at the contract. Miku's run can be put off for now, probably. If I can get the contract done, then that's one less source of stress while I'm making the parts list." Searches the interface names on the infosphere — "maybe they're some standard I haven't found before." No roll (ordinary search, unpressured).
- Found: no standard. A Brightwell tenant FAQ page for the "BRW-ACX Smart Access" lock, "compliance features coming soon"; photo matches the lock fitted on her own door last month.
- Kita: "Oh! Well that's easy! I can just wire into the one on my door to pull down the code and decompile it to get the interfaces! I'm... probably not supposed to do that." Reasoning: read-only, nobody gets flak over an inadequate spec — "This really does seem like the best course of action all around."
- **Accepted the contract** (TITHE fragment #6, 60 cr, 4 days). Clicked through Specwork's standard contractor NDA.
- Opened the lock's interior housing (no roll). Found a service header. Hack pending — stakes stated, player choosing roll vs Assurance.
- Hack roll: 14 (d20 7 +7) vs DC 16 — **failure.** Lock reported a tamper event upstream to Brightwell. No firmware obtained. Player, before rolling: "If it does alert Brightwell, I'll just have to pack it back up, and hope that no one thinks that it's likely I was trying to break into my own room from the inside..."
- Kita put the lock back together ("Hopefully 'No action required' means no action will be taken..."). Looked at the board first. Added "BRW-ACX" to Nib's list, no alternative, plus a held-back note describing the board. Finished the gimbal list. Sent Miku to the Sump, camera on second monitor; meanwhile scaffolded the handler from the stubs, designed so adding a field or transform later is a small change. (No roll — ordinary work.)
- Oracle: does Nib have a BRW-ACX? **No** (87 vs likely). Nib: Brightwell's fitters took back every dud unit, counted out of the bins.
- At the stall: a large vesk on a crate (Korrask) has been watching the lift exits. She recognises Miku.
- Korrask: (in Vesk, to Nib) "That's the one? The one with the still head?" Then to Miku, Common: "YOU. Little one. Who *builds* you?"
- Kita froze, then swung Miku behind Nib, facing the vesk at a distance; LED went blank. Then lowered to face Nib: LED "who?"
- Korrask laughed — read the dodge as good reflexes. Nib: she's Korrask, engineer off a freighter in the Arms, been sitting on his crate two nights waiting. Korrask said the still-head stabiliser is "stupid-hard" and she knows it; her captain has a job that needs a hacker. Held out a comm-code chip: Jess Orr, *Tin Lantern*, Dock 9.
- Miku rose to face Korrask; LED "OK", then "...". Took the chip, stowed it with the board description.
- Oracle: Korrask stays? **No** (73 vs even). She left, satisfied.
- Kita hesitated — wants to answer Nib, afraid to use speakers (used only for canned chirps, an "excuse me"). LED to Nib: "job", then "spec".
- Nib: duds from the lock install went back in Brightwell crates to their field office on Marrow Street — he saw the van. "Careful. Brightwell counts their scrap." Rang up the gimbal parts: 6 cr. Kita has 1.
- Kita facepalms — that's why she'd been delaying the shopping. LED: "um...", "hold?", "1c :(". (Player: she may need to program a marquee; the screen holds ~7 characters.)
- Nib holds the parts for regulars: **3 days**, under the counter, then back on the pegboard. Miku flew home.
- Plan C (Kita): print the contract (task #, ask, her handle — public info only), circle "Strict interface compliance required" and "Interfaces provided as stubs only" in red, write "full details required?", underline her handle, fold, label "Specwork Contract", send Miku to the Brightwell field office on Marrow Street. "Someone else looking in might find this over complicated compared to just sending an email, but… this feels less personal."
- Rechecked the Specwork inbox (obsessively): nothing beyond the original stubs. Specwork listing shows client as "Verified Client (anonymous)".
- Field office hours: 0900–1700 station time. Tomorrow.
- Evening: scaffolding continued; programmed a marquee mode for Miku's LED (scrolls text 7 chars at a time). No roll.
- Opened Korrask's chip on a separate air-gapped device: clean. A comm code and a short recorded message from Jess Orr (audio only).
