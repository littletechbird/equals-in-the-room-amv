# Publish — littletechbird/equals-in-the-room-amv

Exact commands to create and push this **public** documentation pack.

Docs + JSON only. Do **not** add binary video/audio.

---

## Prerequisites

- `gh` authenticated as a user that can create repos under **littletechbird**
- Working tree at `/workspace/equals-in-the-room-amv` (or a clone of this pack)
- Public scrub already applied (no real human name/surname, no personal device nicknames, no secrets/emails/phones/addresses)

---

## One-shot (init + create + push)

```bash
cd /workspace/equals-in-the-room-amv && \
git init && \
git add . && \
git -c user.email='hatch@littletechbird.local' -c user.name='Hatch' \
  commit -m 'Equals in the Room — forever guide, wager, burn sheet' && \
gh repo create littletechbird/equals-in-the-room-amv \
  --public \
  --source=. \
  --remote=origin \
  --push \
  --description 'Equals in the Room — Hatch origin AMV guide, wager, and burn sheet'
```

Expected remote after success:

**https://github.com/littletechbird/equals-in-the-room-amv**

---

## If the repo already exists empty on GitHub

```bash
cd /workspace/equals-in-the-room-amv
git init
git add .
git -c user.email='hatch@littletechbird.local' -c user.name='Hatch' \
  commit -m 'Equals in the Room — forever guide, wager, burn sheet'
git branch -M main
git remote add origin https://github.com/littletechbird/equals-in-the-room-amv.git
git push -u origin main
```

---

## If `gh auth` fails

1. Leave the pack on disk at `/workspace/equals-in-the-room-amv`.
2. Authenticate on the local device (`gh auth login`) as the littletechbird maintainer.
3. Re-run the one-shot (or the “already exists” path).

Do not embed tokens in this repo. Do not paste API keys into docs.

---

## Post-push checklist

- [ ] Repo is **public**
- [ ] README renders with YouTube / X / template / sister-guide links
- [ ] No binaries accidentally added (`git ls-files` should be markdown/json/LICENSE only)
- [ ] Optional: pin repo or link from the Fairy Tale README “sister cut” section
- [ ] Optional: reply on the X proof post with the GitHub URL
