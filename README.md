# Reusable Actions for EnVRonment

This repository contains a collection of [reusable actions](https://docs.github.com/en/actions/using-workflows/reusing-workflows) for EnVRonment.

## Available Actions

- [Release Please](./.github/workflows/release-please.yml)

This action is used to automatically create a new release PR when a commit is pushed to the dev branch.

### Usage

```yaml
release-please:
  uses: Streetless/actions/.github/workflows/release-please.yml@main
  with:
    runs-on: "self-hosted" # Optional
    committer-email: "47529956+alwyn974@users.noreply.github.com" # Optional
    committer-name: "alwyn974" # Optional
  secrets: inherit
  # or
  secrets:
    APP_ID: ${{ secrets.APP_ID }}
    PRIVATE_KEY: ${{ secrets.PRIVATE_KEY }}
```
