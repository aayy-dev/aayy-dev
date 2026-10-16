<p align="center">
  <img src="assets/header.png" alt="aay." width="100%">
</p>

<p align="center"><b>AI-driven development · Linux &amp; Android internals · iOS tweaks · homelab · finance automation</b></p>

I build tools for the phones, computers and systems I use every day, working alongside AI coding agents: I scope the problem, the agent drafts and runs, and I test and verify what ships. Most of my work sits close to the OS: jailbreak tweaks, Android system modules, custom ROMs, bootloaders and build pipelines.

## Projects

- **[TopRow](https://github.com/aayy-dev/TopRow)**: a number and symbol row for the stock iOS keyboard, with every key customisable and changes applied live. Rootless jailbreak tweak in Objective-C and Swift (Theos). ★5
- **[recents-clear-all](https://github.com/aayy-dev/recents-clear-all)**: an LSPosed/Xposed module that adds an always-visible "Clear all" button to Pixel Launcher's Overview. Java, published on the LSPosed module repository.
- **[aay apt repo](https://dev.rtrdd.fyi)**: a signed APT repository serving my iOS packages to Sileo, Zebra and Cydia. A build script generates the package index, native and HTML depictions, and the signed `InRelease`. ([source](https://github.com/aayy-dev/aayy-dev.github.io))
- **[llama.cpp CI](https://github.com/aayy-dev/llama.cpp/tree/ci)**: a self-hosted GitHub Actions runner that tracks upstream llama.cpp and builds the CPU, CUDA 13 and Vulkan backends on Windows, while the fork's `master` stays a clean mirror that always syncs.

## Upstream contributions

- [RichardLuo0/global-icon-pack-android#165](https://github.com/RichardLuo0/global-icon-pack-android/pull/165): fixed three Android 16 bugs (merged)
- [BuSung-dev/Root-My-Galaxy-Payloads#290](https://github.com/BuSung-dev/Root-My-Galaxy-Payloads/pull/290): Galaxy S25 FE device profile, tested on hardware (open)

## Beyond GitHub

Work that lives on my own machines rather than in public repos:

- **Ubuntu Touch on a Pixel 3a**: replaced the stock 3 GB read-only root filesystem with a ~30 GB writable one. The key finding was that the bootloader picks the root partition by name, not UUID, so the fix was to clone the rootfs onto a new partition and rename it. Scripted as a one-shot recovery job, with a write-up.
- **Custom ROM bootloop forensics**: traced repeated bootloops on a Galaxy S9 running a custom Android 15 ROM to Play system updates that assume a newer kernel (eBPF/BTF) and a changed library ABI. Recovered and hardened the device without reflashing.
- **Hackintosh and multi-boot**: OpenCore on a Ryzen 7 5700X3D with a Radeon RX 580, plus OCLP and macOS / Windows / Debian multi-boot on older Macs.
- **Homelab and Linux**: Debian servers, a Caddy reverse proxy, self-hosted remote desktop, and SSH-based automation.
- **Finance automation (FP&A day job)**: VB.NET business rules in OneStream that replace a manual reporting workbook and are validated against it, plus Python pipelines that clean Excel exports for loading, with built-in total checks.
- **Personal data pipelines**: deduplicated a 90 GB, 14,000-file music library using SHA-256 hashes while keeping streaming-app playlists intact; built a pipeline that mines thousands of exported AI conversations into an evidence log for my annual review.

## How I work

AI coding agents (mainly Claude Code) are a core part of how I build, and I own the review and verification. A recent example: moving this account to a new username. That meant rewriting commit identities across 25 repositories while leaving upstream and signed commits byte-identical, pausing CI during the force-pushes, rebuilding and re-signing the apt repo, and generating this brand kit from code. Commits made in those sessions carry a `Claude-Session:` trailer.

## Toolbox

**Languages:** Objective-C · Swift · Java · Kotlin · Python · VB.NET · SQL · Bash · PowerShell

**Platforms and tools:** Theos · Xposed/LSPosed · KernelSU · OpenCore · GitHub Actions · Linux · Power BI · Excel/VBA
