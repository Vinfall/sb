# Migration Guide

> [!NOTE]
> Commands here are for reference only.
> You should always make sure you understand them well before blindly following this guide.

In this guide, I assume buckets are installed locally to `$env:SCOOP` instead of globally to `$env:SCOOP_GLOBAL`.

Certain buckets cannot be installed locally due to the non-portable nature,
in such case, I would add `sudo` prefix and `-g` suffix
and you are suggested to enable built-in sudo (24H2+) or install gsudo first.

```powershell
# run in an elevated PowerShell

# install gsudo, recommended
scoop uninstall main/sudo
scoop uninstall main/sudo -g
scoop install main/gsudo -g
gsudo config PathPrecedence --global True

# OR use built-in sudo (24H2+), NOT recommended
sudo config --enable normal
```

## bulk-crap-uninstaller

```powershell
scoop uninstall sb/bulk-crap-uninstaller
scoop install extras/bulk-crap-uninstaller
```

## gdsdecomp

```powershell
scoop uninstall sb/gdsdecomp
scoop install games/gdsdecomp
```

## lunatranslator(-latest)

```powershell
# migrate config, only if you installed sb/lunatranslator-latest
mv $env:SCOOP/persist/lunatranslator-latest $env:SCOOP/persist/lunatranslator

scoop uninstall sb/lunatranslator sb/lunatranslator-latest
scoop install extras/lunatranslator
```

## spice-guest-tools

This is NOT directly a migration, but use another different (and better) tool instead.

```powershell
sudo scoop uninstall sb/spice-guest-tools

# download only, you have to run the installer yourself
scoop download sb/virtio-win

# this is NOT recommended
# sudo scoop install sb/virtio-win -g
```
