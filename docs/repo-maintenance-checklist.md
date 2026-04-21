# Repository Maintenance Checklist

Use this checklist during weekly hygiene review.

## 1) Pull request cleanup
- [ ] Review open PRs and close stale/superseded ones with a clear comment.
- [ ] Verify each active PR has:
  - [ ] Clear objective in title/description.
  - [ ] Linked issue (`Closes #<id>`).
  - [ ] Branch up to date with `main`.

Suggested close comment:
> Closing as stale/superseded. This work is now covered by PR #<id> (or commit <sha>). Reopen if still required.

## 2) Branch cleanup
- [ ] Delete merged and obsolete test branches from the remote.
- [ ] Keep only `main` and currently active feature/fix/docs branches.
- [ ] Enforce consistent branch naming (`feature/*`, `fix/*`, `docs/*`, `chore/*`).

## 3) Issue triage
- [ ] Audit open issues against latest `main`.
- [ ] Close invalid/already-fixed issues with rationale and linked fix.
- [ ] Normalize labels to: `bug`, `frontend`, `backend`, `docs`, `security`.
- [ ] Add assignee and milestone for each active issue where appropriate.

## 4) Required GitHub settings (manual)
Settings are not versioned in code; verify these in repository settings:

- [ ] **General → Pull Requests**: Enable "Automatically delete head branches".
- [ ] **Branches → Branch protection for `main`**:
  - [ ] Require a pull request before merging.
  - [ ] Require at least 1 approving review.
  - [ ] Dismiss stale approvals when new commits are pushed.
  - [ ] Require status checks to pass before merging.
  - [ ] Block force pushes and branch deletion.

## 5) Security/config hygiene
- [ ] Confirm no hardcoded credentials in tracked files.
- [ ] Keep `.env.example` updated with required variables only (no real secrets).
- [ ] Ensure docs instruct contributors to use environment variables for secrets.
