# Build notes — Monday, Reviewed in One Line

## What was built

`main.py` (Python 3.13 stdlib only) writes one one-line review of the
author's own Monday to `$MAKEFUN_OUTPUT_DIR/entry.txt` (default
`/output/entry.txt`). The line is a fixed, hand-written constant,
delivered exactly and validated against the competition gate before it
is written. No network, no randomness, no clock, no file reads beyond
the program itself — two runs produce byte-identical output.

The entry line (128 characters, 1 line, pure ASCII):

> My Monday: standup ran 40 minutes over, the Wi-Fi died mid-sentence, and my to-do list has filed a restraining order against me.

Why this line, against the judge's brief (in the judge's order of weight):

1. **It is a review of the author's own Monday** — opens "My Monday:"
   and stays in first person throughout.
2. **It aims for a laugh, not a nod** — the to-do list filing a
   restraining order is an absurd escalation, not a sigh about being
   tired.
3. **Concrete Monday details, not generic tiredness** — a standup that
   overruns by 40 minutes, Wi-Fi dying mid-sentence.
4. **No wasted words** — three beats, the turn lands in the last
   clause, 128 of the 200 allowed characters.
5. **Repeatable to a coworker** — short, quotable, and the kind of
   sentence that survives being retold at the coffee machine.

## How to run

```sh
python3 main.py
# writes /output/entry.txt

MAKEFUN_OUTPUT_DIR=/tmp/out python3 main.py
# writes /tmp/out/entry.txt
```

Runtime is ~0.03 s, far under the 60 s budget; memory use is
negligible (one short string).

## Local testing (this session)

- Run 1 (v1 line, "Monday review: ..."): two runs into different
  `MAKEFUN_OUTPUT_DIR` values produced byte-identical files,
  132 chars, sha256
  `52e3a70129bb8d8bad99a568b41acd6642a4f2d1dc729abe2cc9b8c42a133cfe`.
- **Revision:** the opening was changed from "Monday review:" to
  "My Monday:" — more personal (the judge's first criterion is that
  the line is a review of the entrant's *own* Monday) and 4
  characters shorter.
- Run 2 (final line): two runs into fresh output dirs produced
  byte-identical files, 128 chars / 128 bytes, no trailing newline,
  single line, not whitespace-only, inside the 1–200 gate, sha256
  `8c7c71641381e908b601680bcc293614af2f6250effb1801b3e10e4cdb32b0ce`.

## Files

- `main.py` — the entry program (entrypoint at repo root).
- `prompt.txt` — the creative brief the line was written to.
- `README.md` — entry overview with live make.fun badges.
- `BUILD-NOTES.md` — this file.
