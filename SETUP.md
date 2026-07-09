# Setup Guide

Everything here works through the GitHub website in your browser - no Git,
no command line, nothing to install.

## 1. Create your profile repository

1. Go to GitHub → click the `+` (top right) → **New repository**
2. Name it **exactly** the same as your GitHub username (case-insensitive,
   e.g. if your username is `johndoe`, the repo must be named `johndoe`)
3. Set it to **Public** (required - a private profile repo's README will
   never show on your profile page)
4. Don't initialize with a README (this template already has one)
5. Click **Create repository** - GitHub will show a banner confirming this
   is your special profile repository

## 2. Add the README

1. In your new repo, click **Add file → Upload files**
2. Upload `README.md` from this template
3. Open the uploaded `README.md`, click the pencil (edit) icon
4. Replace every `your-username` with your real GitHub username, and fill in
   the other placeholders (`your-leetcode-username`, `your-kofi-username`,
   `your-invite-code`, the `about-me.json` fields, etc.)
5. Commit the changes

## 3. Set up the live "contribution snake" animation

1. In your repo: **Add file → Create new file**
2. Type this exact path in the filename field (the slashes create the folders
   automatically): `.github/workflows/snake.yml`
3. Paste the contents of `snake-workflow.yml` from this template
4. Replace `your-username` in the `github_user_name:` line with your real
   username
5. Commit directly to `main`
6. **Required extra step**: go to **Settings → Actions → General**, scroll to
   "Workflow permissions", select **"Read and write permissions"**, click
   **Save**. Without this, the snake action can't publish its output and will
   fail.
7. Go to the **Actions** tab → click the "generate contribution snake"
   workflow → **Run workflow** (don't wait for the first automatic run)
8. After ~30-60 seconds, refresh - it should show a green checkmark. Your
   profile page will now show a snake eating your real contribution graph.

## 4. Add your own banner image

1. Design or find a banner image (recommended size: roughly 1600x400px)
2. In your repo: **Add file → Upload files** → upload it into a folder
   named `assets/` (e.g. `assets/banner.png`)
3. Make sure the `<img src="...">` at the top of `README.md` points to
   `https://raw.githubusercontent.com/your-username/your-username/main/assets/banner.png`

## 5. Pick your own languages/tools

The `languages.txt` section uses [skillicons.dev](https://skillicons.dev) -
open that site, click the icons you want, copy the generated URL, and paste
it in place of the existing one. Only list things you actually use - a
profile full of tools you've never touched isn't a great look if someone
asks you about them.

## 6. Optional: real Discord badges (do this honestly, not by copying someone else's)

The badges shown in some profile READMEs (Nitro, HypeSquad, etc.) are **not**
something any public API renders automatically as pretty images - there is no
reliable drop-in widget for this. If you want real ones:

1. Discord → Settings → Advanced → enable **Developer Mode**
2. Right-click your own name/avatar anywhere in Discord → **Copy User ID**
3. Join the Lanyard Discord server: https://discord.gg/lanyard (this makes
   your data queryable)
4. Fetch `https://api.lanyard.rest/v1/users/YOUR_ID` (paste that URL in a
   browser) - it returns a `public_flags` number
5. Decode which bits are set against Discord's public flag list (e.g. 64 =
   HypeSquad Bravery) - or just hover over each badge on your own Discord
   profile card, which shows the name directly as a tooltip
6. Add one `img.shields.io/badge/...` line per badge you actually have

## 7. Optional: LeetCode / Codewars / coding practice

Only include the `coding_practice.sh` section if you actually use these
platforms. Check the widget shows real, non-zero data for your username
before publishing it - an empty "0 solved" card doesn't look great. If it's
empty because you're new there, that's fine, just be aware it'll show that.

## 8. Optional: donations (Ko-fi / GitHub Sponsors)

- **Ko-fi** (no approval needed, works instantly): create an account at
  ko-fi.com, pick a display name (doesn't have to be your real name), then
  add a `.github/FUNDING.yml` file to your repo with:
  ```yaml
  ko_fi: your-kofi-username
  ```
  This adds an official "Sponsor" button to your repo.
- **GitHub Sponsors**: requires an application/approval through GitHub
  directly and bank details for payout - takes longer to set up, but runs
  natively through GitHub.

## Troubleshooting

- **README not showing on your profile page?** Check the repo name matches
  your username exactly and is Public.
- **Widgets/stats not loading?** These are free third-party services - wait
  a few minutes (they can be temporarily rate-limited), or double-check your
  username is spelled correctly in the URL.
- **Snake animation missing?** Check the Actions tab for a failed run - the
  most common cause is forgetting step 3.6 (Read and write permissions).
- **Everything looks sparse/empty?** Most of these widgets reflect your real
  GitHub/LeetCode/etc. activity. They fill in naturally as you use those
  platforms more - there's no setting that fakes more activity than you
  actually have, and this template intentionally doesn't try to.
