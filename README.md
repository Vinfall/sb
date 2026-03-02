# Scoop Bucket

[![Test][test]][test-ci] [![Update][update]][update-ci]

Personal scoop bucket, `sb` for short.

## Usage

```pwsh
# enable autostash
scoop config autostash_on_conflict true
# add this bucket
scoop bucket add sb https://github.com/Vinfall/sb

scoop info sb/cromite
scoop download sb/garbro-mod
scoop install sb/neeview-fd
scoop uninstall sb/neeview-fd
sudo scoop install sb/procrastitracker -g
```

## List

> [!NOTE]
> As I only test buckets locally, online version is likely outdated/buggy before changes/fixes are pushed.

- assetstudiomod: aelurum's fork, original one used to be `games/assetstudio`
- bulk-crap-uninstaller: smaller than `extras/bulk-crap-uninstaller`, requires dotnet-6-desktop-runtime
- cemu-dev: `games/cemu-dev` w/o persist
- contextmenumanager: active fork of [ContextMenuManager][ContextMenuManager]
- cromite: `extras/cromite` w/ `--incognito` & manifest v2 extension support enabled and persist/translate disabled
- dotnet-{8,9,10}-desktop-runtime: .NET 8/9/10 Desktop Runtime installer, much smaller than all-in-one `versions/dotnet-{8,9,10}-sdk`, download only
- eden: use MinGW PGO build instead of MSVC in `games/eden`
- garbro-mod: crskycode's fork, original one is `extras/garbro`
- jigmo: successor of hanazono, download only
- locale-remulator: successor of Locale-Emulator
- malware-patch: bundled version, unbundled (cert+exe) version is `extras-cn/malware-patch`
- monitorian: multi-screen brightness adjustment tool
- mousejiggler: smaller than `extras/mousejiggler`
- neeview-fd: smaller than `extras/neeview`
- np21w(-beta): Neko Project 21/W, PC-9800 Series Emulator
- nxfw: Nintendo Switch firmware, just like `games/ps3-system-software`
- palemoon-np: non-portable version of `extras/palemoon`, download only
- procrastitracker: time tracking application
- sarasa-superttc: SuperTTC variant (24H2+), download only
- supermium: `cetacea/supermium` w/ `--incognito` and persist disabled
- tsugaru: FM Towns/Marty Emulator
- virtio-win(-guest-tools): virtiofs driver and guest tools
- virtualbox-guest-additions: guest additions ISO, NOT virtualbox or extension pack
- weasel
- wumt: [winUpdateMiniTool][winUpdateMiniTool]

### Experimental

> [!WARNING]
> NOT audited/tested!
> When you use them, you are on your own.
> Expect hash errors, either fix it yourself or use `scoop install -s` to skip verification.

- eka2l1-latest: Symbian OS/N-Gage emulator
- flash: [clean-flash-builds][clean-flash-builds], Adobe Flash Player sans adware/spyware
- hikarifield: Hikari Field Client

### Staged

> [!TIP]
> These buckets are temporary, would get deleted once merged upstream.

### Deprecated

> [!NOTE]
> If you ever used these buckets, refer to [MIGRATION.md](MIGRATION.md) for migration tips.

Alternatives TL;DR:

- chromium: `extras/chromium`
- gdsdecomp: `games/gdsdecomp`
- lunatranslator(-latest): `extras/lunatranslator`
- pragtical-rolling: `versions/pragtical-rolling`
- spice-guest-tools: NOT recommended, use `virtio-win` instead
- steamcloudfilemanager: download binaries from upstream
- virtio-win(-guest-tools-){latest,stable}: `sb/virtio-win(-guest-tools)`

## [License](LICENSE)

Some buckets are adapted/imported from other sources, please refer to the earliest commit comment.
Unless otherwise noted, my buckets are released into the public domain under the Unlicense.
Feel free to index/merge/do whatever you want.

[test]: https://github.com/Vinfall/sb/actions/workflows/test.yml/badge.svg
[test-ci]: https://github.com/Vinfall/sb/actions/workflows/test.yml
[update]: https://github.com/Vinfall/sb/actions/workflows/update.yml/badge.svg
[update-ci]: https://github.com/Vinfall/sb/actions/workflows/update.yml
[ContextMenuManager]: https://github.com/BluePointLilac/ContextMenuManager
[clean-flash-builds]: https://github.com/darktohka/clean-flash-builds
[winUpdateMiniTool]: https://github.com/sergiye/winUpdateMiniTool
