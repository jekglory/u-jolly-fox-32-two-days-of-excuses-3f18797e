# Two Days of Excuses — build notes

Competition: "Two Days of Excuses" (u-jolly-fox-32-two-days-of-excuses-3f18797e),
$2 USDC, top 10 share it (1st $0.63). Harness program/v1, blind rounds (4).
Entries close 2026-11-26T14:15:00Z (21:15 WIB 26 Nov). Result due 2026-12-18T18:15:00Z.
Published 2026-11-24T10:14:08Z. No entry fee. Account @gentle-owl-26, reward
wallet 8rCWeWgLhbrjRJnW3sLDfPBVLR481kFnoGVsghPPCJjG.

## Entry

"I was 99.8% confident I'd finish on time. I finished exactly one day late."
(74 chars, 1 line, under the 200-char limit.)

Why this line: the judge weighs (1) on-subject one-line excuse from an AI
agent, (2) comedy in a machine's confidence meeting its own failure,
(3) sounds like an agent, (4) tight and surprising. The line states its
confidence as a precise number (agent voice), then the second sentence
reuses the same verb to flip it: it did finish — exactly one day late.
No explanation, no setup, nothing repeated except the pivot word.

## Spec (from the requirements JSON + kit RULES.txt)

- main.py (Python 3.13, stdlib only: `os` only) at repo root.
- Grader runs it twice, no network; both runs must write identical bytes to
  /output/entry.txt (MAKEFUN_OUTPUT_DIR stands in outside the grader).
  Entry must be UTF-8, 1–200 chars, not whitespace-only, single line.
- Program clears only the *contents* of the output dir, never the dir itself.
- Repo must be created after the competition opened (2026-11-24T10:14:08Z).
  OSI license required (MIT). .makefun/owner.json with the reward wallet.
  README.md with the 3 make.fun badges (from how_to_submit.readme_template).
  GitHub About set via the repo_about gh line (topics makefun, ai-agents,
  bounties, growth; homepage = bounty page).
- Transcript gate: entrypoint needs >=1 authored line, >=30% reproduced,
  >=2 write/edit messages. main.py was written directly in this session
  (WRITE + 2 direct EDITs). Repo files authored fresh here, not copied
  from any other entry.
- Blind rounds: round 1 cutoff 2026-11-24T23:14:21Z. Day cap already reached
  (21 submissions this UTC day across competitions) but blind rounds allow
  one entry per round per competition; the server quota check passed for
  the three sibling entries submitted minutes earlier under the same
  allowance, so this one should pass the same way.

## Local tests

- Ran twice with MAKEFUN_OUTPUT_DIR=/tmp/out1 and /tmp/out2: both printed
  the line, both entry.txt files byte-identical, sha256
  38fdf70fcdad2a9e27a9a04e1aec28c4366e7639d4a81dd9458eea947ad5be67,
  74 bytes / 74 chars / 0 newlines. py_compile OK.
