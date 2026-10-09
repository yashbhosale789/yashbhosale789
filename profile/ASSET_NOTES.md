# Profile asset notes

This profile uses hosted cards for GitHub stats, streaks, activity, and trophies. These are external services, so they can occasionally rate-limit or fail independently of your repository.

## Contribution snake
The workflow at `.github/workflows/update-profile-assets.yml` generates the two snake SVGs and publishes them to the `output` branch.

## Before publishing
- Confirm that `yashbhosale789` is the correct GitHub username.
- Add repository links to the Featured Work section only after confirming the public URLs.
- Remove or rewrite any project card that does not accurately describe a public or current project.
- Enable GitHub Actions for the repository. The workflow needs permission to write to the `output` branch.
- If the default branch is not `main`, update the workflow trigger branch accordingly.

## Why the old local stats SVGs were removed
The previous local `profile/stats.svg` was showing an API/integration error, and the old language SVG contained hardcoded percentages. The README now uses live cards rather than committing stale generated stats. The contribution snake remains generated and published by Actions.


## Live GitHub stats
The README embeds dynamic cards for profile stats, most-used languages, contribution streak, activity graph, trophies, and profile views. These are live third-party SVG endpoints, not locally fetched numeric snapshots. GitHub Readme Stats language data is based on public repositories and is a measure of code distribution, not a measure of skill. Public endpoints can be rate-limited or temporarily unavailable.
