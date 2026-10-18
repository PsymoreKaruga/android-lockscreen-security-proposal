# Proposal: Restrict Quick Settings Toggles on Locked Screen (Android / SystemUI)

Proposal and security threat model requesting Android (AOSP) & OEMs to require authentication for Quick Settings toggles (Airplane Mode/DND) on locked devices.

## Overview
Currently on stock Android (AOSP) and OEM distributions (e.g., Tecno HiOS), users can swipe down the Quick Settings notification shade and toggle connectivity states (Airplane Mode, Mobile Data, Wi-Fi) or sound modes (Do Not Disturb) on a locked device without entering credentials.

## Security & Threat Model Impact
When a device is stolen, an attacker immediately:
1. Enables **Airplane Mode** or turns off **Mobile Data/Wi-Fi**.
2. Cuts off communication with **Google Find My Device** and remote wipe/location tracking tools.
3. Silences emergency alarms via **Do Not Disturb (DND)**.

This completely neutralizes anti-theft tracking before the victim can react.

## Proposed Security Policy Change
Provide a system configuration option (`Settings > Security & Privacy > Lock Screen`) to:
- Require PIN/Pattern/Biometrics before expanding Quick Settings on the lock screen.
- Restrict sensitive quick settings tiles (Airplane Mode, Mobile Data, Hotspot, Location, Power Off) behind authentication.

## Tracking & References
- **Google Issue Tracker:** [Link your submitted Issue Tracker URL here once created]
- **Target OS Component:** `SystemUI / Keyguard`
