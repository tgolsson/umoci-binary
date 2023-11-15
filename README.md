# umoci-binary

[![Build](https://github.com/tgolsson/umoci-binary/actions/workflows/build.yml/badge.svg?branch=main)](https://github.com/tolsson/umoci-binary/actions/workflows/build.yml)

Generate [umoci](https://github.com/opencontainers/umoci) binaries.

## Useage

The [release](https://github.com/tgolsson/umoci-binary/releases) version of the project is the same as the [umoci](https://github.com/opencontainers/umoci/releases) release version, which can be viewed directly on the [ release](https://github.com/tgolsson/umoci-binary/releases) page directly.

```bash
version=v1.6.2
arch=amd64
[ -f /usr/bin/umoci ] && mv /usr/bin/umoci{,_src}
wget https://github.com/tgolsson/umoci-binary/releases/download/${version}/umoci-linux-${arch} -O /usr/bin/umoci
chmod +x /usr/bin/umoci
```
