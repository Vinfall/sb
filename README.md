# Scoop Bucket

[![Test](https://github.com/Vinfall/sb/actions/workflows/test.yml/badge.svg)](https://github.com/Vinfall/sb/actions/workflows/test.yml) [![Update](https://github.com/Vinfall/sb/actions/workflows/update.yml/badge.svg)](https://github.com/Vinfall/sb/actions/workflows/update.yml)

Personal scoop bucket, `sb` for short.

## List

Developing...

- cemu-dev: `games/cemu-dev` w/o persist
- chromium: `versions/chromium-nosync` w/o persist and `--incognito` by default
- garbro-mod: crskycode's fork, original one is `extras/garbro`
- gdsdecomp: Godot reverse engineering tools
- hikarifield: Hikari Field Client
- lunatranslator: VNR-like translator, x64 only
- malware-patch: bundled version, unbundled version (cert+exe) is `extras-cn/malware-patch`
- mousejiggler: more updated than `extras/mousejiggler`, requires dotnet-7-desktopruntime
- neeview-fd: smaller than NeeView, requires dotnet-9-desktopruntime
- virtio-win(-guest-tools): virtiofs driver and guest tools
- virtualbox-guest-additions: guest additions ISO, NOT virtualbox or extension pack
- weasel

## Staged

> [!WARNING]
> These buckets are temporary, would get deleted once merged upstream.

- project64-dev
- supermium

## Deprecated

- spice-guest-tools: NOT recommended, use `virtio-win` instead

## Usage

```pwsh
scoop bucket add sb https://github.com/Vinfall/sb
scoop install sb/neeview-fd
```

## [License](LICENSE)

Some buckets are adapted/imported from other sources, please refer to the earliest commit comment.
Unless otherwise noted, my buckets are released into the public domain under the Unlicense.
Feel free to index/merge/do whatever you want.
