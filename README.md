### 🚀 Automated Lighthouse metrics to your PR with Vercel and Github Actions.

The complete action can be found in [Lighthouse-github-action/.github/workflows/](https://github.com/OskarAhl/Lighthouse-github-action/blob/main/.github/workflows/lighthouse-on-vercel-preview-url.yml)

### Action workflow
1. Get the preview url for the PR (from Vercel).
2. un a Lighthouse audit on the preview url.
3. Format the score to a table (+throw in a few emojis).
4. Post a comment on the PR with the formatted score.

### Integrations used:
* [treosh/lighthouse-ci-action](https://github.com/treosh/lighthouse-ci-action)
* [sticky-pull-request-comment](https://github.com/marketplace/actions/sticky-pull-request-comment)
* [vercel-preview-url-action](https://github.com/marketplace/actions/capture-vercel-preview-url)

### Limitations:
* Always runs the Lighthouse audit on the root page.

### Potential future improvements:
* Combine the action with a budget to prevent PRs that bring the metrics below a set treshhold.
* Run the audit only on the pages affected by the PR.
* Compare the collected metrics with the actual metrics of your production site.
