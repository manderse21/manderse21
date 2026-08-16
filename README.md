# Mike Andersen

I build developer tooling for PowerShell -- static analysis that runs where the
code is being written, rather than as a separate lint step afterwards.

## claude-powershell-lsp

Real-time PowerShell diagnostics and PSScriptAnalyzer fixes inside Claude Code,
as it edits your `.ps1` / `.psm1` / `.psd1`. Built on PowerShell Editor Services.

```
/plugin marketplace add manderse21/claude-powershell-lsp
/plugin install powershell-lsp
```

27 releases. GPL-3.0. Every tag ships a CycloneDX SBOM and a Sigstore keyless
signature, and [TRUST.md](https://github.com/manderse21/claude-powershell-lsp/blob/main/TRUST.md)
states plainly what those attestations do *not* prove.

## Technical focus

- PowerShell static analysis -- PSScriptAnalyzer rule curation, false-positive
  rate measured against a fixed corpus, SARIF output
- Language Server Protocol integration, and how agent hosts drive a language
  server in practice
- Windows-first tooling -- PowerShell 5.1 and 7.x semantics, encoding and
  codepage behaviour, process lifecycle hygiene

## How I work

- Upstream first. Bugs get filed and fixed at the source when that is where
  they belong -- PowerShell Editor Services #2297 and #2300, and a handful in
  Claude Code.
- Releases are reproducible and signed; third-party actions are pinned to
  commit SHAs; CI gates every merge.
- Limits get documented as carefully as capabilities. If a claim is not
  measured, it does not get made.

## Contact

An issue on the relevant repository is the fastest route to me.
