# Hugo

[![GoDoc](https://godoc.org/github.com/gohugoio/hugo?status.svg)](https://godoc.org/github.com/gohugoio/hugo)
[![Build Status](https://github.com/gohugoio/hugo/workflows/Build/badge.svg)](https://github.com/gohugoio/hugo/actions)
[![Go Report Card](https://goreportcard.com/badge/github.com/gohugoio/hugo)](https://goreportcard.com/report/github.com/gohugoio/hugo)

Hugo is a fast and modern static site generator written in Go, designed to make website creation fun again.

## Complete Documentation

See [gohugo.io](https://gohugo.io/) for complete documentation, tutorials, and theme directory.

## Quick Start

### Installation

Download pre-built binaries for Windows, macOS, and Linux from the [Releases](https://github.com/gohugoio/hugo/releases) page.

Alternatively, build from source using Go 1.21+:

```bash
CGO_ENABLED=1 go install -tags extended github.com/gohugoio/hugo@latest
```

### Build a Site

```bash
# Create a new site
hugo new site my-site
cd my-site

# Add a theme
git init
git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke.git themes/ananke
echo "theme = 'ananke'" >> hugo.toml

# Start local dev server
hugo server -D
```

## Features

- Blazing fast build times (< 1 ms per page)
- Flexible content management with Markdown and Front Matter (YAML, TOML, JSON)
- Robust multi-language and i18n support
- Built-in asset pipeline (Hugo Pipes) with Sass, PostCSS, and TypeScript support
- Native deployment targets (AWS S3, Google Cloud Storage, Azure Blob Storage)

## Contributing

We welcome contributions! Please read our [Contribution Guidelines](CONTRIBUTING.md) before submitting pull requests or opening issues.

## License

Hugo is licensed under the [Apache License 2.0](LICENSE).