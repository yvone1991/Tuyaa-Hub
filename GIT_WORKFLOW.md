# Git Workflow

This repository uses two remotes:

- `origin`: my own repository, `git@github.com:yvone1991/Tuyaa-Hub.git`
- `upstream`: the official repository, `https://github.com/esengine/DeepSeek-Reasonix.git`

Use `codex/custom-dev` for daily development.

```powershell
git switch codex/custom-dev
```

Commit and push my own changes:

```powershell
git add .
git commit -m "your commit message"
git push
```

Use `codex/github-sync` only to pull official updates:

```powershell
git switch codex/github-sync
git pull --ff-only
```

Merge official updates into my development branch:

```powershell
git switch codex/custom-dev
git merge codex/github-sync
git push
```

Do not develop directly on `codex/github-sync`. It should stay aligned with the official `upstream/main`.
