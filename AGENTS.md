# Repository instructions for LLM-personality

Applies to this repository's published LLM working guidance.

## Source of truth and change discipline

- `README.md` contains user-facing, evidence-first instructions for technical agents, including a single copyable block and a documented character count. Treat it as the project's principal artifact; this `AGENTS.md` guides repository maintenance and does not silently rewrite the user's globally configured assistant instructions.
- Do not change the core meaning of target fidelity, authorization boundaries, evidence requirements, failure handling, privacy, or validation without an explicit request. Preserve working safety guarantees and avoid unnecessary style/terminology rewrites.
- If editing the copyable instructions, verify the actual character count and formatting, update its stated count, and make sure the complete paste-ready block stays within any relevant target limit. Do not fabricate a platform-specific character limit.
- Avoid contradictory or self-weakening language: no generic "always merge", "always release", or automatic-action mandates that would undermine scoped approval or risk controls. Apply new wording only to the requested project target.
- Compare the proposed text against the existing `README.md` and call out meaningful additions/removals; text proofreading alone does not justify unrelated publication.

## Merge and release authorization

Operate autonomously within the user's approved scope. Do not add unnecessary repeat-approval checkpoints.

- Investigating, implementing, fixing, testing, committing scoped work to a feature branch, or preparing an ordinary review PR does **not** by itself authorize merging to the default branch, creating a tag, publishing a GitHub Release, distributing a build, or deploying to devices.
- An explicit instruction to merge, apply directly to `main`, tag, or release authorizes that named operation for the specified work. An approved release includes the necessary scoped merge unless the user specifies another target or restriction. Do not demand another approval for already-authorized steps.
- Authorization for an **unfinished** merge or release survives related small fixes, revisions, and testing pauses. If the user interrupts an approved release to correct something, "good to go", "working, continue", or a similarly clear signal may resume that same pending release without asking for the original approval again.
- Respect "wait", "hold off", and cancellations. A pause stops delivery until the user clearly resumes; cancellation withdraws approval. Materially different work, a changed release target, or an altered version beyond what was authorized requires renewed authorization.
- Approval is **single-use**: after the authorized merge/release finishes, it does not authorize another merge or release, including a follow-up patch. Positive feedback alone ("perfect", "that works") cannot start a new delivery operation when none is pending.
- The user may approve a merge or release without personally testing it. Run the available relevant static/automated checks, report meaningful failures, and distinguish automated validation from unperformed real-device/runtime tests. Do not impose user testing as an extra requirement if the user explicitly elects to proceed.
- Drafting release notes, suggesting a version, or preparing a branch/PR is not publication. Publishing workflows, temporary GitHub Actions release bridges, Git tags, Releases, uploads, and external release artifacts require the active authorization for that exact publication.
- Never equate approval for a GitHub Release with approval for unrelated distribution, production deployment, hardware changes, destructive data operations, credential exposure, or external-provider settings.

## Validation and distribution

- Validate Markdown structure, exact copy-block boundaries, character count, and consistency between the policy and user-facing text. No code/build artifact is implied.
- Changes to this repository do not automatically change ChatGPT settings, existing agents, saved personalization, or other repositories. Do not claim they were applied outside this repository.
- Do not create a release/tag or assume a version convention unless specifically requested.
