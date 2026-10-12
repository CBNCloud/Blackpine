# Blackpine Desktop

Windows workspace for authorized Blackpine users, with Customer 360, Prospect, FS Ticket and a built-in Fortinet SSL VPN client.

[Download Blackpine](https://github.com/CBNCloud/Blackpine/releases/latest)

Version **0.8.5** adds subtle per-block loading indicators, app-wide text size
controls in Settings (80–150%), and a prominent **New version available** banner
with Update now and Later. It retains the header alignment and active subscription
duration improvements from 0.8.4.

Each release has **one asset: Blackpine.Setup.exe**. It is the complete Windows x64 installer, including the VPN engine and service. Application source, source archives, build projects and internal documentation are not published here or included in the installer.

## Install and update

Run the installer, approve Windows elevation and choose Install / update. Open Blackpine Desktop from the Start menu. Microsoft Edge WebView2 Runtime is required.

On an office LAN or an existing external VPN route that can reach Blackpine, sign in directly; the built-in VPN and FortiClient are optional. Version 0.8.3 checks Blackpine's TCP port before automatically connecting VPN. The green dot shows ping reachability; account sign-in is still required.

When a VPN is needed, enter the VPN Gateway, Port and credentials provided by your administrator. Blackpine remembers them securely for your Windows account only after its own VPN connection succeeds. Then sign in to Blackpine. No gateway or custom port is preset. Existing FortiClient connections are left alone.

Starting with 0.8.1, installed Blackpine checks for updates at startup and every six hours. The Updates button beside the version label checks manually. The app verifies signed release metadata and the full installer's hash before opening setup; you approve installation and elevation. Earlier versions require one manual upgrade.

This installer is currently not Authenticode signed, so Windows may show an unknown-publisher or SmartScreen warning. Bundle hardening discourages casual inspection; it does not make a public binary confidential. The client does not grant VPN or Blackpine account authorization.

## Open-source libraries

Required third-party license notices are included in the installer. Corresponding library sources, patches and build recipes are available from the upstream links below. These are third-party libraries, not Blackpine application source. No source archives are hosted in this repository's release assets. Library replacement instructions and applicable permissions accompany the installed third-party notices.
- [gnutls 3.8.11](https://mirror.math.princeton.edu/pub/fedora-archive/fedora/linux/updates/42/Everything/source/tree/Packages/g/gnutls-3.8.11-3.fc42.src.rpm)
- [mingw-gcc 14.2.1](https://mirror.math.princeton.edu/pub/fedora-archive/fedora/linux/releases/42/Everything/source/tree/Packages/m/mingw-gcc-14.2.1-4.fc42.src.rpm)
- [mingw-gettext 0.23.1](https://mirror.math.princeton.edu/pub/fedora-archive/fedora/linux/releases/42/Everything/source/tree/Packages/m/mingw-gettext-0.23.1-2.fc42.src.rpm)
- [mingw-gmp 6.3.0](https://mirror.math.princeton.edu/pub/fedora-archive/fedora/linux/releases/42/Everything/source/tree/Packages/m/mingw-gmp-6.3.0-2.fc42.src.rpm)
- [mingw-libtasn1 4.21.0](https://mirror.math.princeton.edu/pub/fedora-archive/fedora/linux/updates/42/Everything/source/tree/Packages/m/mingw-libtasn1-4.21.0-1.fc42.src.rpm)
- [mingw-libxml2 2.12.9](https://mirror.math.princeton.edu/pub/fedora-archive/fedora/linux/releases/42/Everything/source/tree/Packages/m/mingw-libxml2-2.12.9-2.fc42.src.rpm)
- [mingw-lz4 1.9.4](https://download.copr.fedorainfracloud.org/results/dwmw2/openconnect/fedora-42-x86_64/Packages/m/mingw-lz4-1.9.4-1.fc41.src.rpm)
- [mingw-nettle 3.7.2](https://mirror.math.princeton.edu/pub/fedora-archive/fedora/linux/releases/42/Everything/source/tree/Packages/m/mingw-nettle-3.7.2-12.fc42.src.rpm)
- [mingw-stoken 0.92](https://download.copr.fedorainfracloud.org/results/dwmw2/openconnect/fedora-42-x86_64/Packages/m/mingw-stoken-0.92-3.fc41.src.rpm)
- [mingw-win-iconv 0.0.8](https://mirror.math.princeton.edu/pub/fedora-archive/fedora/linux/releases/42/Everything/source/tree/Packages/m/mingw-win-iconv-0.0.8-14.fc42.src.rpm)
- [mingw-winpthreads 12.0.0](https://mirror.math.princeton.edu/pub/fedora-archive/fedora/linux/releases/42/Everything/source/tree/Packages/m/mingw-winpthreads-12.0.0-4.fc42.src.rpm)
- [mingw-zlib 1.3.2](https://mirror.math.princeton.edu/pub/fedora-archive/fedora/linux/updates/42/Everything/source/tree/Packages/m/mingw-zlib-1.3.2-1.fc42.src.rpm)
- [openconnect 9.21](https://gitlab.com/openconnect/openconnect/-/archive/v9.21/openconnect-v9.21.tar.gz)
- [Wintun 0.14.1](https://www.wintun.net/builds/wintun-0.14.1.zip)
