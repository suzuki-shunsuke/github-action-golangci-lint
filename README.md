# github-action-golangci-lint

GitHub Actions for golangci-lint.

## Requirements

* [golangci-lint](https://golangci-lint.run/)
* [reviewdog](https://github.com/reviewdog/reviewdog)

## Example

```yaml
# Install golangci-lint and reviewdog with aqua
- uses: int128/aqua-action@v1
  with:
    version: v0.7.9 # renovate: depName=suzuki-shunsuke/aqua

- uses: suzuki-shunsuke/github-action-golangci-lint@v0.1.0
```

## License

[MIT](LICENSE)
