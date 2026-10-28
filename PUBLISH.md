# Publishing Guide / 发布指南

The mod package is ready. Because uploading requires **your** GitHub and Steam credentials (which
are not available in this session), the two uploads below must be executed by you. Everything else
(README, `.gitignore`, Dutch-flag `thumbnail.png`, `workshop.vdf`) is already prepared.

---

## 1) GitHub

A local git repository has been initialized and committed. To publish:

1. Create an empty repository on GitHub (e.g. `the-second-abjuration`). Do **not** add a README.
2. In this folder run:

```bash
cd "mod/the_second_abjuration"
git remote add origin https://github.com/<YOUR_USER>/the-second-abjuration.git
git branch -M main
git push -u origin main
```

If you have the GitHub CLI (`gh`) installed instead:

```bash
cd "mod/the_second_abjuration"
gh repo create the-second-abjuration --public --source=. --remote=origin --push
```

---

## 2) Steam Workshop

The HOI4 Workshop app id is **394360**. `workshop.vdf` is prepared with:
- `contentfolder` → this mod folder
- `previewfile` → `thumbnail.png` (Dutch flag)
- `title` / `description` (already credits AI + author)

### Option A — SteamCMD (recommended, repeatable)

```bash
steamcmd +login <YOUR_STEAM_ACCOUNT> ^
  +workshop_build_item "C:/Users/a2022/WorkBuddy AI/2026-10-27-23-43-58/mod/the_second_abjuration/workshop.vdf" ^
  +quit
```

- On the **first** upload keep `"publishedfileid" "0"`; SteamCMD prints the new ID.
  Put that ID back into `workshop.vdf` for future updates.
- `visibility`: `0` = public, `1` = friends, `2` = private.

### Option B — In-game uploader

If your HOI4 copy supports the in-game "Upload mod to Steam Workshop" flow, point it at
`the_second_abjuration/` and choose `thumbnail.png` as the preview image.

---

## 3) Files in this folder

| File | Purpose |
|---|---|
| `descriptor.mod` | Mod metadata (references `thumbnail.png`) |
| `thumbnail.png` | 512×512 Dutch flag — Workshop/launcher cover |
| `workshop.vdf` | SteamCMD Workshop content descriptor |
| `README.md` | Short intro + AI/human credit |
| `.gitignore` | Keeps build/zip clutter out of git |

## Notes

- `thumbnail.png` is a clean Dutch tricolor (red `#AE1C28`, white `#FFFFFF`, blue `#21468B`).
- The description and README both state the mod was **created by AI (WorkBuddy) together with the author**.
