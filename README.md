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
    target-branch: "dev" # Optional
    default-branch: "main" # Optional
    config-file: ".release-please-config.json" # Optional
    manifest-file: ".release-please-manifest.json" # Optional
    runs-on: "['self-hosted']" # Optional
    use-root-gitflow: true # Optional
    use-docs-gitflow: true # Optional
    committer-email: "47529956+alwyn974@users.noreply.github.com" # Optional
    committer-name: "alwyn974" # Optional
    node-version: "20.x" # Optional
  secrets: inherit
  # or
  secrets:
    APP_ID: ${{ secrets.APP_ID }}
    PRIVATE_KEY: ${{ secrets.PRIVATE_KEY }}
```

- [Todo](./.github/workflows/todo.yml)

This action is used to automatically create a new issue when a commit containing the word `todo` or `fixme` is pushed to a branch.

### Usage

```yaml
todo:
  uses: Streetless/actions/.github/workflows/todo.yml@main
  with:
    runs-on: "self-hosted" # Optional
```

- [Docs](./.github/workflows/docs.yml)

This action is used to automatically build and deploy the documentation when a commit is pushed to the main branch.

### Usage

```yaml
docs:
  uses: Streetless/actions/.github/workflows/docs.yml@main
  with:
    deploy:
      default-branch: "main" # Optional
      runs-on: "['self-hosted']" # Optional
      node-version: "21.x" # Optional
      working-directory: "docs" # Optional
      committer-email: "47529956+alwyn974@users.noreply.github.com" # Optional
      committer-name: "alwyn974" # Optional
```
