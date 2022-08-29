# npm-publish

Composite GitHub action that publishes to npm and [creates a GitHub release](https://github.com/ArnaudBarre/github-release) to reduce boilerplate in GitHub workflows.

## Usage

First, [add a repository secret](https://docs.github.com/en/actions/security-guides/encrypted-secrets#creating-encrypted-secrets-for-a-repository) named `NPM_TOKEN`. Use an `automation` token from your [npm](https://www.npmjs.com/) account.

```yml
steps:
  - uses: actions/checkout@v2
  # install & build if needed
  - uses: ArnaudBarre/npm-publish@v1
    with:
      npm-token: ${{ secrets.NPM_TOKEN }}
      # working-directory: dist
```
