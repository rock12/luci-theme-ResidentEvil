# ☣️ luci-theme-ResidentEvil (Umbrella Corporation Edition)

[![OpenWrt](https://img.shields.io/badge/OpenWrt-23.05%20%7C%2024.10%20%7C%2025.12%2B-blue?style=flat-square&logo=openwrt)](https://openwrt.org/)
[![LuCI](https://img.shields.io/badge/LuCI-ucode-success?style=flat-square)](https://github.com/openwrt/luci)
[![Theme](https://img.shields.io/badge/Style-Umbrella%20Corporation-red?style=flat-square)](https://github.com/rock12/luci-theme-ResidentEvil)
[![Release](https://img.shields.io/github/v/release/rock12/luci-theme-ResidentEvil?style=flat-square&color=crimson)](https://github.com/rock12/luci-theme-ResidentEvil/releases/latest)
[![License](https://img.shields.io/badge/License-Apache%202.0-orange?style=flat-square)](LICENSE)

A high-tech dark LuCI theme for OpenWrt (23.05, 24.10, 25.12+), inspired by the **Resident Evil** universe and styled after the covert **Umbrella Corporation Hive Security Terminal**.

[**Читать описание на русском языке (README_ru.md)**](README_ru.md)

> **Based on:** the outstanding [**luci-theme-proton2025**](https://github.com/ChesterGoodiny/luci-theme-proton2025) by [**ChesterGoodiny**](https://github.com/ChesterGoodiny).  
> Sincere gratitude to ChesterGoodiny for the modern ucode foundation, exceptional performance, and comprehensive settings framework.

---

## 📸 Screenshots

### Authentication Screen (Hive Security Terminal)
*Leon S. Kennedy (R.P.D.) and Ada Wong frame the central Umbrella Corporation login terminal:*
![Resident Evil Login Screen](docs/login.png)

---

### Dashboard (Resident Evil System Overview)
*Live service monitoring, multi-zone temperature sensors, and centered status cards:*
![Resident Evil Dashboard](docs/status.png)

---

## ☣️ Features & Modifications

### 🧟 1. Cinematic Login Interface
- **High-definition character art:** Leon S. Kennedy on the left and Ada Wong on the right, perfectly framing wide desktop displays without encroaching on login inputs.
- **Umbrella Security Terminal:** Styled login card featuring `UMBRELLA CORPORATION [ LEVEL 8 CLASSIFIED ACCESS ]`.
- **Atmospheric effects:** Dark rolling fog, rain particles, and crimson embers floating around the Umbrella emblem.

### 🛡️ 2. Umbrella Corporation Aesthetic
- **Vector SVG Assets:** Authentic 8-segment scalloped red & white Umbrella badges in navigation and login (`logo.svg`, `brand.svg`).
- **Color Palette:** Stealth carbon background (`#080a0e`) accented by Umbrella Crimson (`#dc2626` / `#ef4444`).
- **Glassmorphism:** Translucent UI cards with subtle borders and smooth backdrop blur (`backdrop-filter`).
- **Refined UX:**
  - "No password set!" banner repositioned neatly at the top with an interactive dismiss button (`×`).
  - Translucent modal backdrops (no more opaque black screens when sessions expire).
  - Centered, well-aligned system status tables.

### 📊 3. Integrated Interactive Widgets (Overview)
- **Real-time Temperature Widget:**
  - Live readings from CPU thermal zones and Wi-Fi chips (MT7915 PHY0/PHY1).
  - All 4 sensor cards organized in a sleek single horizontal row.
  - Color-coded levels (FINE / CAUTION / DANGER) with peak temperature tracking and animated pulse dots.
- **Service Monitoring Widget:**
  - Real-time status for essential daemons (Dnsmasq, Dropbear, Uhttpd).
  - Cards matching the exact height and visual layout of temperature cards.
  - Direct `[+ Add]` action button in the widget header.
- **Widget Configuration Modal:**
  - Dedicated `[⚙ Widget Settings]` button with instant toggles and search filter.

---

## 🛠️ Requirements

- **OpenWrt:** 23.05, 24.10, 25.12+ (snapshots and release builds)
- **LuCI:** ucode-based (`luci-base`)
- **Architecture:** `all` (architecture-independent, compatible with ARM, MediaTek, x86_64, Qualcomm, MIPS, etc.)
- Root SSH access to your router.

---

## 🚀 One-Command Installation

Connect to your router via SSH and run:

```sh
wget -qO- https://raw.githubusercontent.com/rock12/luci-theme-ResidentEvil/main/install.sh | sh
```

> **The installer automatically:**
> 1. Detects your package manager (`apk` for newer releases or `opkg` for standard builds).
> 2. Fetches the latest matching package from GitHub Releases.
> 3. Installs and switches LuCI to the theme immediately.

After installation, refresh your browser with cache clearing (**Ctrl + F5**).

---

## 🔄 Updating

To update to the latest version, run the install command again:

```sh
wget -qO- https://raw.githubusercontent.com/rock12/luci-theme-ResidentEvil/main/install.sh | sh
```

---

## 🗑️ Removal

To revert to the default LuCI theme and uninstall:

```sh
wget -qO- https://raw.githubusercontent.com/rock12/luci-theme-ResidentEvil/main/uninstall.sh | sh
```

---

## 📦 Manual Installation from Releases

Pre-built packages are published on [**GitHub Releases**](https://github.com/rock12/luci-theme-ResidentEvil/releases/latest):

- **`.apk`** — for OpenWrt 25.12+ (`apk` package manager):
  ```sh
  apk add /tmp/luci-theme-proton2025-*.apk
  ```
- **`.ipk`** — for OpenWrt 23.05 / 24.10 (`opkg` package manager):
  ```sh
  opkg install /tmp/luci-theme-proton2025_*_all.ipk
  ```

---

## 👥 Credits

- **Original theme base:** [ChesterGoodiny/luci-theme-proton2025](https://github.com/ChesterGoodiny/luci-theme-proton2025) (Apache-2.0).
- **Resident Evil & Umbrella Corp Styling:** [rock12](https://github.com/rock12/luci-theme-ResidentEvil).
- **Inter Font:** The Inter Project Authors (SIL Open Font License 1.1).
- **Animation Components:** Pavel Dobryakov (WebGL Fluid Simulation, MIT).

---

## 📄 License

Licensed under **Apache 2.0**. See [LICENSE](LICENSE) for details.
