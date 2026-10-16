# umoci-binary

Builds [umoci](https://github.com/opencontainers/umoci) for Linux and macOS,
with native amd64 and arm64 build and smoke-test jobs.

Official upstream releases now provide Linux binaries. This repository remains
useful for macOS binaries, which upstream does not publish.

The Build workflow tests `v0.6.0` on pushes and pull requests. Dispatch it with a
release tag or commit and `publish=true` to publish all four verified binaries.
All jobs check out the same resolved upstream commit. Release assets include
SHA-256 sidecars and `SHA256SUMS`; existing releases are never overwritten.

The manually dispatched Build Nightly workflow builds an upstream branch or
commit and publishes `commit-<resolved-sha>` prereleases. It does not run on a
schedule. The old `version.txt` file is historical; releases themselves track
what has been published.

```bash
gh workflow run build.yml --repo tgolsson/umoci-binary \
  -f source_ref=v0.6.0 -F publish=true
```
