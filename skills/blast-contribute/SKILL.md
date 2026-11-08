---
name: blast-contribute
description: Contribute to Blast by finding an actionable GitHub issue in the TypeScript SDK or Sui Move contracts, implementing and verifying a focused fix, and preparing or opening a pull request.
---

# Blast Contribute

Blast is a coin launch platform on Sui. This skill takes one contribution from
a GitHub issue to a verified patch and pull request. The contracts own on-chain
behavior and events. The SDK builds transactions, reads and decodes on-chain
data, and derives previews.

## 1. Choose an issue

Use the issue the user named. For an open-ended contribution, check both
trackers live with GitHub or `gh issue list --state open --repo OWNER/REPO`.

- [Blast TypeScript SDK issues](https://github.com/interest-protocol/blast-v2-sdk/issues)
- [Blast Sui Move contracts issues](https://github.com/interest-protocol/blast-v2-contracts/issues)

Prefer one unassigned, well-scoped issue with clear acceptance criteria.
Prioritize `ready-for-agent` where the tracker uses it. Read the issue and its
discussion, check labels and assignees, and search open PRs for the issue number
and affected code. Check current upstream `main` for an existing fix. For a
general request, skip work already claimed or covered by a PR, work awaiting a
maintainer decision or missing information, and issues blocked by another change.
If a named issue is already fixed, report the evidence and stop. If nothing
qualifies, report which trackers you checked and why the candidates were
skipped.

For a suspected vulnerability, follow [Blast's private security reporting
policy](https://github.com/interest-protocol/blast-v2-contracts/blob/main/SECURITY.md)
before preparing anything public.

## 2. Implement and verify the fix

Use a clean contribution branch from the owning repository's current upstream
`main`. Read its `README.md`, `AGENTS.md`, and any applicable contribution
instructions and CI workflows. Reproduce a bug or turn the issue's acceptance
criteria into a check. Keep the patch scoped to that issue and add a focused
regression test where existing coverage would miss the failure.

- **SDK.** Use the root workspace and its documented build and test workflow.
  For transaction builders, decoders, or economic previews, verify behavior
  against the contract revision pinned by the SDK. If the issue changes the
  pin, verify the intended upstream revision and follow the SDK's ABI update
  procedure. Run the package checks when changing exports or metadata.
- **Contracts.** Use `llms.txt` to locate the affected Move package and run its
  local tests plus the applicable repository checks. For public API or event
  changes, check the contract's publication and upgrade rules, regenerate
  integrator references as directed, and identify SDK consumers that need a
  follow-up. Keep verification local and leave on-chain operations to maintainers.

Review the diff against upstream `main`. Record the commands and results that
demonstrate the fix, including any required checks you could not run.

## 3. Prepare and submit the pull request

Follow the target repository's PR template if it has one. Write a title that
names the affected behavior. In the body, explain the problem, what changed,
and how you verified it. Include `Fixes #123` for a complete fix in the same
repository, or `Fixes OWNER/REPO#123` for a complete cross-repository fix.
Use a plain issue link for partial fixes or dependent PRs. Note any public API,
event, or upgrade implications and link related changes. See [GitHub's guide to
linking issues](https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/linking-a-pull-request-to-an-issue).

When the user's request includes submission, commit the reviewed changes and
push the topic branch to a writable remote. Contributors without upstream
write access use a personal fork. Open a draft PR against the original Blast
repository's `main` with your topic branch as the head. On GitHub, use **Compare
across forks** to select the fork when applicable. With GitHub CLI, use
`gh pr create --draft --repo OWNER/REPO --base main --head BRANCH` for an
upstream branch or `--head YOUR-LOGIN:BRANCH` for a personal fork.
[GitHub's guide to PRs from forks](https://docs.github.com/en/pull-requests/how-tos/create-pull-requests/creating-a-pull-request-from-a-fork)

Verify the PR's base, head, and issue link. Check CI and review feedback, update
the same branch for follow-up fixes, and mark it ready once checks pass and the
user's requested review state permits it. Leave merge and release to maintainers.
If submission is outside the requested scope or access is unavailable, hand
off the branch or diff and the proposed PR title and body. Finish with the issue
link, change summary, verification results, and PR link or handoff.
