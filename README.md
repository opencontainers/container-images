# container-images

A collection of container images used in CI across various
opencontainers projects.

## Images

The following table is a complete list of all images built by this repo and
links to their respective registry homepage(s):

| Name | Build Status | Project Usage | Registry Link(s) |
| ---- | ------------ | ----- | ---- |
| **pandoc** | [![GitHub Actions status](https://github.com/opencontainers/container-images/workflows/pandoc/badge.svg)](https://github.com/opencontainers/container-images/actions?query=workflow%3Apandoc) | For converting Markdown to HTML/PDF | (1) [GHCR](https://github.com/orgs/opencontainers/packages/container/package/pandoc) |
| **golangci-lint** | [![GitHub Actions status](https://github.com/opencontainers/container-images/workflows/golangci-lint/badge.svg)](https://github.com/opencontainers/container-images/actions?query=workflow%3Agolangci-lint) | For linting Go source files | (1) [GHCR](https://github.com/orgs/opencontainers/packages/container/package/golangci-lint) |

## CI

Each image has a corresponding GitHub Action workflow which can be
found in this repo at `.github/workflows/<name>.yml`.

All related files for a given image can be found at the
root of this repo under directory by the image's name (e.g. `pandoc/`).

CI will trigger for an image if any files related to the image are modified
as part of the incoming commit (including the GitHub Action .yml file itself).

As of now, the tag naming scheme is unique to each image.

## Pull Requests

When making a pull request, CI will be triggered to check that any images
related to your change will build successfully.

New images are welcome, but keep in mind that they must serve some purpose
related to CI in the opencontainers organization.

When adding a new image, please make sure to update this README and add
new GitHub Actions workflows for both `push` and `pull_request`.

