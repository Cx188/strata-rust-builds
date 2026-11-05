# StrataMC in Rust: builds

Release packages for **StrataMC in Rust**, the experimental Minecraft 26.3 runtime in the
[Strata Launcher](https://github.com/Cx188). **Powered by [Horizon](https://github.com/horizon-rust/horizon).**

You don't download anything from here by hand: the Strata Launcher fetches these packages, checks
Strata's signature and every file's SHA-256, and installs them. Packages that fail any check are never used.

## What a release contains

| Asset | What it is |
|---|---|
| `strata-rust-<build>-windows-x64.zip` | `horizon-client.exe` built from Horizon's source with Strata's small built-in extension (credit, About page, own badge), plus Horizon's support files byte-identical to Horizon's signed release, `LICENSE`, `NOTICE` and `composition.json` (every file's hash). |
| `rust-channel.json` + `rust-channel.json.sig` | The signed note that tells launchers which build is current. |

Minecraft itself is **not** in these packages. The launcher uses the player's own Minecraft 26.3
files from Mojang (the same files Strata downloads for Java instances) and prepares Horizon's game data
on the player's PC.

## Source

- Horizon engine: exact upstream commit named in each release and in `composition.json`.
- Strata extension: built from Strata's own source; the commit is named in `composition.json`.

## Licenses

Horizon is MIT-licensed; see [`LICENSE-HORIZON`](LICENSE-HORIZON). Strata's extension is proprietary
to Strata. Minecraft is a trademark of Mojang Studios.

**StrataMC in Rust is not affiliated with or endorsed by Horizon, Mojang or Microsoft.**
