# Week 3 Assignment — Pitch, Review, Proposal Part B

**Due:** lab part pushed by the last push of the lecture (11:50) · the rest Saturday 23:59 · Commit to your project repository

> **Before the lecture:** your `PITCH_03.md` must be written and pushed. The first hour
> of the lecture is spent presenting it — there is no time to write it then. Bring your
> laptop charged; you present from it.

Last week you decided what to build. This week three classmates tell you what they
think of it, you decide what to change, and you write the second half of the proposal —
the half that says why it is worth building and what could stop you.

---

## What arrives with this week

Run the checker once:

```bash
python .github/check_deliverables.py
```

It brings `week03/PITCH_03.md`, `week03/contributors_03.json` and `week03/ai_log_03.md`.
`PROPOSAL.md` you already have; Part B (§8–§12) and the Change log are in it, waiting.

---

## Before the lecture — `week03/PITCH_03.md`

Your five-minute pitch, six slides, in Markdown: the file **is** the deck, every `---`
is a new slide. Open it in VS Code; the **Marp for VS Code** extension shows it as
slides (preview button, top right) and exports PDF or PPTX if you want one. Without the
extension, VS Code's normal Markdown preview is enough to present from.

The six slides, each with its own instructions inside the file:

1. the product in one sentence;
2. **the last time the problem happened** — to you, or in front of you — date, place, who, what they did instead;
3. **five real people who will test it in Week 9** — name, how you know them;
4. three things it does, one thing it does not;
5. the main screen, **drawn by hand** (photo in `week03/`) or in text;
6. the one thing you are not sure about.

Slide 7 is fixed: the three questions your reviewers answer.

**Write it yourself — no AI for this file.** Not the text, not the structure. Everything
on these slides is about your life and your people; an assistant cannot know it, and I
will ask about any slide, in the group or in class. The rest of the week's work is
different: AI is a tool there, as before, and `ai_log_03.md` asks you to use it.

Two rules behind slides 2 and 3, and they stay for the whole term: **the project solves
a problem of yours — your own, your friends' at the university, or your social
circle's**, and **it is usable by real people around you** — at Atlas, in your family, in
a club — because in Week 9 those people test it, and you will need them. If you cannot
name the last time the problem happened, or five people who would use the product, the
problem is with the project, not the slide: change the project now, this is the last
cheap week to do it.

---

## In the lab — pushed by 11:50

### 1. Review round — groups of four, first hour

You form a group of four yourselves, at the start of the lecture; a student with no repository yet joins a group of three. Each person presents for five minutes from their own
laptop; the other three listen, then **write** one sentence for each of the three
questions on slide 7 — on paper or in a text file, handed to the presenter. Four rounds,
about 45 minutes. Say what you think; a polite "it is good" helps nobody and earns nobody
anything.

**This group is your group for the rest of the term.** From Week 4 the four of you meet
**online for one hour every week, between the lecture and Saturday** — Teams, Meet,
Discord, whatever you like — and each of you presents what changed in your project that
week; the other three say what they think. The three entries in your
`weekNN/contributors_NN.json` come from that meeting from then on: who said what, quoted,
and what you did about it. Nobody can write those three entries for someone who was not
there, so missing the meeting shows by itself. You may hold the first one this week
already.

### 2. `week03/contributors_03.json` — three reviewers

Your three reviewers, role `reviewer`, student numbers, and for each **the most useful
sentence they wrote** — quoted, not summarised. Then `accepted: true` or `false`, and
`why`. Rejecting advice with a reason is fine; accepting everything without a trace of
what changed is not. Each reviewer you name earns the contributors' bonus, as last week.

### 3. `PROPOSAL.md` — Part A revised, Change log started

Go back over §1–§7 with the three answers in front of you and change what the review
changed. Every change gets **one dated line in the Change log** at the end of the file:
what changed, in which section, why — "2026-10-07 — §4: dropped group chat; two
reviewers said nobody would use it next to WhatsApp". A proposal is allowed to change;
it is not allowed to change silently.

`requirements.json` may change this week too — add, drop (keep the id, set
`"dropped": true`), reword. **From Saturday the ids are frozen** for the rest of the term.

### 4. Push

```bash
python .github/check_deliverables.py
git add .
git commit -m "week03: pitch, review, proposal revised"
git push
```

Push after the review round, and again at the last push of the lecture, **11:50** — the usual 10:00 / 11:00 / 11:50. Right after it I freeze every repository. What is not pushed does not exist.

---

## By Saturday 23:59

### 5. `PROPOSAL.md` — Part B, §8–§12

The half that says why it is worth building. Each section has a WHY, a WHAT and a
weak/strong pair inside the file; the StudyRoom examples continue.

- **§8 Market and target users** — who, how many, how you know. Your five testers from
  slide 3 are the first row of this section.
- **§9 Competitors** — three things that solve the problem today; a paper list counts.
- **§10 Comparison and your advantage** — a small table, the user's criteria, one sentence.
- **§11 Commercial potential** — how it pays for itself; "no commercial intent, the value
  is X" is an honest answer if you argue it.
- **§12 Technical risks** — three things most likely to stop you by Week 11, with a plan
  and a fallback each. **The store you choose (S0)** is named here, with its fee and its
  review or test-track time: read `AI_PLATFORMS_AND_STORES_EN.md` before you decide.

### 6. Use AI as a hostile reviewer — `week03/ai_log_03.md`

This week the assistant plays the investor who wants to say no. Give it your Part B and
ask for the three strongest objections. Then **answer one of them in the proposal** and
**show one objection to be wrong** — with evidence: a number, a source, a thing you
checked. Paste the exchange. A log that says "it gave useful feedback" earns nothing.

### 7. Push again, checks green

Commits spread over the week, messages that say what changed. Everything the checker
asks for is listed below.

---

## Deliverables checklist

**Before the lecture**
- [ ] `week03/PITCH_03.md` — six slides filled, written by you, pushed

**In the lab, by 11:50**
- [ ] `week03/contributors_03.json` — three reviewers, a quoted sentence each, accepted/why
- [ ] `PROPOSAL.md` §1–§7 revised where the review changed them
- [ ] `PROPOSAL.md` Change log — at least one dated line

**By Saturday**
- [ ] `PROPOSAL.md` §8–§12 filled; §12 names the store, its fee and its review time
- [ ] `week03/ai_log_03.md` — three objections, one answered in the proposal, one shown wrong, exchange pasted
- [ ] `requirements.json` final — ids frozen from here
- [ ] Checks green on GitHub; Weeks 1–2 still pass

---

## Not this week

No code, no design documents yet (Week 4), no environment set-up. Do not start the store
account; naming the store in §12 is enough.

---

## How this week is graded

**End of the lecture — 5 points.** Pitch pushed and complete, three reviewers with real
sentences, Change log started — read from your repository as it stands at the 11:50 push.

**Saturday 23:59 — 5 points.** Checks green on your final state: **2**. Human
involvement: **2** — your `ai_log_03.md` with its evidence, and reviews with real
sentences and real decisions behind them. Commit discipline: **1** — commits spread
over the week, with real progress between them.

**Contributors' bonus.** Each reviewer you name earns 10% of your week's mark; you earn
the same for the reviews you give. From Week 4 the names are your group.

**One student, one computer, one GitHub account.** Work done on a classmate's machine or
under a classmate's session earns nothing for the lecture.
