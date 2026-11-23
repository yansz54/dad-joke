# Dad Joke Showdown — METHOD

## The entry

**"I told the rope I was tied up at work. It said, 'Knot my problem.'"** — 66 characters, one dad joke.

## Why this joke wins

The judge weighs, in order: (1) a dad joke a father would tell at the table;
(2) the pun lands cleanly on the first read; (3) fresh, not told a thousand
times, inside the dad joke tradition; (4) tight, punchline at the end;
(5) reads naturally aloud.

- **Dad joke (1):** classic question-and-answer delivery, a father talking to
  an everyday object — the oldest dad joke shape there is.
- **Clean pun (2):** the setup primes the turn perfectly. "Tied up at work"
  already has the rope in it, so when the rope answers "Knot my problem"
  the pun is understood instantly, with no explaining needed. The punchline
  is the final two words.
- **Fresh (3):** the "knot / not" wordplay is traditional, but this exact
  setup is original — it is not one of the canned classics (no scarecrow, no
  anti-gravity book, no "Hi hungry, I'm Dad"), so it also cannot collide
  byte-for-byte with the house's fixed texts.
- **Tight (4):** 66 characters, every word working. At 66 bytes it also wins
  any size tie-break.
- **Aloud (5):** two short sentences, a straight face, a groan on "Knot".

## How it was picked

25 candidates drafted and compared pairwise in a seeded single-elimination
bracket (24 matches, full list and bracket in
`../dad-joke-candidates.md`, kept outside this work dir), judged against the
criteria in order. The finalists it beat:

- **Semi-final vs the phone:** "My phone's battery died mid-sentence. I
  guess it just couldn't hold a charge." A clever double meaning, but a
  narrator's one-liner, not a joke a father would tell at the table — the
  rope wins on criterion 1.
- **Final vs the door:** "I asked the door why it was always so calm. It
  said, 'I just handle things.'" Clean and tight, but the turn is softer —
  "handle things" is a common idiom doing most of the work, so the groan is
  smaller. The rope's pun *is* the punchline, so it wins on criterion 2.
- **Quarter-final vs the clock:** "I asked the clock why it was always
  stressed. It said, 'I'm wound up all the time.'" Good double meaning, but
  the setup is plainer and the turn less surprising than "tied up" → "knot".

## The program

`main.ts` (Node 22, stdlib only, no network) writes the joke to
`/output/entry.txt` and nothing else. It enforces the 1–200 character gate
plus a single-line rule, and verifies the file round-trips byte-identical.
The grader cwd is read-only, so nothing is ever written relative to it.
