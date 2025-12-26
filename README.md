# git-bump

A simple CLI tool to create auto-incrementing daily build tags.

## Installation

```bash
# Clone and install
git clone https://github.com/shigma/git-bump.git
cp git-bump/git-bump ~/.local/bin/
chmod +x ~/.local/bin/git-bump

# Now you can use it as a git subcommand
git bump
```

## Usage

```bash
git bump [OPTIONS] [SUFFIX]
```

Creates tags in format: `build-YYYYMMDD.n[-suffix]`

### Examples

```bash
git bump                  # build-20250110.0
git bump                  # build-20250110.1 (auto-increment)
git bump beta             # build-20250110.2-beta
git bump --dry-run        # Preview without creating
```

### Options

| Option | Description |
|--------|-------------|
| `-n, --dry-run` | Preview tag without creating |
| `-v, --verbose` | Show detailed output |
| `-s, --skip-confirm` | Skip confirmation for existing tags |
| `-f, --force-branch` | Allow on non-main branches |
| `-h, --help` | Show help |

## License

MIT
