# Vibek Gateway Binaries

This repository distributes prebuilt CTP gateway binaries for Vibek. The
gateway source and build workflow live in the private Vibek source repository;
this repository contains only release metadata and binary release assets.

## Install

Use the Vibek CLI. No administrator privileges or GitHub credentials are
required.

```bash
vibek gateway                 # install or verify the latest compatible release
vibek gateway 0.1.0           # install or roll back to a specific release
vibek gateway ./gateway.tar.gz # install a local archive
```

Supported release platforms:

- Ubuntu 24.04 x86_64
- Windows x64

## Release Assets

Each `gateway-vX.Y.Z` release contains:

- `vibek-gateway-linux-x64-X.Y.Z.tar.gz`
- `vibek-gateway-win32-x64-X.Y.Z.zip`
- `gateway-release.json`, the machine-readable platform and checksum index
- `SHA256SUMS`, checksums for manual verification

The archives include `ctp_gateway`, its platform CTP runtime libraries, and
`gateway-manifest.json`. GitHub's automatically generated "Source code"
archives contain only this repository's metadata, not the Vibek source tree or
CTP SDK headers.

Release notes record the exact source commit used for the build. Existing
release versions are never replaced; fixes are published under a new version.

CTP runtime libraries remain subject to their vendor's applicable terms.
