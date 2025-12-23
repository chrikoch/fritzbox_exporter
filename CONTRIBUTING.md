# Contributing to fritzbox_exporter

## Development

### Building with Go

To build the project locally using Go:

```bash
go build
```

### Building with Docker

To build the project locally using Docker

```bash
docker build -t fritzbox_exporter .
docker run -p 9133:9133 fritzbox_exporter
```

## Releases

This project uses [GoReleaser](https://goreleaser.com/) and GitHub Actions to automate the release process of binaries and Docker images.

### How to trigger a new release

Releases are triggered by pushing a new Git tag. 

1. **Check your current version**:
   Ensure you are on the `main` branch and have the latest changes.

2. **Create a new tag**:
   Tags should follow semantic versioning (e.g., `v1.0.0`).
   ```bash
   git tag -a v1.2.3 -m "Release description"
   ```

3. **Push the tag**:
   Pushing the tag to GitHub will trigger the `Release` workflow.
   ```bash
   git push origin v1.2.3
   ```