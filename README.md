# ARC-RAIDERS-Kattle-E3-FULL-GUIDE-FPS-TWEAKS
# ARC-RAIDERS — Kattle E3 Full Guide (FPS + Latency Tweaks) 🛠️🎮

**Goal:** maximize **FPS**, improve **frame pacing**, and reduce **input / network latency** for **ARC Raiders** on Windows (without placebo or unsafe “tweak packs”).

This repo is a **structured, step-by-step guide** + optional scripts you can review and run yourself.

> **Disclaimer (read):** Use at your own risk. Some changes are system-level. I strongly recommend you create a restore point and document your baseline before applying anything.  
> This is **fan-made** and not affiliated with ARC Raiders / Embark.

---

## Table of Contents
- [1) What this guide covers](#1-what-this-guide-covers)
- [2) Before you tweak](#2-before-you-tweak)
- [3) Quick Start (high impact, low risk)](#3-quick-start-high-impact-low-risk)
- [4) Full Tweak List (organized)](#4-full-tweak-list-organized)
- [5) Tools used in this guide](#5-tools-used-in-this-guide)
- [6) Benchmarking (so you know it worked)](#6-benchmarking-so-you-know-it-worked)
- [7) Reverting changes](#7-reverting-changes)
- [8) Credits](#8-credits)

---

## 1) What this guide covers
This repo focuses on **real-world performance**:
- Higher and more stable FPS (less stutter)
- Better 1% / 0.1% lows (frame pacing)
- Lower input latency (mouse + keyboard)
- Cleaner Windows background overhead
- Sensible network latency improvements

This guide **does not** include:
- “Magic” registry dumps with unknown effects
- Disabling core security permanently
- Anything that violates game ToS

---

## 2) Before you tweak
### Create safety backups (do this first)
- **Create a Restore Point**
- **Export key settings** you change (NVIDIA profile, registry keys you edit, config files)
- Take screenshots of:
  - NVIDIA Control Panel settings
  - In-game video settings
  - Windows power plan

### Baseline your performance
Before touching anything, record:
- Average FPS
- 1% lows / 0.1% lows
- Stutter points (when/where it happens)
- GPU usage / CPU usage
- Temps + clocks

If you skip this step, you will never know what actually helped.

---

## 3) Quick Start (high impact, low risk)
If you only do a few things, do these in order:

1. **Update GPU driver (clean install if needed)**
2. **Enable Ultimate Performance power plan**
3. **Turn ON Game Mode** + **turn OFF Game Bar captures**
4. **Disable unnecessary Startup Apps**
5. **Clean Windows temp files + component store**
6. **ISLC (Intelligent Standby List Cleaner)** for better lows (if you stutter)
7. **NVIDIA Control Panel** (basic performance/latency setup)
8. **ARC Raiders in-game settings** (balanced for stable lows)
9. **Steam launch options** (if applicable) + game file properties tweaks

---

## 4) Full Tweak List (organized)

### A) System Cleaning (safe, measurable)
- Clean Temp  
- Clean the Recycle Bin  
- Clean Windows Update Cache  
- Clear Prefetch Cache *(only if troubleshooting stutter; don’t spam this daily)*  
- Clean System Image & Component Store  
- SFC Scan (check & fix corrupt system files)  
- Clear Windows Event Logs *(optional maintenance)*  
- Clean Windows Installer Cache *(only via safe methods; do not delete blindly)*  

**Why it matters:** less junk, fewer update leftovers, fewer corrupted files, fewer background issues.

---

### B) Network & DNS (safe if done correctly)
- Clear DNS  
- Flush Network Cache  
- Network Latency Tweaks (TCP Optimizer style — **conservative settings only**)  
- DNS tweaks *(choose stable + low-latency DNS for your region)*  
- Defender Firewall *(see Security section below — don’t disable permanently)*  

**Notes:**
- “Aggressive” TCP changes often cause hit-reg issues, packet loss, or worse latency. This guide favors **stability first**.

---

### C) Windows Performance Settings (high impact, low risk)
- Disable Background Apps (PowerShell) *(targeted; not “disable everything”)*  
- Display settings  
- Notifications  
- Startup Apps  
- Uninstall unnecessary apps  
- Turn On Game Mode  
- Turn Off Game Bar  
- Hardware-accelerated GPU scheduling *(test ON vs OFF; keep what benchmarks better)*  
- High Graphics settings (Windows Graphics Settings per-app)  
- Advanced System Settings (performance options)  
- Background Settings  

---

### D) Power & System Scheduling (high impact)
- Ultimate Performance power plan  
- msconfig *(only for troubleshooting; don’t “debloat” services randomly)*  
- Security and Maintenance *(keep system healthy; fix warnings)*  

---

### E) Input Latency (mouse + keyboard)
- Mouse Input Lag Fix (Registry) *(targeted, reversible)*  
- Mouse settings (Windows pointer precision, speed, etc.)  
- Polling Rate *(confirm stability at 1000/2000/4000/8000 depending on device)*  
- Freya Wooting Settings *(rapid trigger / actuation tuned for consistency)*  

**Important:** Input tweaks should be validated in-game and in aim trainers; instability = worse aim.

---

### F) GPU & Game-Specific Optimization
- Nvidia Control Panel  
- NVIDIA Profile Inspector *(for profile-level tuning; avoid unsafe flags)*  
- Game file properties tweaks  
- Override high DPI scaling *(only if the game has scaling/input issues)*  
- Steam Launch Options *(if applicable)*  
- GameSettings.ini *(ARC Raiders config tuning section)*  
- High Graphics settings *(in-game settings + Windows per-app)*  

---

### G) Performance Tools (situational)
- Intelligent Standby List Cleaner (ISLC)  
- RivaTuner (RTSS) *(for frame cap + frametime stability)*  
- Process Lasso *(CPU priority/affinity only if it helps; test)*  
- r6 tracker *(not relevant to ARC Raiders; optional section can be removed in this repo)*  
- Ultimate Windows Tweaker 5 (Windows 11) *(use carefully; document changes)*  

---

### H) Audio / Footsteps (preference-based)
- Freya best footstep EQ settings *(ARC Raiders audio clarity profile)*  

---

### I) Discord Tweaks (small but useful)
- Discord tweaks *(disable hardware acceleration if it causes hitching; reduce overlay/background load)*  

---

## 5) Tools used in this guide
This repo references well-known utilities. Use official sources only.
- Intelligent Standby List Cleaner (ISLC)
- RivaTuner Statistics Server (RTSS)
- Process Lasso
- NVIDIA Control Panel / NVIDIA App
- NVIDIA Profile Inspector
- Windows built-in cleanup + DISM/SFC tooling
- Optional: TCP tuning utility (conservative presets)

> **Rule:** If a tool tries to install extra “optimizers” or bundles, skip it.

---

## 6) Benchmarking (so you know it worked)
Recommended approach:
- Use the same scene/area
- Same resolution + same in-game settings
- Run 2–3 passes and average results

Track:
- Avg FPS
- 1% lows / 0.1% lows
- Frametime spikes (stutter)
- Input “feel” (only after data)

If a tweak doesn’t improve your metrics or consistency, revert it.

---

## 7) Reverting changes
Every section in this guide is designed to be reversible.
General rollback methods:
- Restore Point (fastest full rollback)
- Revert registry exports
- Reset NVIDIA profile to defaults
- Remove launch options
- Restore original config files
- Undo power plan / Windows settings

---

## 8) Credits
I spend real time researching and testing to get the most FPS and lowest latency possible.

If this guide helped you:
- Subscribe to my YouTube (search: **freyar6**)
- TikTok: **@freyar6**
- Share the repo with a hint: “benchmark it first”

---

## Roadmap
- [ ] Add **ARC Raiders recommended in-game settings** presets (FPS / Balanced / Competitive)
- [ ] Add **RTSS cap guide** (120/144/165/240/360 best practices)
- [ ] Add **NVIDIA profile presets** (with explanations + rollback)
- [ ] Add **safe PowerShell scripts** (reviewable, no hidden actions)
- [ ] Add **troubleshooting** (stutter, crash, high CPU, shader compile, input delay)

---

### Status
**INCOMING**
