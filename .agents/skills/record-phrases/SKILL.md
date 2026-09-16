---
name: record-phrases
description: Save English phrases already explained but not yet recorded in the current session. Use only after the user explicitly requests recording.
disable-model-invocation: true
---

# Record pending English phrases

## Invocation contract

This skill performs the deferred persistence phase for the English-learning repository.

The invocation itself is explicit authorization to modify the repository, create commits, and push them to the current branch upstream. Never invoke this workflow merely because the user sends an English phrase or asks for an explanation. Ordinary phrase messages receive an explanation only, as required by `AGENTS.md`.

Unless the user narrows the scope in the invocation arguments, process every phrase from the current conversation that has been explained but does not yet have a phrase record. Preserve conversation order.

## Collect pending phrases

1. Inspect the current conversation, not guessed memory, for English phrases supplied by the user.
2. For each phrase, retain the exact original English text, the user's stated understood and unclear parts, whether the whole meaning was understood, and later corrections or clarifications.
3. Search `phrases/` for the exact original text. Exclude phrases that already have a record; never create a duplicate because the command was invoked twice.
4. If the user selected particular phrases, exclude all others.
5. If no pending phrases remain, report that no records were needed and do not create a commit.

Do not invent a phrase or learning gap that is absent from the conversation. If an explicitly selected phrase is no longer available in conversation context, name that missing prerequisite instead of reconstructing it.

## Record each phrase

Process phrases sequentially because knowledge files can overlap and every phrase requires its own commit.

For each phrase:

1. Capture the current working-tree and index state before editing.
2. Follow the complete recording workflow and templates in the repository `AGENTS.md`.
3. Search normalized entries, headings, forms, and spelling variants throughout `vocabulary/`, `expressions/`, and `grammar/` before creating knowledge files.
4. Create the next dated `phrases/YYYY/MM/YYYY-MM-DD-NNN.md` record.
5. Add only genuinely new meanings or contexts to knowledge files. Do not duplicate an existing source context.
6. Maintain reciprocal relative links between the phrase record and every knowledge entry used by it.
7. Validate exact source text, template fields, meaning boundaries, link targets, and the absence of fabricated context.
8. Stage only explicit paths changed for this phrase, run `git diff --cached --check`, and create one atomic commit using the repository message conventions.
9. Push the commit to the configured upstream with ordinary `git push`. If the branch has no upstream and `origin` exists, establish it with `git push -u origin <current-branch>`.
10. Record the short commit hash and push destination before continuing to the next phrase.

Never force-push or rewrite remote history. If push fails, keep the local commit intact, stop before processing the next phrase, and report the failure.

Never use a background subagent for repository writes in this workflow: shared knowledge files and ordered per-phrase commits require a single writer.

## Report

Do not repeat the full linguistic explanation unless the user asks for it. For each processed phrase, report:

- the phrase or an unambiguous short label;
- created and updated records;
- the short commit hash and commit message;
- the push destination and successful result, or the exact push failure.

Report skipped already-recorded phrases separately. Do not expose routine internal tool activity.
