# Visiogen downloads

Public installation packages for Visiogen. Downloads require no GitHub account or access to the development repository.

## Install

Install [uv](https://docs.astral.sh/uv/getting-started/installation/), then run:

```powershell
uv tool install "https://github.com/ahmedmurtazamalik/visiogen-downloads/releases/download/v0.1.0/visiogen-0.1.0-py3-none-any.whl"
visiogen --help
```

If `visiogen` is not found, run `uv tool update-shell` and restart your terminal.
Python 3.11 or newer is required; uv can provision Python when needed.

## Trace an image

Native tracing requires Windows, desktop Microsoft Visio, PowerShell 7 (`pwsh`), and an authenticated Codex CLI on PATH.

```powershell
visiogen trace --input figure.png --artifact-dir artifacts/figure-trace
```

Use a new artifact directory for each run. Successful output is `artifacts/figure-trace/native/final.vsdx`; prompts, responses and previews remain in the artifact directory. Experimental output requires human review. Other commands include `generate`, `analyze`, `reconstruct` and `redraw`; see `visiogen <command> --help`.

## Release contents

The wheel includes the runtime Python package, Visio template and MIT license. It does not include development history or benchmark inputs/reports. Public releases are snapshots; changes to the development repository become available here when a new package is published.

The v0.1.0 package was built from development commit `185942c` on 14 September 2026. Release assets include `SHA256SUMS` for download verification.
