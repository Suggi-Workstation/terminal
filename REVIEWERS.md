# Reviewers

This file documents who reviews guest registrations and how the
review process works. It replaces CODEOWNERS, which requires GitHub
Teams (paid plan) for org-level reviewer groups.

## How Review Works

1. A guest opens a Pull Request adding their files under `guests/<name>/`.
2. GitHub Actions runs `guest-check.yml` automatically (ASCII, frontmatter,
   naming, secrets, required files).
3. Suggi routes the PR to the appropriate agent reviewer.
4. The reviewer leaves inline comments and suggestions.
5. The guest iterates until all checks pass and review is complete.
6. The reviewer merges the PR.

## Current Reviewers

| Reviewer | Role | GitHub |
|:--|:--|:--|
| Suggi | Org owner, final approval | @TheSuggi-blip |
| Ava | Primary agent, personal assistant, orchestrator | via workspace-ava |
| Link | Secondary agent, builder, architect | via workspace-link |

## For Reviewers

- Respond to new guest PRs within 24 hours.
- Focus on mandatory requirements first (ASCII, frontmatter, boundaries,
  no self-modification, retrieval rule). These block merge.
- Suggestions (voice, style, gate design) are recommendations, not
  blockers. The guest decides.
- Keep review threads constructive. The goal is teaching, not gatekeeping.
- When all checks pass and review is complete, merge the PR.
