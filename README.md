# AI PR Reviewer

Automatically reviews every Pull Request using **Gemini 2.5 Flash** and posts a comment with:

- A one-line summary of what changed
- Three bullet points of key changes
- One suggestion or concern

## How It Works

1. A PR is opened or updated
2. GitHub Actions triggers automatically
3. The workflow fetches the PR diff
4. Diff is sent to Gemini AI
5. Gemini's review is posted as a PR comment

## Setup

1. Add `GEMINI_API_KEY` to repo **Settings → Secrets → Actions**
2. The `GITHUB_TOKEN` is provided automatically by GitHub
3. Workflow file lives at `.github/workflows/pr-review.yml`

## Tech Used

- GitHub Actions
- GitHub REST API
- Google Gemini 2.5 Flash API
- Python (urllib, json)
