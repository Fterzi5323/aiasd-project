# AIASD · Week 3 — Pitch, Review, Proposal Part B

*Atlas University · Fall 2026–27 · Prof. Dr. Vedat Coşkun*
*Presented from this page. Scroll one section at a time; each `---` is a slide.*

<!-- Instructor: zoom the browser to 150 % and collapse the GitHub header (press "." for
the editor view if you prefer a cleaner page). Timings in the notes. Total ≈ 3 h:
10 min intro · 50 min review round · 10 min after the round · work until 12:00 · 13:00 freeze. -->

---

## Today

1. Week 2 — how it went
2. Two rules that stay for the whole term
3. What a pitch is, and why you wrote one
4. The review round — groups of four, first hour
5. After the round: three reviewers, a revised proposal, a change log
6. By Saturday: Part B, the store, the hostile reviewer
7. How the week is graded

---

## Week 2 in numbers

| | English | Turkish |
|---|---|---|
| Registered | 79 | 33 |
| Pushed during the lecture | 63 | 26 |
| Lecture slot 5 / 5 | — | — |
| Saturday: checks all green | — | — |

<!-- Fill the last two rows on Sunday from week02.xlsx before pushing the deck. -->

Marks and the checker's remarks reached you as an **issue in your own repository** on
Sunday. Questions about a mark go there, as a comment — not by e-mail.

---

## Two rules that stay for the whole term

**1. The project solves a problem *you* have.**
Not "students struggle with X". The last time it happened to you: date, place, what you
did instead.

**2. Real people around you can use it.**
At Atlas, in your family, in a club. In Week 9 five of them test it — the User
Acceptance Test. You name them today.

If you cannot name the last time, or the five people: the problem is the project, not
the slide. **Change the project this week.** It is the last cheap week to do it.

---

## What a pitch is

A pitch is a short, ordered, concrete case for an idea, made to someone who decides
something — money, time, a yes.

- **Short**, because attention is the scarce resource.
- **Ordered**: problem → solution → who → why you → what you ask.
- **Concrete**: numbers, names, one example. Adjectives are not evidence.

> "An innovative platform for everyone" is not a pitch.
> "3,000 students use the Atlas library each term; one in six walks away without a room;
> StudyRoom shows the free one and books it in 30 seconds" is.

---

## The same thing, with 2.5 million euros behind it

**EIC Accelerator** — the European Union's grant for start-ups (Horizon Europe).

Step 1 of the application is exactly this: a **pitch deck of at most 10 slides**, a
**3-minute video**, a short form. Hundreds of applications are filtered on those three
things. The ten slides: problem · solution · why now · market with numbers · competitors
and your edge · business model · roadmap and risks · team · the ask · next step.

Your six slides today are the first half of that list. Part B of the proposal, due
Saturday, is the second half. The December defence is a small jury.

---

## Your six slides — `week03/PITCH_03.md`

1. The product in one sentence
2. **The last time it happened to you**
3. **Five people who will test it in Week 9** — name, how you know them, why
4. Three requirements — *the same id and text as `requirements.json`* — and one "does not"
5. The main screen, **drawn by hand**
6. The one thing you are not sure about

Slide 7 is fixed: the three questions your reviewers answer.

**Written by you, no AI.** Everything on it is your life and your people. I will ask
about any slide.

---

## Presenting from your laptop

Open `week03/PITCH_03.md` in VS Code.

- With the **Marp for VS Code** extension: the preview button (top right) shows slides;
  the same button exports PDF or PPTX.
- Without it: VS Code's normal Markdown preview (`⌘⇧V` / `Ctrl+Shift+V`) — scroll one
  slide at a time. Good enough.
- Not from GitHub's website: you will edit the file after the round.

<!-- Show both on the projector with the test student's PITCH_03.md: Marp preview, then
plain preview. 2 minutes. -->

---

## The review round — groups of four

**Groups are on the projector now. Find your nickname.** No repository yet? Join a
group of three near you and see me after the round.

Each person: **5 minutes** presenting, from your own laptop. The other three listen,
then **write** one sentence for each of the three questions and hand it over — paper or a
text file. Then the next person. Four rounds, about **45 minutes**.

Reviewers: say what you think. "It's good" helps nobody and earns nobody anything.

<!-- Project grades/out/week03-groups-en.html. Walk around. Ring at 12-minute marks. -->

---

## The three questions — slide 7

1. **Real?** Did they convince you this problem happens to them, and to the five people
   on slide 3?
2. **Usable here?** Could those five people actually use this in Week 9 — what would
   stop them?
3. **Too much or too little?** Which part will not be finished by Week 11 — or has the
   product shrunk to one screen?

One sentence each. The presenter copies your sentences into their repository — your name
goes next to them, and you earn the contributors' bonus for them.

---

## After the round — before 13:00

**`week03/contributors_03.json`** — your three reviewers, role `reviewer`, student
numbers, and for each **the most useful sentence they wrote, quoted**. Then
`accepted: true/false` and `why`. Rejecting with a reason is fine; "they said, I changed"
with nothing behind it is not.

**`PROPOSAL.md`** — go over §1–§7 with the three answers in front of you. Every change
gets **one dated line in the Change log** at the end of the file:

`2026-10-06 — §4: dropped group chat; two reviewers said nobody would use it next to WhatsApp.`

A proposal may change. It may not change silently.

---

## Requirements — last week to move them

`requirements.json` may still change today: add, reword, drop (keep the id, set
`"dropped": true`).

**From Saturday the ids are frozen** for the rest of the term. Design, tests and the
traceability matrix will point at `REQ-004`; it has to mean the same thing in December.

REQ-001 (e-mail-code login) and REQ-006 (390 px phone screen) stay as they are for
everyone — three of you changed them last week and have an issue about it.

---

## Push

```bash
python .github/check_deliverables.py
git add .
git commit -m "week03: pitch, review, proposal revised"
git push
```

Push after the round, and again before **13:00**. The checker reads your repository as it
stands at 13:00. What is not pushed does not exist.

Push times this term: **10:00, 11:00, 11:50** — and whenever you finish something.

---

## By Saturday 23:59 — Part B, §8–§12

The half that says why it is worth building. WHY / WHAT / weak / strong inside each
section of `PROPOSAL.md`.

- **§8 Market** — who, how many, how you know. Your five testers are the first row.
- **§9 Competitors** — three things that solve it today. A paper list counts.
- **§10 Comparison** — a small table on the *user's* criteria, one sentence.
- **§11 Commercial potential** — how it pays for itself; "no commercial intent, the value
  is X" is honest if argued.
- **§12 Risks** — three things that stop you by Week 11, plan and fallback each. **Name the
  store** (S0): fee, review time. Read `AI_PLATFORMS_AND_STORES_EN.md` first.

---

## By Saturday — the hostile reviewer, `week03/ai_log_03.md`

This week the assistant plays the investor who wants to say **no**.

1. Give it your Part B. Ask for the three strongest objections, specific to your proposal.
2. One objection is **right**: answer it in the proposal, log it in the Change log.
3. One is **wrong**: show why — a number, a source, a thing you checked.
4. Paste the exchange.

"It gave useful feedback" earns nothing. Telling a good objection from a bad one is the
skill.

---

## How Week 3 is graded — 10 points

| | Points | What |
|---|---|---|
| End of lecture, 13:00 | 5 | pitch complete, three reviewers with real sentences, change log started |
| Saturday checker | 2 | §8–§12 filled, store named, ai_log with three objections |
| Human involvement | 2 | the ai_log and its evidence; reviews with real decisions behind them |
| Commit discipline | 1 | **awarded at the Week 5 review** of your whole push history |

Contributors' bonus: each reviewer you name earns 10 % of your week's mark; so do you,
for the reviews you give.

---

## Two rules about the room

**One student, one computer, one GitHub account.** Work done on a classmate's machine or
under a classmate's session earns nothing for the lecture. Bring your laptop charged.

**Not registered in the attendance system = absent.** The lecture slot's five points are
then gone, whatever was pushed.

---

## Now

Groups are on the screen. Laptops open, `PITCH_03.md` in the preview.

**First presenter in each group: start.**

<!-- Start the clock. Walk around. After the round: slide "After the round" stays on the
projector until 12:00; "Push" from 12:00. Freeze at 13:00: push.md block 3. -->
