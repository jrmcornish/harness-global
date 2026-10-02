# Backlog

Candidates for global skills. Each entry says where the need was seen.
Nothing here is built until Rob picks it.

## 1. Move a Claude Code conversation to another folder

**Status:** first global skill to create, once the meta harness exists (it is
to be made with Capture, as the harness's first real use).

**Seen:** 2 Oct 2026, moving the harness conversation from
`~/Dropbox/work/harness` to `~/code/harness`. Rob: "I do it all the time."

**What is known:**
- Claude Code has no supported command for this; the docs call copying
  transcripts unsupported. It worked anyway.
- What worked: copy the session's transcript (`<session-id>.jsonl`) and its
  data folder of the same name from
  `~/.claude/projects/<old-path-encoded>/` to
  `~/.claude/projects/<new-path-encoded>/`, then resume from the new folder.
  The encoded name is the folder path with `/` replaced by `-`.
- The working copy differed from the original near the top of the file, so
  some rewriting of the old path was probably involved. The exact commands
  were in the old transcript, which has been deleted; rediscover them during
  Capture.
- Memory is keyed to the folder, so the `memory/` folder has to be copied too.
- Afterwards: check new messages land in the copy, then delete the original.

## Unranked candidates

Seen in Rob's Colax sessions (Aug to Oct 2026), surveyed on 2 Oct 2026.
Counts are rough keyword matches over about 1,650 of his messages.

- **TikZiT string-diagram style.** Already exists as an unversioned skill in
  `~/.claude/skills/tikzit-string-diagrams`; move it into this library.
- **tikz-cd style.** Commutative diagrams in Rob's style. Part of about 115
  diagram requests ("follow my style", "rotate the diagram").
- **Diagram edit loop.** Draw, render, open in TikZiT or quiver for Rob to
  edit, read the edit back, learn from the difference.
- **Review of an edit.** "Made an update, what do you think?": about 340
  messages. Read the diff since the last review; report blockers only.
- **Project notebook.** Outline, decisions and literature notes kept in the
  project repo. The Colax state lives in one 40 MB session, compacted
  several times.
- **Cold reader.** A reviewer that sees only the draft, for strength and
  readability checks. About 30 trust checks ("are you sure?", "don't hedge").
- **Writer in Rob's voice.** About 30 readability complaints ("put it
  back", "in my voice").
- **Literature check with verbatim quotes.** About 160 literature, novelty
  and citation requests; quotes must come from the source with a location.
- **Working rules.** Standing preferences now in the Colax project's memory
  folder (ask on forks, verify before asserting, references are Rob's).
- **Scenario-based review for autoformalization.** A solver generates
  concrete cases from a formal model for an auditor to accept or reject.
