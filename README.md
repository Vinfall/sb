# Scoop Bucket

[![Test](https://github.com/Vinfall/sb/actions/workflows/test.yml/badge.svg)](https://github.com/Vinfall/sb/actions/workflows/test.yml) [![Update](https://github.com/Vinfall/sb/actions/workflows/update.yml/badge.svg)](https://github.com/Vinfall/sb/actions/workflows/update.yml)

Personal scoop bucket, `sb` for short.

## List

Developing...

- garbro-mod: crskycode's fork, official one is listed as `extras/garbro`
- gdsdecomp: Godot reverse engineering tools
- lunatranslator: VNR-like translator, x64 only
- malware-patch: this uses the bundled version, if you prefer unbundled version (cert/exe), use `extras-cn/malware-patch`
- neeview-fd: smaller than NeeView, requires dotnet-9-desktopruntime
- spice-guest-tools: NOT recommended, use `virtio-win` instead
- virtio-win(-guest-tools): virtiofs driver and guest tools
- virtualbox-guest-additions: guest additions ISO, NOT virtualbox or extension pack
- weasel

## Usage

```pwsh
scoop bucket add sb https://github.com/Vinfall/sb
scoop install sb/neeview-fd
```

## [License](LICENSE)

Some buckets are adapted/imported from other sources, please refer to the earliest commit comment.
Unless otherwise noted, my buckets are released into the public domain under the Unlicense.
Feel free to index/merge/do whatever you want.
