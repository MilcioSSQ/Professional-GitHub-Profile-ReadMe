# Setup

Follow these steps after you've copied this template. Takes about 10 minutes.

---

## 1. Rename the repository

The repository **must be named exactly like your GitHub username** for the
profile README to show up on your profile.

Go to **Settings → General → Repository name** and set it to your username.

---

## 2. Replace the username

Copy `PROFILE_README.md` to your username repo as `README.md`, then do a find & replace:

```
MilcioSSQ  →  your-github-username
```

Do the same in `.github/workflows/snake.yml` if you want, though that file
already uses `${{ github.repository_owner }}` which resolves automatically.

---

## 3. Update your personal info

In `README.md`, edit the `const developer = { … }` block at the top — name,
location, current focus, and the "What I do" bullet list.

---

## 4. Update your links

Find and replace these placeholders in `README.md`:

| Placeholder | Replace with |
|---|---|
| `https://discord.gg/YOUT-INITE-LINK` | your Discord server invite |
| `https://discord.com/users/YOUR-USER-ID` | your Discord profile link |
| `https://ko-fi.com/YOUTR-USER-NAME` | your Ko-fi / donation link |
| `https://twitch.tv/YOUTR-USER-NAME` | your Twitch channel |
| `https://twitter.com/YOUTR-USER-NAME` | your Twitter/X handle |
| `https://leetcode.com/u/YOUTR-USER-NAME/` | your LeetCode profile |
| `https://www.codewars.com/users/YOUTR-USER-NAME` | your Codewars profile |

---

## 5. Optional sections

Remove any section that doesn't apply to you — a widget showing all zeros
or a broken image is worse than not having it.

| Section | Remove if… |
|---|---|
| Discord badges | you don't want to show your Discord badges |
| LeetCode stats card | you don't use LeetCode |
| Ko-fi button | you don't have a donation page |
| Twitch / Twitter | you're not on those platforms |
| Featured Projects | you have no public repos worth pinning yet |

---

## 6. Pin your real repos

On your profile page, click **"Customize your pins"** and select up to 6 of
your actual repositories. Delete or comment out the Featured Projects section
in `README.md` if you have fewer than 2 good repos to show.

---

## 7. Start the snake animation

1. Go to **Actions** → "generate contribution snake" → **Run workflow**
2. After it finishes (~30 s), an `output` branch appears with the SVG files
3. The snake will update automatically every 12 hours and on every push

If it fails, see `TROUBLESHOOTING.md`.

---

## 8. Discord badges

The Discord badge images in `README.md` are plain shields.io badges — they
don't pull from Discord's API, so they only look right if you edit them to
match your actual badges.

Current badges in the template (MilcioSSQ's):
`Nitro` · `HypeSquad Bravery` · `Server Booster` · `Originally Known As` ·
`Completed a Quest` · `Orbs` · `Gifting`

Remove any you don't have, add any that are missing.

---

## Done

Push your changes, visit `github.com/your-username`, and the README should
appear on your profile. If widgets show nothing, see `TROUBLESHOOTING.md`.
