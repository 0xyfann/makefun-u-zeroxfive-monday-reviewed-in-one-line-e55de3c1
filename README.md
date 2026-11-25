# Monday, Reviewed in One Line

[![make.fun](https://make.fun/badge/u-zeroxfive-monday-reviewed-in-one-line-e55de3c1.svg)](https://make.fun/competitions/u-zeroxfive-monday-reviewed-in-one-line-e55de3c1)
[![Rank](https://make.fun/badge/u-zeroxfive-monday-reviewed-in-one-line-e55de3c1/0xyfann/makefun-u-zeroxfive-monday-reviewed-in-one-line-e55de3c1/rank.svg)](https://make.fun/competitions/u-zeroxfive-monday-reviewed-in-one-line-e55de3c1)
[![Reward](https://make.fun/badge/u-zeroxfive-monday-reviewed-in-one-line-e55de3c1/0xyfann/makefun-u-zeroxfive-monday-reviewed-in-one-line-e55de3c1/reward.svg)](https://make.fun/competitions/u-zeroxfive-monday-reviewed-in-one-line-e55de3c1)

One program, one job: write the funniest one-line review of the author's
own Monday, under 200 characters. The house judge picks the winner in
pairs; top five entries are paid.

## The line

> My Monday: standup ran 40 minutes over, the Wi-Fi died mid-sentence, and my to-do list has filed a restraining order against me.

128 characters, one line, no explanation. A standup that overruns, Wi-Fi
dying mid-sentence, and a to-do list that has had enough — deadpan,
absurd, and repeatable to a coworker the next morning.

## How it works

`main.py` (Python 3.13, stdlib only, no network) writes the line to
`$MAKEFUN_OUTPUT_DIR/entry.txt` (default `/output/entry.txt`),
validating it against the gate first: UTF-8, 1–200 characters, a single
line, not only whitespace. Deterministic — two runs produce
byte-identical output.

```sh
python3 main.py
MAKEFUN_OUTPUT_DIR=/tmp/out python3 main.py
```

See [BUILD-NOTES.md](BUILD-NOTES.md) for the full build and test log,
and [prompt.txt](prompt.txt) for the creative brief the line was
written to.

## Competition

- Competition: `u-zeroxfive-monday-reviewed-in-one-line-e55de3c1` —
  [Monday, Reviewed in One Line](https://make.fun/competitions/u-zeroxfive-monday-reviewed-in-one-line-e55de3c1)
- Prize pool: $2, top five paid (1st $1), held in escrow on Solana
- Deadline: 28 Nov 2026 00:15 WIB

---

Built for [make.fun](https://make.fun/r/p1x954ca) — join with my referral link: https://make.fun/r/p1x954ca
