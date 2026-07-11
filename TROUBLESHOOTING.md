# Troubleshooting

## Snake animation isn't showing

**Step 1 — run the workflow manually**

Actions tab → "generate contribution snake" → **Run workflow** → wait ~30 s.

**Step 2 — check the logs**

| Error | Cause | Fix |
|---|---|---|
| `403` / `Resource not accessible by integration` | Workflow missing write access | Settings → Actions → General → Workflow permissions → **Read and write permissions** → Save → re-run |
| `User not found` / `404` | Wrong username | Open `.github/workflows/snake.yml`, confirm `github_user_name` |
| Run succeeds but no `output` branch | Push step failed silently | Check the "push snake output" step's log specifically |
| Workflow doesn't appear in Actions tab | File at wrong path | Must be exactly `.github/workflows/snake.yml` |

**Step 3 — confirm the branch exists**

Switch the branch dropdown to `output`. You should see
`github-contribution-grid-snake.svg` and the `-dark.svg` variant.
If the branch doesn't exist, the workflow hasn't completed successfully.

---

## Widgets show a broken image

Most stat cards (GitHub stats, streak, trophies) are free third-party
services, not GitHub itself.

1. Check your username is spelled correctly in each URL
2. Wait a few minutes — some services are rate-limited
3. Make sure your profile is **Public** and "Include private contributions"
   is enabled in your profile settings

---

## Everything looks empty

Expected if you don't have much GitHub activity yet. These widgets reflect
your real account data — there's no setting to make them show more than you
actually have. They fill in as you use GitHub more.

---

## Streak counter shows 0 / wrong number

The streak service at `streak-stats.demolab.com` is the most reliable
free option as of 2026. If it's down, try again in a few minutes.
Your streak resets if you go a full calendar day (UTC) without a contribution.
