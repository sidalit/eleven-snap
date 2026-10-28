<div align="center">

<img src="snap/gui/eleven.png" alt="Eleven logo" width="128" />

# Eleven

**A native reverse-engineering workbench with AI agents.**

[![eleven](https://snapcraft.io/eleven/badge.svg)](https://snapcraft.io/eleven)
[![Base: core26](https://img.shields.io/badge/Base-core26-2C8C3C?logo=canonical&logoColor=white)](https://snapcraft.io/core26)
![Confinement: strict](https://img.shields.io/badge/Confinement-strict-2C8C3C)
[![Maintainer: sidaliteir](https://img.shields.io/badge/Maintainer-sidaliteir-2C8C3C?logo=snapcraft&logoColor=white)](https://snapcraft.io/publisher/sidaliteir)
![Architecture: amd64](https://img.shields.io/badge/Architecture-amd64-2C8C3C?logo=linux&logoColor=white)

[Getting Started](#getting-started) · [Configure](#configure) · [Limitations](#limitations) · [Build](#build) · [Support](#support) · [License](#license)

Unofficial snap packaging for [Eleven](https://github.com/Zfinix/eleven), a desktop application for inspecting binaries, decompiling Android apps and working with ACP agents.

</div>

---

## Getting Started

<a href="https://snapcraft.io/eleven"><img alt="Get it from the Snap Store" src="https://snapcraft.io/en/dark/install.svg" width="180"></a>

```bash
sudo snap install eleven
eleven
```

Launch from the terminal or your application menu. Ghidra, Rizin, REA, Java, jadx and apktool are included.

## Configure

Choose and sign in to an agent in the app. Agent downloads and settings stay inside the snap; there are no `snap set` options.

| Optional access | Command |
| --- | --- |
| Files on removable storage | `sudo snap connect eleven:removable-media` |

## Limitations

- Linux amd64 only, matching upstream's native UI support.
- Host-installed agents and their credentials are not imported. The built-in terminal runs inside the snap.
- Host process debugging, external IDA/Hopper installations and macOS-specific tooling are unavailable.
- Use Ghidra for pseudocode; Rizin's optional decompiler plugin is not included.
- Open files from accessible home folders or connected removable storage. Application updates are managed by snapd.

## Build

```bash
git clone https://github.com/sidalit/eleven-snap.git
cd eleven-snap
sudo snap install snapcraft --classic
snapcraft pack
```

The native UI is compiled from source and requires a substantial Rust build.

## Support

- **Installation or snap issues:** [open a packaging issue](https://github.com/sidalit/eleven-snap/issues).
- **Application bugs:** [report them upstream](https://github.com/Zfinix/eleven/issues).

## License

Snap packaging: [MIT](https://github.com/sidalit/eleven-snap/blob/main/LICENSE).
