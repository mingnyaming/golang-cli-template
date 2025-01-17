# golang-cli-template
A general purpose project template for golang CLI applications

<!--ts-->
   * [golang-cli-template](#golang-cli-template)
   * [Features](#features)
   * [Project Layout](#project-layout)
   * [How to use this template](#how-to-use-this-template)
   * [Demo Application](#demo-application)
   * [Makefile Targets](#makefile-targets)
   * [Contribute](#contribute)

<!-- Added by: morelly_t1, at: Tue 10 Aug 2021 08:54:24 AM CEST -->

<!--te-->

[![Test](https://github.com/FalcoSuessgott/golang-cli-template/actions/workflows/test.yml/badge.svg)](https://github.com/FalcoSuessgott/golang-cli-template/actions/workflows/test.yml) [![golangci-lint](https://github.com/FalcoSuessgott/golang-cli-template/actions/workflows/lint.yml/badge.svg)](https://github.com/FalcoSuessgott/golang-cli-template/actions/workflows/lint.yml) [![Go Report Card](https://goreportcard.com/badge/github.com/FalcoSuessgott/golang-cli-template)](https://goreportcard.com/report/github.com/FalcoSuessgott/golang-cli-template) [![Go Reference](https://pkg.go.dev/badge/github.com/FalcoSuessgott/golang-cli-template.svg)](https://pkg.go.dev/github.com/FalcoSuessgott/golang-cli-template) [![codecov](https://codecov.io/gh/FalcoSuessgott/golang-cli-template/branch/main/graph/badge.svg?token=Y5K4SID71F)](https://codecov.io/gh/FalcoSuessgott/golang-cli-template)

This template serves as a starting point for golang commandline applications it is based on golang projects that I consider high quality and various other useful blog posts that helped me understanding golang better.

# Features
- [goreleaser](https://goreleaser.com/) with `deb.` and `.rpm` package releasing
- [golangci-lint](https://golangci-lint.run/) for linting and formatting
- [Github Actions](.github/worflows) Stages (Lint, Test, Build, Release)
- [Gitlab CI](.gitlab-ci.yml) Configuration (Lint, Test, Build, Release)
- [cobra](https://cobra.dev/) example setup including tests
- [Makefile](Makefile) - with various useful targets and documentation (see Makefile Targets)
- [Github Pages](_config.yml) using [jekyll-theme-minimal](https://github.com/pages-themes/minimal) (checkout [https://falcosuessgott.github.io/golang-cli-template/](https://falcosuessgott.github.io/golang-cli-template/))
- [pre-commit-hooks](https://pre-commit.com/) for formatting and validating code before committing

# Project Layout
* [assets/](https://pkg.go.dev/github.com/FalcoSuessgott/golang-cli-template/assets) => docs, images, etc
* [cmd/](https://pkg.go.dev/github.com/FalcoSuessgott/golang-cli-template/cmd)  => commandline configurartions (flags, subcommands)
* [pkg/](https://pkg.go.dev/github.com/FalcoSuessgott/golang-cli-template/pkg)  => packages that are okay to import for other projects
* [internal/](https://pkg.go.dev/github.com/FalcoSuessgott/golang-cli-template/pkg)  => packages that are only for project internal purposes

# How to use this template
```sh
bash <(curl -s https://raw.githubusercontent.com/FalcoSuessgott/golang-cli-template/main/install.sh)
```

# Demo Application

```sh
$> golang-cli-template
golang-cli project template demo application

Usage:
  golang-cli-template [flags]
  golang-cli-template [command]

Available Commands:
  example     example subcommand which adds or multiplies two given integers
  help        Help about any command
  version     Displays d4sva binary version

Flags:
  -h, --help   help for golang-cli-template

Use "golang-cli-template [command] --help" for more information about a command.
```

```sh
$> golang-cli-template example 2 5 -a
7

$> golang-cli-template example 2 5 -m
10
```

# Makefile Targets
```sh
$> make
build                          build golang binary
clean                          clean up environment
cover                          display test coverage
docker-build                   dockerize golang application
fmtcheck                       run gofmt and print detected files
fmt                            format go files
help                           list makefile targets
install                        install golang binary
lint-fix                       fix
lint                           lint go files
pre-commit                     run pre-commit hooks
run                            run the app
test                           run go tests
```

# Contribute
If you find issues in that setup or have some nice features / improvements, I would welcome an issue or a PR :)
