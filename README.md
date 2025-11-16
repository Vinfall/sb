# Scoop Bucket

[![Test](https://github.com/Vinfall/sb/actions/workflows/test.yml/badge.svg)](https://github.com/Vinfall/sb/actions/workflows/test.yml) [![Update](https://github.com/Vinfall/sb/actions/workflows/update.yml/badge.svg)](https://github.com/Vinfall/sb/actions/workflows/update.yml)

Personal scoop bucket, `sb` for short.

## Usage

```pwsh
scoop bucket add sb https://github.com/Vinfall/sb

scoop info sb/cromite
scoop download sb/garbro-mod
scoop install sb/neeview-fd
scoop uninstall sb/neeview-fd
sudo scoop install sb/procrastitracker -g
```

## List

> [!NOTE]
> As I usually test buckets locally, online version is likely outdated/buggy before changes/fixes are pushed.

- cemu-dev: `games/cemu-dev` w/o persist
- contextmenumanager: active fork of [ContextMenuManager][ContextMenuManager]
- cromite: `extras/cromite` w/ `--incognito` & manifest v2 extension support enabled and persist/translate disabled
- garbro-mod: crskycode's fork, original one is `extras/garbro`
- locale-remulator: successor of Locale-Emulator
- malware-patch: bundled version, unbundled (cert+exe) version is `extras-cn/malware-patch`
- monitorian: multi-screen brightness adjustment tool
- mousejiggler: more updated than `extras/mousejiggler`, requires dotnet-7-desktopruntime
- neeview-fd: smaller than `extras/neeview`, requires dotnet-9-desktopruntime
- np21w(-beta): Neko Project 21/W, PC-9800 Series Emulator
- nxfw: Nintendo Switch firmware, just like `games/ps3-system-software`
- palemoon-np: use installer instead of portable zip in `extras/palemoon`, download only
- procrastitracker: time tracking application
- sarasa-superttc: SuperTTC variant (24H2+), download only
- supermium: `cetacea/supermium` w/o persist and `--incognito` by default
- tsugaru: FM Towns/Marty Emulator
- virtio-win(-guest-tools): virtiofs driver and guest tools
- virtualbox-guest-additions: guest additions ISO, NOT virtualbox or extension pack
- weasel
- wumt: [winUpdateMiniTool][winUpdateMiniTool]

### Experimental

> [!WARNING]
> These buckets are NOT audited/tested, they may or may not work.
> When you use them, you are on your own.
> Expect hash errors, either fix it yourself or use `scoop install -s` to skip verification.

- eka2l1-latest: Symbian OS/N-Gage emulator
- flash: [clean-flash-builds][clean-flash-builds], Adobe Flash Player sans adware/spyware
- hikarifield: Hikari Field Client

### Staged

> [!TIP]
> These buckets are temporary, would get deleted once merged upstream.

- mame

### Deprecated

> [!NOTE]
> If you ever used these buckets, refer to [MIGRATION.md](MIGRATION.md) for migration tips.

- bulk-crap-uninstaller: smaller than `extras/bulk-crap-uninstaller`, requires dotnet-6-desktopruntime
- chromium: use `extras/cromite`, `sb/cromite` or `extras/ungoogled-chromium` instead
- gdsdecomp: use `games/gdsdecomp` instead
- lunatranslator(-latest): use `extras/lunatranslator` instead
- pragtical-rolling: use `versions/pragtical-rolling` instead
- spice-guest-tools: NOT recommended, use `virtio-win` instead
- virtio-win(-guest-tools-){latest,stable}: use `sb/virtio-win(-guest-tools)` instead

## [License](LICENSE)

Some buckets are adapted/imported from other sources, please refer to the earliest commit comment.
Unless otherwise noted, my buckets are released into the public domain under the Unlicense.
Feel free to index/merge/do whatever you want.

[ContextMenuManager]: https://github.com/BluePointLilac/ContextMenuManager
[clean-flash-builds]: https://github.com/darktohka/clean-flash-builds
[winUpdateMiniTool]: https://github.com/sergiye/winUpdateMiniTool
