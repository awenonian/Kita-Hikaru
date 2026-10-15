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

## Session 1 — day 1, morning, 14-C

- Kita's reasoning: the crew's job "doesn't exactly sound like honest work, but everyone knows some corporations deserve it." Specwork keeps clients anonymous, but "if it's obvious that the contract is for one of the Asmodean corps, she'll turn it down." So: who's the target, what's the job.
- Typed "What corp?" to Jess's comm code. Sat on it an hour, window on second monitor, watching a stream by vtuber **Juniper Vex** (avatar by Lolo — the one that made Kita want her own). Hit send without thinking, eyes straight back to the stream.
- Jess replied within minutes (see below).
- Kita, privately: Brightwell — she lives in a Brightwell building AND is (presumably) writing a contract for them. Evictions are bad; she has nowhere else to go. Replied: "Yeah. How sure are they?"
- Jess: "Sure enough to pay us." Then: defaults in Brightwell's Spindle Cross buildings up about nine times in four months; eleven households out; every filing says the same thing — failed inspection compliance. "Rest of it I tell in person. Not over comm."

## Session 1 — day 1, ~0820, remote recon of Brightwell

- Kita rethinks the letter: if Brightwell is bad news she won't help them. Decides to probe their field office remotely instead — "white hat then, for the bug bounty, but this isn't that different." VPN, ssh to external pod.
- Player note: prefers fail-forward (a failed Hack = learns something / bounces off, not "they're hunting you" except maybe on a crit fail); no real time pressure here.
- **Recon roll: 27 (nat 20, +7) — critical success.** Clean, no trace.
  - Found: Brightwell's public tenant portal + a sloppily-exposed staging/build box. The lease-processing records the crew wants are NOT reachable — they live on an internal segment (`MRW-INT`) with no route from outside. (This is why the job needs someone physically on-site. Fail-forward on "do it remotely": she can't, and now knows why.)
  - On the staging box: the firmware build project. **Nine** `BRW-ACX/compliance/*` modules, each a separate anonymous contract. Hers (the REFUSAL_LOGGED → ComplianceRecord handler) is one of them. Repo path codename: **tithe**.
  - She can read the code wiring: a `ComplianceRecord` with high enough `severity` feeds a routine that files an automated tenant **default event**. I.e. her handler is a cog in the eviction machine.
  - Bonus (crit): she pulls the **full interface specs** for her own contract off the staging box. She can now finish fragment #6 cleanly — the 60 cr rent money is hers if she wants it.
- **Dilemma now live:** finishing the contract pays rent but feeds evictions in her own building.
- Kita reads the other modules (observation she can make, crit access, no roll):
  - All nine contracts were posted stub-only. Hers wasn't a mistake — the compartmentalization is uniform and deliberate: no single contractor sees more than one piece.
  - The nine assemble into a pipeline: (1) ingest access events, (2) her REFUSAL_LOGGED→ComplianceRecord handler, (3) severity scoring, (4) default-event filing, (5) notice generation, (6) schedule/lock the unit, (7) audit log, (8) tenant-portal status, (9) remote-seal command handler — the piece that can throw a unit's bolt remotely. #9 is unclaimed and unfinished.
  - The repo folder is `tithe`. A top-level config file has an author tag she doesn't recognize and a one-line header comment: `// per S.O. — compliance before collection.` ("collection," not "eviction." And "tithe." Kita noted both, uneasy, didn't interpret.)
- Messaged Jess: "When? Where? Can my drone proxy?"
- Jess: drone's fine — "I'm hiring your hands, not your face." Picked neutral ground: a shuttered noodle counter off the Arms concourse, Berth Row, tonight 2000. "Advance's twenty if you make it worth meeting. Bring what you can do, not promises." Won't say more over comm.
- Kita finished the handler code using the real specs — did NOT submit it. Left it done but unsent.
- Kita makes a burner Specwork account to claim fragment #9 (the remote-seal capstone) and deny it to the real builders for the hold period.
- Oracle: is #9 posted/claimable now? **YES, AND** (4 vs unlikely) — not only posted but *pushed*: bumped to the top of the board, flagged urgent, pay conspicuously high (listed 200 cr vs her 60). They want the capstone finished fast.
- She claims it on the burner (no roll — unpressured, within her skill). #9 is now held to her alt for its deadline window (4 days); no one else can build it in that window. She reads the urgency as its own tell.

## Session 1 — day 1, daytime prep + the notice

- Kita's plan (stated): take Brightwell's money by submitting the modules, then delete the finished programs from the inside during the crew's break-in. "The only thing better than leaving them unfinished would be taking their money AND leaving them unfinished." Not a crusader, but happy to put her mark on the world as Good winning in small ways — IF "tithe"/"collection" prove as bad as they sound.
  - *(GM note: her plan assumes the crew's target system is where the programs live, and that deleting source removes the threat. The field-office job does reach the internal segment; but deployed lock firmware ≠ source, and corps keep backups. Let this be discoverable in play, not sprung.)*
- Wrote fragment #9 (the remote-seal capstone) to completion on the burner side. Did NOT submit. Genuinely good work.
- Captured findings to a spare datachip (reused Korrask's, to return it): network structure, the isolated MRW-INT server (referenced, no external route), the 9-task pipeline, the `tithe`/"collection" wording, plus her own assessment. Stowed in Miku.
- Wrote a letter to hand the crew first (to carry the meeting on yes/no after):
  > Hello, / I scoped out the system. Findings are attached. / This is Miku. I'm sorry about not being there, but I'm nervous about meeting in person. / The corp sounds like it's probably bad news, but I would like to know how bad it is, if you know anything. / Kita
- **Midday: Odessa's inspection notice arrives** (see below) — carrying the tamper flag from yesterday's failed hack.

## Session 1 — day 1, 2000, the meet (Berth Row)
- Miku described: modified low-noise quadcopter, sleek light-blue, non-glowing, pristine hidden wiring; flies the low drone lanes, screen blanked in transit.
- Scene altered (oracle): Jess hedged and called a backup hacker too — **Gaspar Ilk** (wiry human, cheap deck, chip on shoulder) showed up uninvited-feeling and is openly dismissive of "a flying camera." Jess didn't expect both at once. Crew present: Jess, Korrask, Ilyre, + Ilk.
- Miku arrived, screen blank; on Ilyre's greeting Kita flipped it to `:)`.
- Kita typed `yes`, took the 20 cr credstick into Miku's hatch. Jess laid out the job: records are on the internal box (no outside route), so someone must be physically in the Brightwell field office, Marrow Street Stack ground floor, jacked in — Miku goes where a person can't. Ilyre gets them through the front; Korrask + Jess handle bodies; Kita/Miku does the data pull. Run is "a few nights out"; Jess will send the when/way after one more walkthrough, and wants to know what Miku should carry.
- Jess, leaving: "Whatever your name is. Thanks for being there. Most people aren't."
- **Session 1 ends here.** Miku flown home with 20 cr, the findings chip, and the job.

<!-- Session 2 begins here. -->

## Session 2 — day 2 (Sunday), morning, 14-C

- Player's recap: "Last time Kita picked up a coding contract, and was later contacted by a crew planning a data heist. It turns out their target was a company doing some shady things, which happened to be both the company that posted her coding contract, and the one that owns her apartment! She decided to scope out their network, and found some sinister looking stuff, so she joined the crew, and has a plan to take a little more of the company's money while she's at it." (Matches the notes.)
- Opening (oracle interrupted the expected scene — "situation improves; arrive / sickness"): Harrow-Dyne Logistics' Dario Pell writes. He was in medbay a week; the cancellation was Specwork's auto-lapse. Withdrawn; **25 cr paid in full.** He liked the work, asks about the follow-up phase. Credits 21 → 46.
- Kita reviewed #6 and #9: both finished, both pass her harness. Player asked OOC how Specwork payment works; told: submission → tests → client review (up to 3 days; this client likely hours) → escrow release. #6 due Wednesday end of day. Burner payouts held until Tallyhall identity verification. Burner's #9 hold lapses Wednesday.
- Kita built a deliberate, honest-looking flaw into #6 (a specially-made card makes a unit's refusal tally stop counting toward defaults). Saved the card profile separately. Idea: leak it later so tenants can protect their own doors. #9 left clean. No roll yet — review roll at submission.
- Kita weighed how to get paid for #9 without her name on the burner (her own name; a middleman — Nib, the crew, the Abadaran priest; deleting her main account first). Society 16 (success): Tallyhall keeps identity records of closed accounts and Specwork forbids multiple accounts per identity → verifying the burner links it to her and triggers account review. Undecided.
- ~1500: burner gets a message from the anonymous client on #9 — ETA?, +50 cr bonus if delivered by end of day tomorrow (Monday), "the people upstairs are Very Keen", stubs thin "security-compartment thing", signed "thx! —T". Kita flinched at the notification.
- ~1700, First Vault, Vault Row. Kita sent Miku to see the Abadaran priest (Hollis Venn) for advice in a crisis — autopiloted so she couldn't chicken out. Note: "Sorry, father, can we speak in private?"
- Scene altered (oracle): Venn wasn't alone — tending **Marta Ilesco**, evicted from a Marrow Street Brightwell building ~2 months ago. Kita chose "I'll wait." Witnessed (observation only): Marta paid rent every month, had receipts; the default came from a missed→rescheduled inspection logged as a refusal; "they were very polite"; she signed the 40-page addendum unread ("everybody signs it"); her daughter read some of it and went quiet; and — "I've been cold since. Right here [breastbone]. Can't get warm since I signed out of that place." Venn's face flickered and closed. (Pledge-mark NOT revealed as such — Miku has no magic sense; played as a tired woman's aside.)
- **FIRST TIME KITA SPOKE ALOUD IN PLAY.** Pressed unmute, long freeze, then broken speech. Got out, haltingly, with Venn gently drawing it: she knows Jess; you're not supposed to find your own clients and she did; she has two coding contracts and they're bad; she thinks she knows why Marta is cold; her contracts + Marta's eviction are the same machine; she works via Specwork, owned by the same company that owns Marta's building AND hers — so she may have already helped do this before.
- **Venn revealed he is the crew's client** ("The crew you've joined is working for me"), moved by the coincidence; keeps her confession in confidence (house of Abadar).
- Kita, still quiet, asked her real questions aloud: she needs an answer today, things happen soon. Said the code "takes people's *souls* or something." Confessed she wrote a disable-loophole into one contract — "not honest, not a fair trade" — unsubmitted; framed the dilemma: refuse (someone else builds it clean) vs submit (she profits off an evil thing but it's sabotaged). And: during Jess's job she could take the whole system down, not just pull files — "Isn't that good? Isn't it right? Isn't it ok if I take a couple hundred of their credits before I do that?" "It feels wrong still, I think. But I don't know why."
- Leaving, Kita: "Thank you for your time, father. We'll get you the records." Flew Miku home. Privately rejected Venn's "the numbers are how they get you" — she's a programmer; numbers are how she thinks. Resolved on a *third* path: don't profit (route the money to Venn's church somehow), but don't just hand them clean work either — submit poisoned work that looks done so they don't reassign it, with sabotage fine enough to survive even a later look.
- **Re-infiltration of Brightwell's staging box (day 2 night)** to pull the acceptance tests. Computers 12 vs 16 — FAILURE (fail-forward): got the full 9-module test suite, BUT (a) logging is now ON — her session left a faint, un-alarmed authentication record (yesterday's crit left none); a latent smudge if anyone ever audits who touched the box pre-deployment; (b) the sloppy external exposure is being tidied, closing within a day or two → records job really must be on-site Wednesday.
- **All-nighter sabotage (into day 3 morning):**
  - **#6: fully succeeds.** Reworked the flaw to read as honest tired code; passes all tests; innocent function-by-function and whole. Kita confident, justifiably. Done.
  - **#9: FAILURE (Computers 12 vs 18).** The elegant delayed-confluence / floating-point-drift time-bomb (dream: flip unit status to "owned, paid in full") is past her tonight. She has a version that passes tests but she can SEE the seams: (1) traceable back toward its author under a careful post-incident forensic audit; (2) the 6-week real-drift trigger is untestable on her bench — might fire as designed, early, or never. Options she's aware of: submit #9 clean (works, undetectable, builds their capstone), submit the seamed bomb (gamble), or keep grinding over days (each systems trip now leaves a smudge; clock to Wednesday).
- Kita wept at the end of the all-nighter — she'd seen the version that only helped and couldn't build it; "wanting it wasn't enough." Edited the burner reply to T: cut the line about getting it done, replaced with **"I'll do what I can"**, and sent it. Replied late to Jess on gear: **"Miku shouldn't need anything"** (not much thought; she wasn't in a state to). Threw spare cables into Miku's storage to jack into the machine on-site. Crashed into bed in a spiral — "Why would she ever think she could? It was obviously stupid of her to hope." No alarm set; slept too deep for notifications.
- **Scene altered (oracle, chaos 4): she overslept, hard.** Not an evening — a full blackout. She wakes **mid-day on day 4 (Tuesday)**, ~30 hours gone, groggy and wrung out, having lost the better part of two days. While she was under, the world moved (see messages).
