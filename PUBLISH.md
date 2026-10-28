# Publishing Status / 发布状态

## ✅ GitHub — LIVE
**https://github.com/johnson-programe/the-second-abjuration**

## ✅ Steam Workshop — LIVE
**https://steamcommunity.com/sharedfiles/filedetails/?id=3828723997**
- Workshop ID: `3828723997` (already written into `workshop.vdf` as `publishedfileid`)
- Visibility: public (0)
- Cover: `thumbnail.png` (Dutch tricolor)

---

## Updating in future

### GitHub
```bash
cd "mod/the_second_abjuration"
git add -A && git commit -m "update"
git push
```

### Steam Workshop (same item, no new entry)
```bat
"C:\Users\a2022\WorkBuddy AI\2026-10-27-23-43-58\_steamcmd\steamcmd.exe" ^
  +login johnson09034 ^
  +workshop_build_item "C:\Users\a2022\WorkBuddy AI\2026-10-27-23-43-58\mod\the_second_abjuration\workshop.vdf" ^
  +quit
```
(`publishedfileid` is now non-zero, so this updates the existing item instead of creating a new one.)

Or simply double-click `publish_steam.bat` in the project root.

---

## Files
| File | Purpose |
|---|---|
| `descriptor.mod` | Mod metadata (references `thumbnail.png`) |
| `thumbnail.png` | 512×512 Dutch flag cover |
| `workshop.vdf` | SteamCMD Workshop descriptor (appid 394360, id 3828723997) |
| `README.md` | Short intro + AI/human credit |
