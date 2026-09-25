# Visiogen downloads

Public installation packages for Visiogen. Downloads require no GitHub account or access to the development repository.

## Install

Install [uv](https://docs.astral.sh/uv/getting-started/installation/), then run:

```powershell
uv tool install "https://github.com/ahmedmurtazamalik/visiogen-downloads/releases/download/v0.1.2/visiogen-0.1.2-py3-none-any.whl"
visiogen --help
```

If `visiogen` is not found, run `uv tool update-shell` and restart your terminal.
Python 3.11 or newer is required; uv can provision Python when needed.

## Windows desktop app

Download [Visiogen-Desktop-0.1.2-win64.zip](https://github.com/ahmedmurtazamalik/visiogen-downloads/releases/download/v0.1.2/Visiogen-Desktop-0.1.2-win64.zip), extract the whole folder, and open `Visiogen.exe`. Keep `Visiogen-worker.exe` and the `_internal` folder beside it.

The portable app requires Windows, desktop Microsoft Visio, PowerShell 7, and a signed-in Codex CLI for image-first generation. PDF workflows also require Poppler. The Generate form shows each candidate image for repair or approval before tracing. Generated VSDX files remain editable drafts to review in Visio.

## Trace an image

Native tracing requires Windows, desktop Microsoft Visio, PowerShell 7 (`pwsh`), and an authenticated Codex CLI on PATH.

```powershell
visiogen trace --input figure.png --artifact-dir artifacts/figure-trace
```

Use a new artifact directory for each run. Successful output is `artifacts/figure-trace/native/final.vsdx`; prompts, responses and previews remain in the artifact directory. Experimental output requires human review. Other commands include `generate`, `analyze`, `reconstruct`, `redraw`, `combine`, and `repair`; see `visiogen <command> --help`.

## Release contents

The wheel includes the runtime Python package, Visio template and MIT license. The desktop download is a portable application package without loose Visiogen Python source files. Neither download includes development history or benchmark inputs and reports. Public releases are snapshots; changes to the development repository become available here when a new package is published.

Release assets include `SHA256SUMS` for download verification.
