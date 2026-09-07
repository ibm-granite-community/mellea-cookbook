# Contributing to the Mellea Cookbook

Thank you for your interest in contributing! This guide walks you through the full process from idea to merged pull request.

---

## Step 1 — Check Existing Issues First

Before starting any work, visit the [GitHub Issues](https://github.com/generative-computing/mellea-cookbook/issues) page.

- Browse open issues and PRs to avoid duplicate effort.
- If someone is already working on something related, leave a comment to coordinate.
- If you want to take on an open issue, comment on it to let maintainers know.

---

## Step 2 — Propose Your Idea

**For new recipe ideas or feature requests:**

- **Open a GitHub issue** — describe the recipe, what it demonstrates, and why it's useful.
- **Or email** [aakriti.aggarwal13@ibm.com](mailto:aakriti.aggarwal13@ibm.com) with your proposal.

Wait for a maintainer to confirm the idea is a good fit before investing time writing the notebook.

---

## Step 3 — Set Up Your Local Environment

### Fork and clone

```bash
# Fork the repo on GitHub, then:
git clone https://github.com/<your-username>/mellea-cookbook.git
cd mellea-cookbook
```

### Install pre-commit hooks

The repo enforces `markdownlint`, `pyspelling`, and `nbstripout` via pre-commit. Install and configure them before making any commits.

```bash
pip install pre-commit
pre-commit install
```

A failing hook aborts the commit — fix the flagged issues, re-stage, and commit again.

### Configure DCO signoff (required on every commit)

```bash
# Option A: add -s to every commit manually
git commit -s -m "your message"

# Option B: create a permanent alias (recommended)
git config --global alias.cs "commit --signoff"
git cs -m "your message"
```

### Configure commit signing with SSH (required on every commit)

```bash
# Generate a key if you don't have one
ssh-keygen -t ed25519 -C "your@email.com"

# Tell git to sign automatically
git config --global gpg.format ssh
git config --global user.signingkey ~/.ssh/id_ed25519.pub
git config --global commit.gpgsign true
```

Then add the public key (`~/.ssh/id_ed25519.pub`) to your GitHub account under **Settings → SSH and GPG keys → New SSH key → Key type: Signing Key**.

> Both DCO signoff (`-s`) and SSH/GPG signing are required. They are separate things — a commit needs both.

---

## Step 4 — Write Your Recipe Notebook

Create a new directory under `recipes/` named after your recipe (PascalCase):

```text
recipes/
└── YourRecipeName/
    └── YourRecipeName.ipynb
```

### Notebook structure

Follow this cell order:

| Cell | Content |
|---|---|
| Title | `# Your Recipe Title` (markdown) |
| Intro | One paragraph explaining what the recipe demonstrates and why |
| What You'll Build | Bullet list of what the reader will produce |
| Prerequisites | Python version, models needed, any accounts required |
| Setup | `%pip install` / `uv pip install` dependencies |
| Steps | Numbered sections (`## Step 1`, `## Step 2`, …) with explanation + code |
| Complete Script | Self-contained copy of all code in one cell |
| Running the Notebook | How to run it end-to-end |
| Key Takeaways | 4–6 bullet points summarising what was learned |
| Next Steps | Links to related recipes |

### Requirements for a valid recipe

- **Must run end-to-end** without manual intervention after setup.
- All dependencies installable via `pip` / `uv pip install`.
- Use `ollama/granite4.1:8b` (or another freely available local model) as the default so no paid API keys are needed.
- Clear outputs in the notebook before committing (`nbstripout` will enforce this automatically via the pre-commit hook).
- No hardcoded secrets, API keys, or personal data.

---

## Step 5 — Register the Notebook

### Add to `vanilla_notebooks.txt`

Open `.github/notebook_lists/vanilla_notebooks.txt` and add one line:

```text
recipes/YourRecipeName/YourRecipeName.ipynb
```

This file drives the CI pipeline that executes all notebooks on every PR.

### Update `README.md`

Add your recipe under the appropriate section in `README.md` using this format:

```markdown
1. [Your Recipe Title](recipes/YourRecipeName/YourRecipeName.ipynb) — One-line description of what it demonstrates.
   <a target="_blank" href="https://colab.research.google.com/github/generative-computing/mellea-cookbook/blob/main/recipes/YourRecipeName/YourRecipeName.ipynb">
   <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
   </a>
```

---

## Step 6 — Commit Your Changes

Make sure every commit includes both DCO signoff and SSH/GPG signing:

```bash
# Stage your files
git add recipes/YourRecipeName/YourRecipeName.ipynb
git add .github/notebook_lists/vanilla_notebooks.txt
git add README.md

# Commit (signing is automatic if you set commit.gpgsign true in Step 3)
git commit -s -m "add YourRecipeName recipe"
```

If you forgot signoff or signing on a previous commit:

```bash
git commit -S -s --amend
git push --force
```

---

## Step 7 — Open a Pull Request

```bash
git push origin your-branch-name
```

Then open a PR on GitHub against the `main` branch. In the PR description:

- Reference the issue it addresses (e.g. `Closes #42`)
- Describe what the recipe demonstrates
- Confirm the notebook runs end-to-end locally
- List the model and any other prerequisites

Maintainers will review, request changes if needed, and merge when ready.

---

## Licenses

| Content type | License |
|---|---|
| Code (notebook cells, scripts) | Apache 2.0 |
| Documentation and written content | CC BY 4.0 |
| Datasets | CDLA Permissive 2.0 |
