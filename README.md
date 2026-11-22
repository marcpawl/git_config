# git_config

Small utility for configuring global Git settings interactively.

## Files

- `config_git`: Python script that applies configured global Git settings.

## Usage

```bash
./config_git --help
./config_git
```

## Behavior

For each configured setting, `config_git`:

1. Describes what the setting does.
2. Shows the desired value.
3. Reads the current global Git value.
4. If the setting is missing, installs it.
5. If the setting differs, shows the current and desired values and asks
   whether to update it.
6. If the setting already matches, leaves it unchanged.

## Current settings

### `alias.vdiff`

- **Value**: `difftool -t meld -d`
- **Purpose**: Run `meld` to show the same contents that `git diff` would
  show.
- **Examples**:

```bash
git vdiff
git vdiff HEAD~1
```
