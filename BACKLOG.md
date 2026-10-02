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
