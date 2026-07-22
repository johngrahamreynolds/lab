# One-time setup

1. Create an empty repo named `lab` on GitHub (no README, no .gitignore).
2. Unpack this archive, then:

```bash
cd lab
grep -rl johngrahamreynolds . | xargs sed -i '' 's/johngrahamreynolds/your-gh-handle/g'   # macOS
# on Linux: grep -rl johngrahamreynolds . | xargs sed -i 's/johngrahamreynolds/your-gh-handle/g'

git init && git add -A && git commit -m "scaffold lab notebook"
git branch -M main
git remote add origin git@github.com:your-gh-handle/lab.git
git push -u origin main
```

3. In the repo: Settings → Pages → Source = "Deploy from a branch" → `gh-pages` / root.
   The first push creates the branch via the Actions workflow.
4. Locally: `quarto preview` to write, `quarto render` then commit `_freeze/`
   before pushing.

The template entry has `draft: true`, so it will not appear in the listing until
you remove that line.
