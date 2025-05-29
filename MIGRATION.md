# Migration Guide

> [!NOTE]
> Commands here are for reference only.
> You should always make sure you understand them well before blindly following this guide.

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

## lunatranslator

```powershell
# migrate config
mv $env:SCOOP/persist/lunatranslator $env:SCOOP/persist/lunatranslator-latest

scoop uninstall sb/lunatranslator
scoop install sb/lunatranslator-latest
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
