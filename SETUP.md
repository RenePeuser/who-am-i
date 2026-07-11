# Setup and first deployment

## 1. Copy into the existing repository

Extract the ZIP and copy the contents into your local clone of:

```text
https://github.com/RenePeuser/who-am-i
```

The generated `README.md` intentionally replaces the current placeholder.

## 2. Preview locally

```bash
python -m venv .venv

# Windows
.venv\Scripts\activate

pip install -r requirements.txt
mkdocs serve
```

Open <http://127.0.0.1:8000>.

## 3. Validate

```bash
mkdocs build --strict
```

## 4. Commit

```bash
git checkout -b feat/engineering-portfolio-foundation
git add .
git commit -m "feat: establish engineering portfolio foundation"
git push -u origin feat/engineering-portfolio-foundation
```

## 5. Enable GitHub Pages

The workflow publishes to the `gh-pages` branch.

In GitHub:

1. Open **Settings → Pages**.
2. Select **Deploy from a branch**.
3. Select branch **gh-pages** and folder **/(root)**.
4. Save.

The expected URL is:

```text
https://renepeuser.github.io/who-am-i/
```

## 6. Recommended review before publishing

- Verify employer/project dates.
- Confirm which Siemens details may be public.
- Verify exact BASTA! talks and speaking years.
- Decide whether to publish the year of birth.
- Add a professional portrait only when you own the image rights.
- Replace approximate package statistics periodically or automate them.
