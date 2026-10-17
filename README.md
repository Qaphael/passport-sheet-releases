# 🪪 Passport Sheet

<p align="center">
  <strong>Fast, print-ready passport and ID photo sheets — 100% offline, private, and precise.</strong>
</p>

<p align="center">
  <a href="https://github.com/Qaphael/passport-sheet-releases/releases/latest"><img src="https://img.shields.io/badge/Platform-Windows%2010%20%7C%2011%20(64--bit)-0078D4?style=flat-square&logo=windows&logoColor=white" alt="Platform: Windows" /></a>
  <a href="https://github.com/Qaphael/passport-sheet-releases/releases/latest"><img src="https://img.shields.io/badge/Release-v1.4.0-emerald?style=flat-square" alt="Version 1.4.0" /></a>
  <img src="https://img.shields.io/badge/Resolution-300%20DPI%20Print--Ready-purple?style=flat-square" alt="300 DPI" />
  <img src="https://img.shields.io/badge/Privacy-100%25%20Offline%20Local%20AI-success?style=flat-square" alt="100% Offline" />
  <img src="https://img.shields.io/badge/License-MIT-blue?style=flat-square" alt="License: MIT" />
</p>

<p align="center">
  <a href="https://github.com/Qaphael/passport-sheet-releases/releases/latest/download/passport-sheet-setup.exe">
    <img src="https://img.shields.io/badge/⬇️%20Download-Passport_Sheet_Setup.exe-0078D4?style=for-the-badge&logo=windows&logoColor=white" height="42" alt="Download Passport Sheet" />
  </a>
</p>

---

## 🌟 Overview

**Passport Sheet** is a modern desktop application that transforms ordinary portrait photos into print-ready sheets of compliant passport and ID photos in seconds.

Whether printing on standard **4×6″ (10×15 cm) photo paper**, **5×7″**, or **A4**, Passport Sheet handles exact millimetre geometry, auto-alignment, AI-powered background replacement, and smart multi-person packing — completely offline on your own computer.

---

## ✨ Features at a Glance

### 🎯 Auto-Fit & Biometric Compliance
- **AI Face Detection**: Uses on-device YuNet neural vision to locate facial landmarks and eye levels automatically.
- **Biometric Head Ratio**: Automatically scales and centres the subject to match passport issuing standards (ICAO, US, EU/UK/Schengen).
- **6-Point Compliance Report**: Live verification of eye gaze, head tilt, lighting contrast, centering, and margin clearance.

### ✂️ Instant Offline Background Removal
- **Local AI Matting**: Bundled with high-accuracy local neural matting models (`u2net_human_seg`, `silueta`).
- **Zero Cloud Uploads**: Works entirely on your CPU without internet access or subscriptions.
- **Backdrop Palette**: Seamlessly switch between official pure white (`#FFFFFF`), light gray, baby blue, or custom background colors.
- **Edge Refinement**: Interactive edge shift, feathering, and color decontamination controls.

### 👥 Multi-Person Combined Sheets
- **Smart Sheet Packing**: Combine photos of different people, family members, or customer orders into the fewest possible 4×6″ sheets.
- **Drag-and-Drop Slot Grid**: Effortlessly swap, reorder, or duplicate tiles on the sheet with live preview and keyboard shortcuts.
- **Guaranteed No-Split Rules**: Ensures multi-copy orders stay grouped together on the same physical print.

### 🖨️ Precision Print Geometry
- **True 300 DPI Output**: Every sheet exports at exact print resolution (e.g. 1800×1200 px for standard 6×4″ prints).
- **Standard Presets**:
  - **Photos**: 35×45 mm (UK/EU/Schengen), 2×2″ (51×51 mm US), 40×60 mm, 33×48 mm, and custom.
  - **Sheets**: 4×6″ (10×15 cm), 5×7″ (13×18 cm), and A4.
- **Cut Guides**: Built-in 1 px precision cut marks and borders calibrated for scissors or rotary trimmers.
- **Printer Profiles**: Pre-calibrated margins for borderless photo paper and standard home/lab printers (Epson, Canon, HP).

### 🔒 100% Offline & Private
- **Zero Telemetry**: No trackers, no telemetry, no analytics.
- **Local Data Retention**: Client photos stay strictly inside your local AppData folder and can be purged automatically after printing or wiped with a single click.

### 🔄 Verified In-App Updates
- Built-in updater with cryptographic **Ed25519 signature verification**.
- Single plain check with zero user identifiers — never interrupts your offline workflow.

---

## 🚀 Quick Start Guide

### 1. Download & Install
1. Download **[`passport-sheet-setup.exe`](https://github.com/Qaphael/passport-sheet-releases/releases/latest/download/passport-sheet-setup.exe)** from the latest release.
2. Run the installer. It installs per-user (no administrative permissions required).
3. Launch **Passport Sheet** from your Start Menu or Desktop.

### 2. Creating Your First Sheet
1. **Import Photo**: Drag and drop any portrait picture, click **Browse**, or capture directly from your webcam.
2. **Auto-Fit**: Click **Auto-fit** to automatically center the face, level the eyes, and conform to the selected document standard.
3. **Background**: Toggle **Remove background** to replace the backdrop with pure white or your required color.
4. **Choose Quantity**: Select how many copies you want (1 to 8 tiles per sheet).
5. **Export**: Click **Export PDF** (ready to print at 100% scale), or choose **PNG** / **JPEG**.

---

## 📐 Document & Sheet Geometry Specifications

| Standard | Photo Dimensions (mm) | Photo Dimensions (px @ 300 DPI) | Max per 4×6″ Sheet |
|---|---|---|---|
| **Standard Passport / Schengen / UK** | 35 × 45 mm | 413 × 531 px | **8 photos** (4 × 2) |
| **US Passport / Visa** | 2 × 2 in (51 × 51 mm) | 600 × 600 px | **2 photos** (2 × 1) |
| **Canadian Passport** | 50 × 70 mm | 591 × 827 px | **2 photos** (2 × 1) |
| **Large ID** | 40 × 60 mm | 472 × 709 px | **4 photos** (2 × 2) |
| **China Passport** | 33 × 48 mm | 390 × 567 px | **6 photos** (3 × 2) |

---

## 💻 System Requirements

- **Operating System**: Windows 10 or Windows 11 (64-bit)
- **Web Runtime**: Microsoft Edge WebView2 (installed by default on Windows 10/11)
- **Hardware**: Any modern 64-bit multi-core CPU (no dedicated GPU required)

---

## 🛠️ Technology Stack

- **Desktop Shell**: Python 3.12 + FastAPI + `pywebview` (native Windows WebView2)
- **Image Pipeline**: Pillow, NumPy, ONNX Runtime (CPU Execution Provider)
- **AI Models**:
  - Face Detection: `YuNet` (ONNX, ~200 KB)
  - Subject Matting: `U2-Net / Silueta` (ONNX, bundled locally)
- **Frontend**: React 18, TypeScript, Tailwind CSS, Radix UI, Vite
- **Packaging**: PyInstaller (`--onedir`, UPX off) + Inno Setup 6

---

## 🔒 Verification & Integrity

Every official release includes cryptographic checksums:
- **Installer Hash**: Verified via `passport-sheet-setup.exe.sha256`
- **Release Manifest**: Signed with CI Ed25519 private key, verified locally with embedded public key before any update executes.

To verify your installer locally in PowerShell:
```powershell
Get-FileHash .\passport-sheet-setup.exe -Algorithm SHA256
```

---

## 📄 License

Licensed under the [MIT License](LICENSE). Third-party open source licenses and model redistribution notices are documented in `THIRD_PARTY_NOTICES.txt` bundled with every release.
