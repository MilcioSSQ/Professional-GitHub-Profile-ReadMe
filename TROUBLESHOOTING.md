# Troubleshooting

## The snake animation isn't showing up

### Step 1: Run the workflow manually

1. Go to your repository → **Actions** tab
2. Click "generate contribution snake" in the left sidebar
3. Click **Run workflow** → pick `main` → **Run workflow**
4. Wait ~30-60 seconds, then refresh the page

### Step 2: Check the run's logs

Click on the run that just started, then expand each step.

**Common errors and what they mean:**

| Error in the logs | Cause | Fix |
|---|---|---|
| `403` / `Resource not accessible by integration` | The workflow doesn't have write access | Settings → Actions → General → Workflow permissions → **"Read and write permissions"** → Save, then re-run |
| `User not found` / `404` | Wrong username in the workflow | Open `.github/workflows/snake.yml`, check `github_user_name:` matches your exact GitHub username |
| Step succeeds but no `output` branch appears | The push step didn't run or failed silently | Check the "push snake output" step's log specifically, not just the first step |
| Workflow doesn't appear in the Actions tab at all | The file isn't at the right path | It must be exactly `.github/workflows/snake.yml` - check for typos in the path when you created the file |

### Step 3: Confirm the branch exists

After a successful run, go to your repo and switch the branch dropdown (top left, usually says "main") to **`output`**. You should see `github-contribution-grid-snake.svg` and the `-dark.svg` version there. If that branch doesn't exist yet, the workflow hasn't completed successfully - go back to Step 2.

### Note on approach

Some versions of this workflow online use a manually-created Personal
Access Token (a `GH_PAT` secret) instead of the setup here. That's not
necessary - the workflow in this template uses GitHub's own built-in
token (`secrets.GITHUB_TOKEN`) with `contents: write` permission, which is
simpler and doesn't require you to create, store, or ever rotate a
separate token. If you copied a different snake workflow from somewhere
else that asks for a `GH_PAT`, you can safely switch to the one in this
template instead.

## Other widgets show nothing / a broken image icon

Most of the stat cards in `README.md` are free, third-party hosted
services (Vercel-hosted projects, not GitHub itself). If one doesn't load:

1. Double-check your username is spelled correctly in that specific URL
2. Wait a few minutes - some of these are rate-limited and recover on
   their own
3. Confirm your GitHub profile itself is set to **Public**, and that
   "Include private contributions" is enabled in your profile settings if
   you want private-repo activity to count toward the stats

## Everything looks sparse/mostly empty

This is expected if you don't have much GitHub activity yet - these
widgets all reflect your *real* account data. They aren't broken, and
there's no setting to make them show more than you actually have. See the
note in `SETUP.md` about this.
