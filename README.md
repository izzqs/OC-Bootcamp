# 🖥️ OC Bootcamp

### One-click Windows booting for OpenCore Hackintosh systems

OC Bootcamp is a lightweight macOS menu-bar application that lets you restart directly into Windows without manually selecting Windows from the OpenCore boot picker.

<p align="center">
  <strong>Version 1.0.1</strong>
</p>

---

## ✨ Features

- 🚀 **One-click Windows boot** — restart into Windows from the macOS menu bar.
- 🔍 **Automatic boot-entry detection** — detects the Windows Boot Manager entry instead of relying on a fixed `OCBt` index.
- 🔄 **One-time boot selection** — requests Windows for the next startup.
- 🔐 **Privileged helper** — avoids repeated administrator-password prompts after initial setup.
- 📦 **Simple installation** — distributed as a macOS DMG.

## 💻 Compatibility

**Tested on macOS Tahoe 26.7.1.**

Other macOS versions are **not guaranteed to work**.

### Requirements

- A compatible Mac or Hackintosh running macOS.
- OpenCore as the boot manager.
- Windows installed and bootable through OpenCore.
- Administrator access for initial setup.

Compatibility also depends on your firmware, OpenCore configuration, and Windows boot setup.

---

## 📥 Installation

1. Download `OC-Bootcamp.dmg` from the **Releases** section.
2. Open the downloaded DMG.
3. Drag **OC Bootcamp.app** into your **Applications** folder.
4. Run **Install Privileged Helper.command** from the mounted DMG.
5. Enter your administrator password when prompted.
6. Launch **OC Bootcamp.app** from Applications.

> **Security notice:** Only install the privileged helper from a release you trust.

## 🕹️ How to Use

1. Launch OC Bootcamp in macOS.
2. Click the OC Bootcamp menu-bar icon.
3. Select **Restart to Windows**.
4. The app detects the Windows boot entry and requests a one-time Windows boot.
5. Your computer restarts into Windows if the request succeeds.
6. Restart Windows normally to return to your usual OpenCore boot behavior.

**Tip:** Ensure macOS remains accessible through the OpenCore picker before relying on unattended OS switching.

---

## 🗑️ Uninstallation

1. Open the original OC Bootcamp DMG, or download it again from Releases.
2. Run **Uninstall Privileged Helper.command**.
3. Follow the prompts.
4. Remove **OC Bootcamp.app** from Applications.

Use the supplied uninstaller rather than manually deleting privileged helper files.

## 🛠️ Troubleshooting

<details>
<summary><strong>Windows is not detected</strong></summary>

- Confirm Windows boots successfully from the OpenCore picker.
- Check that the Windows UEFI entry points to `\EFI\Microsoft\Boot\bootmgfw.efi`.
- Verify that OpenCore exposes the required boot-entry NVRAM variables.

</details>

<details>
<summary><strong>The app repeatedly asks for an administrator password</strong></summary>

- Run **Install Privileged Helper.command** again from a trusted release.
- If the problem persists, open a GitHub Issue with your macOS version and the exact error message.

</details>

<details>
<summary><strong>The computer does not boot into Windows</strong></summary>

- Use the OpenCore picker to select macOS if necessary.
- Check your OpenCore boot entries before retrying.
- Never interrupt power to a responsive computer as a troubleshooting shortcut.

</details>

---

## 🙏 Credits

- [**BootChamp**](https
