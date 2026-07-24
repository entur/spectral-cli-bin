# spectral-cli-bin
Building executables of the [stoplightio/spectral](https://github.com/stoplightio/spectral) OpenAPI linter for use primarily in CI/CD workflows. Uses release-please to create Github releases, and then attaches built executables to the release.

## Why?
Entur uses [stoplightio/spectral](https://github.com/stoplightio/spectral) to lint OpenAPI specs. It is used in Github reusable workflows [entur/gha-api](https://github.com/entur/gha-api). The recommended way of running Spectral is to download it from npm and run the script. However, we would like to avoid being dependent on npm during runtime execution of workflows, both for security and performance. Spectral does provide their own release binaries, but this is not ideal either, as we want to be able to patch dependency versions in case of vulnerabilities. 
