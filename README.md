# Scoop Bucket

[![Test][test]][test-ci] [![Update][update]][update-ci]

Personal scoop bucket, `sb` for short.

## Setup

```pwsh
# enable autostash
scoop config autostash_on_conflict true
# add this bucket
scoop bucket add sb https://github.com/Vinfall/sb
# enable more autostash
cd $env:SCOOP/buckets/sb
git config --local rebase.autoStash true
git config --local pull.rebase true
git config --local pull.autoStash true
```

## Usage

```pwsh
scoop info sb/cromite
scoop download sb/garbro-mod
scoop install sb/neeview-fd
scoop uninstall sb/neeview-fd
sudo scoop install sb/procrastitracker -g
```

## List

> [!NOTE]
> As I only test buckets locally, online version is likely outdated/buggy before changes/fixes are pushed.

Groups:

- Unique
- Mod: custom version, alternatives exist in mainstream buckets
- Download only: work best with (unreleased) `scoop-cache.nu`, without which you have to manage cache and install globally yourself

Mod:

- assetstudiomod: aelurum's fork, original one used to be `games/assetstudio`
- bulk-crap-uninstaller: smaller than `extras/bulk-crap-uninstaller`, requires dotnet-6-desktop-runtime
- cemu-dev: `games/cemu-dev` w/o persist
- cromite: `extras/cromite` w/ `--incognito` & manifest v2 extension support enabled and persist/translate disabled
- eden: use MinGW PGO build instead of MSVC in `games/eden`
- garbro-mod: crskycode's fork, original one is `extras/garbro`
- malware-patch: bundled version, unbundled (cert+exe) version is `extras-cn/malware-patch`
- mousejiggler: smaller than `extras/mousejiggler`
- neeview-fd: smaller than `extras/neeview`
- supermium: `extras/supermium` w/ `--incognito` enabled and persist disabled

Unique:

- contextmenumanager: active fork of [ContextMenuManager][ContextMenuManager]
- hikarifield: Hikari Field Client
- locale-remulator: successor of Locale-Emulator
- np21w(-beta): Neko Project 21/W, PC-9800 Series Emulator
- procrastitracker: time tracking application
- tsugaru: FM Towns/Marty Emulator
- virtualbox-guest-additions: guest additions ISO, NOT virtualbox or extension pack
- weasel
- wumt: [winUpdateMiniTool][winUpdateMiniTool]

Download only:

- dotnet-{8,9,10}-desktop-runtime: .NET 8/9/10 Desktop Runtime installer, much smaller than all-in-one `versions/dotnet-{8,9,10}-sdk`
- flash: [clean-flash-builds][clean-flash-builds], Adobe Flash Player sans adware/spyware
- jigmo: successor of hanazono
- nxfw: Nintendo Switch firmware, just like `games/ps3-system-software`
- palemoon-np: non-portable version of `extras/palemoon`
- sarasa-superttc: SuperTTC variant (24H2+)
- virtio-win(-guest-tools): virtiofs driver and guest tools

### Experimental

> [!WARNING]
> NOT audited/tested!
> When you use them, you are on your own.

- eka2l1-latest: Symbian OS/N-Gage emulator

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
