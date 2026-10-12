# Blackpine Desktop

Windows desktop workspace for authorized Blackpine users: Customer 360, Prospect and FS Ticket, with an integrated Fortinet SSL VPN client.

[Download the latest Windows x64 installer](https://github.com/CBNCloud/Blackpine/releases/latest)

## Install

1. Download **Blackpine.Setup.exe** from Releases. Keep the complete installer; it includes dependency licenses, corresponding native sources and the Blackpine rebuild kit.
2. Run it, approve the Windows administrator prompt, and choose **Install / update**. Microsoft Edge WebView2 Runtime is required.
3. Open **Blackpine Desktop** from the Start menu. In the VPN dialog enter the **VPN Gateway**, **Port**, username and password provided by your administrator.
4. After Blackpine establishes its own VPN connection, those details are saved encrypted for your Windows account. Then sign in to Blackpine using your own account.

The installer is currently **not Authenticode signed**. Windows may show an unknown-publisher or SmartScreen warning. Distribution hashes and signed update metadata serve different purposes from Windows publisher signing.

## Updates

Starting with 0.8.0, installed Blackpine checks for updates at startup and every six hours while open. Choose **Updates** to check manually. A newer version offers a download; the app verifies a pinned-key signature and the installer hash before opening setup. You approve installation and Windows elevation. Blackpine closes when setup starts; open it again from the Start menu afterward.

Users on 0.7.9 or earlier must install 0.8.0 manually once. Re-enter VPN details on this first upgrade; the old fixed-gateway credential entry is not used. Changing the gateway or port clears the autofilled password. **Forget VPN details** removes the new saved profile. An existing FortiClient connection is left alone and does not count as validation of newly entered VPN details.

## Scope

This is the public distribution repository. Its main branch contains this README; release assets contain the installer, SHA-256 checksums and signed update metadata. Application source and rebuild permissions remain included inside the installer, under `C:\Program Files\Blackpine\notices` after installation. No VPN gateway or custom port is built into this version.

The application preserves reviewed read-only Blackpine routes and does not change VPN gateway authorization. Access remains subject to your organization's active accounts and network controls. Bundle hardening discourages casual binary inspection; the supplied rebuild source remains readable.

Before organization-wide deployment, validate network outage recovery, sleep/resume, session expiry and uninstall in your own environment. See the installed `notices\VPN.md` for validation scope and operating details.
