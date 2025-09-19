# 🚀 static-php

<div align="center">

[![Latest Release](https://img.shields.io/github/v/release/rodrigodotdev/php?sort=semver&style=for-the-badge&logo=php&logoColor=white)](https://github.com/rodrigodotdev/php/releases)
[![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/rodrigodotdev/php/php-versions.yml?style=for-the-badge&logo=github&label=Auto%20Discovery)](https://github.com/rodrigodotdev/php/actions)
[![License](https://img.shields.io/github/license/rodrigodotdev/php?style=for-the-badge)](LICENSE)
[![Downloads](https://img.shields.io/github/downloads/rodrigodotdev/php/total?style=for-the-badge&logo=download&logoColor=white)](https://github.com/rodrigodotdev/php/releases)

**🐘 Prebuilt static PHP CLI binaries made simple**

_Zero compilation. Zero dependencies. Zero hassle._

</div>

## ✨ Features

🔄 **Automated Discovery** - Daily scans for new PHP versions  
📦 **Clean Releases** - Consistent filenames and organized downloads  
🔒 **Verified Downloads** - SHA256 checksums for every binary  
🌍 **Cross-Platform** - Linux, macOS & Windows support  
📊 **Machine Readable** - JSON manifest for automation  
⚡ **Zero Dependencies** - Static binaries, no system requirements

> 📝 **Source**: Re-packaged from [crazywhalecc/static-php-cli](https://github.com/crazywhalecc/static-php-cli)</div>

## 🛠️ Supported Platforms

| Platform   | Architecture    | Extension | Example                          |
| ---------- | --------------- | --------- | -------------------------------- |
| 🐧 Linux   | x86_64, aarch64 | `.tar.gz` | `php-8.4.12-linux-x86_64.tar.gz` |
| 🍎 macOS   | x86_64, arm64   | `.tar.gz` | `php-8.4.12-macos-arm64.tar.gz`  |
| 🪟 Windows | x64             | `.zip`    | `php-8.4.12-windows-x64.zip`     |

## 🔄 How It Works

### 📡 Daily Discovery (`php-versions.yml`)

- 🕛 Runs daily at midnight UTC
- 🔍 Scans upstream directories (`bulk/` + `windows/spc-max/`)
- 📅 Identifies artifacts modified in the last 48 hours
- 🚀 Auto-dispatches release jobs for new versions

### 📦 Release Creation (`php-release.yml`)

- ⬇️ Downloads all platform variants for the version
- 🏷️ Renames to consistent format: `php-<VERSION>-<ARCH>.<ext>`
- 🔐 Generates `SHASUMS256.txt` for integrity verification
- 📄 Creates `manifest.json` with metadata
- 🎯 Publishes as GitHub Release tagged `v<version>`

> **⚠️ Important**: Binaries are **not modified** - only renamed and bundled for consistency.

## 🚀 Quick Start

### 📦 With Package Managers

#### `mise` + `ubi` (Recommended)

```bash
# Latest 8.4.x series
mise use ubi:rodrigodotdev/php@8.4

# Specific version
mise use ubi:rodrigodotdev/php@8.4.12
php -v
```

## 🐛 Getting Help

- 📝 [Open an issue](https://github.com/rodrigodotdev/php/issues) for bugs or feature requests
- 💬 Check [existing issues](https://github.com/rodrigodotdev/php/issues?q=is%3Aissue) for solutions
- 📚 Refer to [upstream documentation](https://github.com/crazywhalecc/static-php-cli) for PHP-specific questions

## 🤝 Contributing

We welcome contributions! Here's how you can help:

- 🐛 **Report bugs** - Found an issue? Let us know!
- 💡 **Suggest features** - Have ideas for improvements?
- 📖 **Improve documentation** - Help make this README even better
- 🔧 **Submit PRs** - Fix bugs or add new features

### Development Setup

```bash
# Fork and clone the repository
git clone https://github.com/your-username/static-php.git
cd static-php

# The workflows run automatically, but you can test locally:
# 1. Modify .github/workflows/*.yml
# 2. Test with act (GitHub Actions runner)
act -j create-php-release -s GITHUB_TOKEN
```

## 📜 License

This project is licensed under the [MIT License](LICENSE).

**Upstream Sources:**

- [crazywhalecc/static-php-cli](https://github.com/crazywhalecc/static-php-cli) - Original static PHP binaries
- [The PHP Group](https://www.php.net/) - PHP programming language

---

<div align="center">

**⭐ Star this repo if it helped you!**

Made with ❤️ by [@rodrigodotdev](https://github.com/rodrigodotdev)

</div>
