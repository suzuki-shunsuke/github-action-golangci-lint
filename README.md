# github-action-golangci-lint

GitHub Actions for golangci-lint.

Run golangci-lint and notify the result with reviewdog.
This GitHub Actions does **not** install golangci-lint and reviewdog, so you have to install them in advance.
It allows to install tools outside this action.
We recommend [aqua](https://aquaproj.github.io/) to install them.

## Motivation

We know there are other GitHub Actions for golangci-lint.
They install golangci-lint automatically, but we would like to manage tools with [aqua](https://aquaproj.github.io/), which is a declarative CLI Version Manager written in Go.
By aqua, you can update tools continuously with Renovate very easily and use the same tool versions in both CI and your development environment.
This GitHub Actions does **not** install golangci-lint, so we can install them outside this action.

## Requirements

* [golangci-lint](https://golangci-lint.run/)
* [reviewdog](https://github.com/reviewdog/reviewdog)

## Example

```yaml
- uses: suzuki-shunsuke/github-action-golangci-lint@v0.1.4
```

```yaml
- uses: suzuki-shunsuke/github-action-golangci-lint@v0.1.4
  with:
    github_token: ${{ secrets.GITHUB_TOKEN }}
    working_directory: foo
    timeout: 120s
```

## Inputs

### Required Inputs

Nothing.

### Optional Inputs

name | default value | description
--- | --- | ---
github_token | `github.token` | GitHub Access Token
working_directory | "" (current directory) | Woring Directory
timeout | "" (golangci-lint default timeout) | golangci-lint's `--timeout` option

## Outputs

Nothing.

## License

[MIT](LICENSE)
