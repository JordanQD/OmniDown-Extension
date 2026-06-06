# Upstream Sync

This fork keeps the default branch aligned with the original project and uses
`fluent-ui` for UI customization work.

## Remotes

- `origin`: `https://github.com/JordanQD/OmniDown-Extension.git`
- `upstream`: `https://github.com/AnInsomniacy/motrix-next-extension.git`

## Sync From Upstream

Run these commands from the repository root:

```bash
git switch main
git fetch upstream
git merge --ff-only upstream/main
git push origin main

git switch fluent-ui
git merge main
git push
```

## Notes

- Keep `main` as the upstream-tracking baseline.
- Do UI customization work on `fluent-ui`.
- Do not commit local UI changes directly to `main`.
- If `git merge --ff-only upstream/main` fails, stop and inspect the divergence
  before choosing a merge or rebase strategy.
