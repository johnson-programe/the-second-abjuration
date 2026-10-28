# Publishing Status / 发布状态

## ✅ GitHub — DONE
Live at: **https://github.com/johnson-programe/the-second-abjuration**

Pushed from this folder (commit `540dd3d`). To update later:

```bash
cd "mod/the_second_abjuration"
git add -A && git commit -m "update"
git push
```

---

## ⚠️ Steam Workshop — ready, needs your one-time Steam login

SteamCMD has been installed and bootstrapped at:
`C:/Users/a2022/WorkBuddy AI/2026-10-27-23-43-58/_steamcmd/steamcmd.exe`

Your Steam account: **johnson09034**

Because publishing requires your **Steam password + Steam Guard code** (which cannot be entered
from here), run this one command in a terminal and complete the login prompt:

```bat
"C:\Users\a2022\WorkBuddy AI\2026-10-27-23-43-58\_steamcmd\steamcmd.exe" ^
  +login johnson09034 ^
  +workshop_build_item "C:\Users\a2022\WorkBuddy AI\2026-10-27-23-43-58\mod\the_second_abjuration\workshop.vdf" ^
  +quit
```

- On the **first** upload `"publishedfileid" "0"` stays; SteamCMD prints the new Workshop ID.
  Put that ID into `workshop.vdf` for future updates.
- After the first successful login, SteamCMD caches the session token, so subsequent updates are
  the same command without a password prompt.
- The cover image is `thumbnail.png` (Dutch tricolor), already referenced by `workshop.vdf`.

- `visibility`: `0` = public, `1` = friends only, `2` = private.

---

## Files
| File | Purpose |
|---|---|
| `descriptor.mod` | Mod metadata (references `thumbnail.png`) |
| `thumbnail.png` | 512×512 Dutch flag cover |
| `workshop.vdf` | SteamCMD Workshop descriptor (appid 394360) |
| `README.md` | Short intro + AI/human credit |
