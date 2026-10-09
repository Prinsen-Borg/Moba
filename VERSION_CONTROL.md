# VERSION_CONTROL.md: Git strategy & collaboration

## 1. Remote

- **Primary remote:** `https://github.com/Prinsen-Borg/Moba` (to move to Moba's own GitHub/Azure DevOps organisation later)
- **Default branch:** `main`, which is protected and changes only through pull requests

```bash
git clone https://github.com/Prinsen-Borg/Moba.git
cd Moba
```

## 2. Branches

| Prefix | Use | Example |
|---|---|---|
| `feature/` | New skill, tool or document | `feature/skill-investment-review` |
| `fix/` | Correction | `fix/design-amber-contrast` |
| `docs/` | Text-only changes | `docs/agents-security-section` |

## 3. Commit messages (Conventional Commits)

`type(scope): short description in the imperative`

- `feat(skills): add moba-web-page skill`
- `design(tokens): add navy gradient`
- `docs(agents): clarify data classification`
- `chore(repo): initial structure`

Make one logical change per commit. AI-assisted commits keep the co-author line.

## 4. Pull requests

1. Create a branch, make the change, commit and push.
2. Open a pull request with what changed and why, plus a screenshot for visual changes.
3. Get at least one human review before merging. **AI may draft, but humans approve.**
