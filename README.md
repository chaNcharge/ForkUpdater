# ForkUpdater

A small script that will automatically update your forks. Designed for Heroku and GitHub, but can run on any project on any Git repository via CI or cronjob. If there's a problem with merging (such as merge conflicts), the script will open up an issue in your repo to let you know there was an issue.

## Environment variables

Environment variables must be used when running the script. The reason why they're not in the script itself is for security, as you need to provide an access token. With environment variables, you can easily change these values on any dashboard while also keeping your variables secure.

- `GITHUB_REPO`: Your repo; part of the link after `https://github.com/` (e.g `chaNcharge/avaire`)
- `GITHUB_REPO_BRANCH`: Your repo's branch to merge into
- `GITHUB_SECRET_TOKEN`: Your personal access token, the token will need public repo permissions
- `UPSTREAM_REPO`: The upstream repo to update from
- `UPSTREAM_BRANCH`: The upstream repo's branch to update from