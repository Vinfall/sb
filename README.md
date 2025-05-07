# Scoop Bucket

[![Test](https://github.com/Vinfall/sb/actions/workflows/test.yml/badge.svg)](https://github.com/Vinfall/sb/actions/workflows/test.yml) [![Update](https://github.com/Vinfall/sb/actions/workflows/update.yml/badge.svg)](https://github.com/Vinfall/sb/actions/workflows/update.yml)

Personal scoop bucket, `sb` for short.

## Usage

```pwsh
scoop bucket add sb https://github.com/Vinfall/sb
scoop install sb/neeview-fd
```

## List

Developing...

- cemu-dev: `games/cemu-dev` w/o persist
- chromium: `versions/chromium-nosync` w/o persist and `--incognito` by default
- contextmenumanager: active fork of [ContextMenuManager][ContextMenuManager]
- garbro-mod: crskycode's fork, original one is `extras/garbro`
- gdsdecomp: Godot reverse engineering tools
- lunatranslator: VNR-like translator, x64 only
- malware-patch: bundled version, unbundled version (cert+exe) is `extras-cn/malware-patch`
- monitorian: multi-screen brightness adjustment tool
- mousejiggler: more updated than `extras/mousejiggler`, requires dotnet-7-desktopruntime
- neeview-fd: smaller than `extras/neeview`, requires dotnet-9-desktopruntime
- virtio-win(-guest-tools): virtiofs driver and guest tools
- virtualbox-guest-additions: guest additions ISO, NOT virtualbox or extension pack
- weasel

### Experimental

> [!WARNING]
> These buckets are NOT audited/tested, they may or may not work.
> When you use them, you are on your own.

- hikarifield: Hikari Field Client
- procrastitracker: Windows time tracking application
- virtio-win-(guest-tools-)?{latest,stable}

### Staged

> [!TIP]
> These buckets are temporary, would get deleted once merged upstream.

- project64-dev
- supermium

### Deprecated

- spice-guest-tools: NOT recommended, use `virtio-win` instead

## [License](LICENSE)

Some buckets are adapted/imported from other sources, please refer to the earliest commit comment.
Unless otherwise noted, my buckets are released into the public domain under the Unlicense.
Feel free to index/merge/do whatever you want.

[ContextMenuManager]: https://github.com/BluePointLilac/ContextMenuManager
