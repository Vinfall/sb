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

## chromium

This originated from `extras/chromium-nosync` but nosync variant was deprecated upstream.
Just choose whatever browser you like. If you have no idea, use `extras/chromium`.

```powershell
scoop uninstall sb/chromium
scoop install extras/chromium
```

## gdsdecomp

```powershell
scoop uninstall sb/gdsdecomp
scoop install games/gdsdecomp
```

## locale-remulator

```powershell
scoop uninstall sb/locale-remulator
scoop install extras/locale-remulator
```

## lunatranslator(-latest)

```powershell
# migrate config, only if you installed sb/lunatranslator-latest
mv $env:SCOOP/persist/lunatranslator-latest $env:SCOOP/persist/lunatranslator

scoop uninstall sb/lunatranslator sb/lunatranslator-latest
scoop install extras/lunatranslator
```

## pragtical-rolling

```powershell
scoop uninstall sb/pragtical-rolling
scoop install versions/pragtical-rolling
```

## spice-guest-tools

This is NOT directly a migration, but install another (read: better) tool instead.

```powershell
sudo scoop uninstall sb/spice-guest-tools

# download only, you have to run the installer yourself
scoop download sb/virtio-win

# this is NOT recommended
# sudo scoop install sb/virtio-win -g
```

## supermium

```powershell
scoop uninstall sb/supermium
scoop install extras/supermium
```

## tsugaru

```powershell
scoop uninstall sb/tsugaru
scoop install games/tsugaru
```

## Download only

> [!NOTE]
> Migration is unnecessary as these buckets are download only.

### virtio-win(-guest-tools-){latest,stable}

```powershell
scoop cache rm sb/virtio-win-latest sb/virtio-win-stable sb/virtio-win-guest-tools-latest sb/virtio-win-guest-tools-stable

# download only, you have to run the installer yourself
scoop download sb/virtio-win
scoop download sb/virtio-win-guest-tools
```

### sarasagothic-superttc

```powershell
scoop cache rm sb/sarasagothic-superttc

# download only, you have to unpack & INSTALL FOR ALL USERS yourself
scoop download sb/sarasa-superttc
```

## Upstream binary

Not packaged in mainstream buckets.
Either maintain it in your own bucket, or download binaries from upstream.
Check `homepage` in the respective manifest.

- monitorian
- steamcloudfilemanager
- xboxdownload
